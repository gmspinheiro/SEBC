# Changes
I have changed the number of records being produced by the teragen to the according 10GB size desired. Also, and according to my cluster, I changed the script to try the following combinations: 1, 2 and 4 mappers; 1, 2 and 4 reducers; 512MB, 1G and 2G of RAM.

#### YARNtest.sh
````
#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
HADOOP=/opt/cloudera/parcels/CDH/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 1 2 4
do
   # Reducer containers
   for j in 1 2 4
   do
      # Container memory
      for k in 512 1024 2048
      do
         echo "#Mapper containers $i"
         echo "#Reducer containers: $j"
         echo "#Container memory: $k"

         # Set mapper JVM heap
         MAP_MB=`echo "($k*0.8)/1" | bc`

         # Set reducer JVM heap
         RED_MB=`echo "($k*0.8)/1" | bc`

        time ${HADOOP}/yarn jar ${MR}/hadoop-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     102400000 /results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err

        time ${HADOOP}/yarn jar $MR/hadoop-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                     /results/tg-10GB-${i}-${j}-${k}  \
                     /results/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err

        $HADOOP/hadoop fs -rm -r -skipTrash /results/tg-10GB-${i}-${j}-${k}
        $HADOOP/hadoop fs -rm -r -skipTrash /results/ts-10GB-${i}-${j}-${k}        
      done
   done
done

echo Testing loop ended on `date`
````
