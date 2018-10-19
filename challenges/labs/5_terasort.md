````
[root@sebce2 ~]# kinit raffles
Password for raffles@GMSPINHEIRO.SG:
[root@sebce2 ~]# time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort -Dmapreduce.job.maps=6 -Dmapreduce.job.reduces=6 /user/raffles/tgen512 /user/raffles/tsort512
18/10/19 09:03:00 INFO terasort.TeraSort: starting
18/10/19 09:03:03 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939782992, maxDate=1540544582992, sequenceNumber=1, masterKeyId=2 on 10.0.6.4:8020
18/10/19 09:03:03 INFO security.TokenCache: Got dt for hdfs://sebce1.madrid.es:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.6.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939782992, maxDate=1540544582992, sequenceNumber=1, masterKeyId=2)
18/10/19 09:03:03 INFO input.FileInputFormat: Total input paths to process : 6
Spent 720ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 724ms
Sampling 10 splits of 156
Making 6 from 100000 sampled records
Computing parititions took 813ms
Spent 1540ms computing partitions.
18/10/19 09:03:04 INFO client.RMProxy: Connecting to ResourceManager at sebce1.madrid.es/10.0.6.4:8032
18/10/19 09:03:04 INFO mapreduce.JobSubmitter: number of splits:156
18/10/19 09:03:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539939657459_0001
18/10/19 09:03:05 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.6.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539939782992, maxDate=1540544582992, sequenceNumber=1, masterKeyId=2)
18/10/19 09:03:06 INFO impl.YarnClientImpl: Submitted application application_1539939657459_0001
18/10/19 09:03:06 INFO mapreduce.Job: The url to track the job: http://sebce1.madrid.es:8088/proxy/application_1539939657459_0001/
18/10/19 09:03:06 INFO mapreduce.Job: Running job: job_1539939657459_0001
18/10/19 09:03:15 INFO mapreduce.Job: Job job_1539939657459_0001 running in uber mode : false
18/10/19 09:03:15 INFO mapreduce.Job:  map 0% reduce 0%
18/10/19 09:03:27 INFO mapreduce.Job:  map 1% reduce 0%
18/10/19 09:03:28 INFO mapreduce.Job:  map 2% reduce 0%
18/10/19 09:03:35 INFO mapreduce.Job:  map 4% reduce 0%
18/10/19 09:03:36 INFO mapreduce.Job:  map 8% reduce 0%
18/10/19 09:03:38 INFO mapreduce.Job:  map 9% reduce 0%
18/10/19 09:03:46 INFO mapreduce.Job:  map 10% reduce 0%
18/10/19 09:03:47 INFO mapreduce.Job:  map 12% reduce 0%
18/10/19 09:03:48 INFO mapreduce.Job:  map 16% reduce 0%
18/10/19 09:03:55 INFO mapreduce.Job:  map 17% reduce 0%
18/10/19 09:03:57 INFO mapreduce.Job:  map 18% reduce 0%
18/10/19 09:03:59 INFO mapreduce.Job:  map 19% reduce 0%
18/10/19 09:04:00 INFO mapreduce.Job:  map 21% reduce 0%
18/10/19 09:04:01 INFO mapreduce.Job:  map 23% reduce 0%
18/10/19 09:04:03 INFO mapreduce.Job:  map 24% reduce 0%
18/10/19 09:04:07 INFO mapreduce.Job:  map 25% reduce 0%
18/10/19 09:04:12 INFO mapreduce.Job:  map 26% reduce 0%
18/10/19 09:04:13 INFO mapreduce.Job:  map 28% reduce 0%
18/10/19 09:04:14 INFO mapreduce.Job:  map 31% reduce 0%
18/10/19 09:04:16 INFO mapreduce.Job:  map 32% reduce 0%
18/10/19 09:04:21 INFO mapreduce.Job:  map 33% reduce 0%
18/10/19 09:04:24 INFO mapreduce.Job:  map 35% reduce 0%
18/10/19 09:04:26 INFO mapreduce.Job:  map 38% reduce 0%
18/10/19 09:04:29 INFO mapreduce.Job:  map 39% reduce 0%
18/10/19 09:04:35 INFO mapreduce.Job:  map 42% reduce 0%
18/10/19 09:04:36 INFO mapreduce.Job:  map 44% reduce 0%
18/10/19 09:04:38 INFO mapreduce.Job:  map 45% reduce 0%
18/10/19 09:04:39 INFO mapreduce.Job:  map 46% reduce 0%
18/10/19 09:04:46 INFO mapreduce.Job:  map 47% reduce 0%
18/10/19 09:04:50 INFO mapreduce.Job:  map 48% reduce 0%
18/10/19 09:04:51 INFO mapreduce.Job:  map 49% reduce 0%
18/10/19 09:04:54 INFO mapreduce.Job:  map 50% reduce 0%
18/10/19 09:04:55 INFO mapreduce.Job:  map 51% reduce 0%
18/10/19 09:04:57 INFO mapreduce.Job:  map 52% reduce 0%
18/10/19 09:04:58 INFO mapreduce.Job:  map 53% reduce 0%
18/10/19 09:04:59 INFO mapreduce.Job:  map 54% reduce 0%
18/10/19 09:05:03 INFO mapreduce.Job:  map 55% reduce 0%
18/10/19 09:05:04 INFO mapreduce.Job:  map 56% reduce 0%
18/10/19 09:05:06 INFO mapreduce.Job:  map 57% reduce 0%
18/10/19 09:05:07 INFO mapreduce.Job:  map 58% reduce 0%
18/10/19 09:05:10 INFO mapreduce.Job:  map 60% reduce 0%
18/10/19 09:05:13 INFO mapreduce.Job:  map 61% reduce 0%
18/10/19 09:05:14 INFO mapreduce.Job:  map 62% reduce 0%
18/10/19 09:05:15 INFO mapreduce.Job:  map 63% reduce 0%
18/10/19 09:05:17 INFO mapreduce.Job:  map 65% reduce 0%
18/10/19 09:05:21 INFO mapreduce.Job:  map 66% reduce 0%
18/10/19 09:05:22 INFO mapreduce.Job:  map 67% reduce 0%
18/10/19 09:05:25 INFO mapreduce.Job:  map 70% reduce 0%
18/10/19 09:05:26 INFO mapreduce.Job:  map 71% reduce 0%
18/10/19 09:05:27 INFO mapreduce.Job:  map 72% reduce 0%
18/10/19 09:05:31 INFO mapreduce.Job:  map 73% reduce 0%
18/10/19 09:05:32 INFO mapreduce.Job:  map 74% reduce 0%
18/10/19 09:05:34 INFO mapreduce.Job:  map 75% reduce 0%
18/10/19 09:05:35 INFO mapreduce.Job:  map 76% reduce 0%
18/10/19 09:05:38 INFO mapreduce.Job:  map 78% reduce 0%
18/10/19 09:05:40 INFO mapreduce.Job:  map 79% reduce 0%
18/10/19 09:05:42 INFO mapreduce.Job:  map 80% reduce 0%
18/10/19 09:05:44 INFO mapreduce.Job:  map 82% reduce 0%
18/10/19 09:05:45 INFO mapreduce.Job:  map 83% reduce 0%
18/10/19 09:05:49 INFO mapreduce.Job:  map 85% reduce 0%
18/10/19 09:05:50 INFO mapreduce.Job:  map 86% reduce 0%
18/10/19 09:05:51 INFO mapreduce.Job:  map 87% reduce 0%
18/10/19 09:05:54 INFO mapreduce.Job:  map 88% reduce 0%
18/10/19 09:06:02 INFO mapreduce.Job:  map 88% reduce 5%
18/10/19 09:06:03 INFO mapreduce.Job:  map 90% reduce 5%
18/10/19 09:06:04 INFO mapreduce.Job:  map 91% reduce 10%
18/10/19 09:06:05 INFO mapreduce.Job:  map 92% reduce 10%
18/10/19 09:06:07 INFO mapreduce.Job:  map 92% reduce 24%
18/10/19 09:06:09 INFO mapreduce.Job:  map 93% reduce 24%
18/10/19 09:06:10 INFO mapreduce.Job:  map 93% reduce 25%
18/10/19 09:06:13 INFO mapreduce.Job:  map 94% reduce 26%
18/10/19 09:06:14 INFO mapreduce.Job:  map 95% reduce 26%
18/10/19 09:06:15 INFO mapreduce.Job:  map 96% reduce 26%
18/10/19 09:06:17 INFO mapreduce.Job:  map 97% reduce 26%
18/10/19 09:06:19 INFO mapreduce.Job:  map 97% reduce 27%
18/10/19 09:06:20 INFO mapreduce.Job:  map 99% reduce 27%
18/10/19 09:06:22 INFO mapreduce.Job:  map 100% reduce 27%
18/10/19 09:06:25 INFO mapreduce.Job:  map 100% reduce 45%
18/10/19 09:06:26 INFO mapreduce.Job:  map 100% reduce 51%
18/10/19 09:06:28 INFO mapreduce.Job:  map 100% reduce 58%
18/10/19 09:06:31 INFO mapreduce.Job:  map 100% reduce 65%
18/10/19 09:06:32 INFO mapreduce.Job:  map 100% reduce 68%
18/10/19 09:06:34 INFO mapreduce.Job:  map 100% reduce 70%
18/10/19 09:06:35 INFO mapreduce.Job:  map 100% reduce 75%
18/10/19 09:06:37 INFO mapreduce.Job:  map 100% reduce 81%
18/10/19 09:06:38 INFO mapreduce.Job:  map 100% reduce 83%
18/10/19 09:06:40 INFO mapreduce.Job:  map 100% reduce 85%
18/10/19 09:06:43 INFO mapreduce.Job:  map 100% reduce 87%
18/10/19 09:06:44 INFO mapreduce.Job:  map 100% reduce 88%
18/10/19 09:06:59 INFO mapreduce.Job:  map 100% reduce 96%
18/10/19 09:07:05 INFO mapreduce.Job:  map 100% reduce 98%
18/10/19 09:07:08 INFO mapreduce.Job:  map 100% reduce 100%
18/10/19 09:07:13 INFO mapreduce.Job: Job job_1539939657459_0001 completed successfully
18/10/19 09:07:14 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2274720347
                FILE: Number of bytes written=4522771007
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120019812
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=486
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=156
                Launched reduce tasks=6
                Data-local map tasks=156
                Total time spent by all maps in occupied slots (ms)=1504215
                Total time spent by all reduces in occupied slots (ms)=326867
                Total time spent by all map tasks (ms)=1504215
                Total time spent by all reduce tasks (ms)=326867
                Total vcore-milliseconds taken by all map tasks=1504215
                Total vcore-milliseconds taken by all reduce tasks=326867
                Total megabyte-milliseconds taken by all map tasks=1540316160
                Total megabyte-milliseconds taken by all reduce tasks=334711808
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2223497972
                Input split bytes=19812
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2223497972
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =936
                Failed Shuffles=0
                Merged Map outputs=936
                GC time elapsed (ms)=37777
                CPU time spent (ms)=869970
                Physical memory (bytes) snapshot=85237981184
                Virtual memory (bytes) snapshot=452597645312
                Total committed heap usage (bytes)=90869071872
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
18/10/19 09:07:14 INFO terasort.TeraSort: done

real    4m14.376s
user    0m12.551s
sys     0m0.675s
````
