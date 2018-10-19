````
[root@sebce1 krb5kdc]# kinit fullerton
Password for fullerton@GMSPINHEIRO.SG:
[root@sebce1 krb5kdc]# time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 5 5
Number of Maps  = 5
Samples per Map = 5
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Starting Job
18/10/19 09:04:07 INFO client.RMProxy: Connecting to ResourceManager at sebce1.madrid.es/10.0.6.4:8032
18/10/19 09:04:07 INFO hdfs.DFSClient: Created token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939847221, maxDate=1540544647221, sequenceNumber=2, masterKeyId=2 on 10.0.6.4:8020
18/10/19 09:04:07 INFO security.TokenCache: Got dt for hdfs://sebce1.madrid.es:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.6.4:8020, Ident: (token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939847221, maxDate=1540544647221, sequenceNumber=2, masterKeyId=2)
18/10/19 09:04:07 INFO input.FileInputFormat: Total input paths to process : 5
18/10/19 09:04:08 INFO mapreduce.JobSubmitter: number of splits:5
18/10/19 09:04:09 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539939657459_0002
18/10/19 09:04:09 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.6.4:8020, Ident: (token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939847221, maxDate=1540544647221, sequenceNumber=2, masterKeyId=2)
18/10/19 09:04:09 INFO impl.YarnClientImpl: Submitted application application_1539939657459_0002
18/10/19 09:04:09 INFO mapreduce.Job: The url to track the job: http://sebce1.madrid.es:8088/proxy/application_1539939657459_0002/
18/10/19 09:04:09 INFO mapreduce.Job: Running job: job_1539939657459_0002
18/10/19 09:04:31 INFO mapreduce.Job: Job job_1539939657459_0002 running in uber mode : false
18/10/19 09:04:31 INFO mapreduce.Job:  map 0% reduce 0%
18/10/19 09:04:44 INFO mapreduce.Job:  map 20% reduce 0%
18/10/19 09:04:45 INFO mapreduce.Job:  map 40% reduce 0%
18/10/19 09:04:47 INFO mapreduce.Job:  map 80% reduce 0%
18/10/19 09:04:48 INFO mapreduce.Job:  map 100% reduce 0%
18/10/19 09:05:03 INFO mapreduce.Job:  map 100% reduce 100%
18/10/19 09:05:04 INFO mapreduce.Job: Job job_1539939657459_0002 completed successfully
18/10/19 09:05:04 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=51
                FILE: Number of bytes written=904201
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1380
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=23
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=5
                Launched reduce tasks=1
                Data-local map tasks=5
                Total time spent by all maps in occupied slots (ms)=47769
                Total time spent by all reduces in occupied slots (ms)=9761
                Total time spent by all map tasks (ms)=47769
                Total time spent by all reduce tasks (ms)=9761
                Total vcore-milliseconds taken by all map tasks=47769
                Total vcore-milliseconds taken by all reduce tasks=9761
                Total megabyte-milliseconds taken by all map tasks=48915456
                Total megabyte-milliseconds taken by all reduce tasks=9995264
        Map-Reduce Framework
                Map input records=5
                Map output records=10
                Map output bytes=90
                Map output materialized bytes=167
                Input split bytes=790
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=167
                Reduce input records=10
                Reduce output records=0
                Spilled Records=20
                Shuffled Maps =5
                Failed Shuffles=0
                Merged Map outputs=5
                GC time elapsed (ms)=1230
                CPU time spent (ms)=6590
                Physical memory (bytes) snapshot=2588688384
                Virtual memory (bytes) snapshot=16769478656
                Total committed heap usage (bytes)=2750414848
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=590
        File Output Format Counters
                Bytes Written=97
Job Finished in 57.32 seconds
Estimated value of Pi is 3.68000000000000000000

real    1m1.672s
user    0m8.094s
sys     0m0.484s
````
