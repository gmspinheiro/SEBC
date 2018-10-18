# Teragen Command
````
[gmspinheiro@sebct1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000  /user/gmspinheiro/teragen_file
18/10/18 07:38:09 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848289638, maxDate=1540453089638, sequenceNumber=56, masterKeyId=6 on ha-hdfs:sebcgmspinheiro
18/10/18 07:38:09 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848289638, maxDate=1540453089638, sequenceNumber=56, masterKeyId=6)
18/10/18 07:38:09 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/18 07:38:10 INFO terasort.TeraGen: Generating 100000000 using 4
18/10/18 07:38:10 INFO mapreduce.JobSubmitter: number of splits:4
18/10/18 07:38:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539847360066_0001
18/10/18 07:38:11 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848289638, maxDate=1540453089638, sequenceNumber=56, masterKeyId=6)
18/10/18 07:38:12 INFO impl.YarnClientImpl: Submitted application application_1539847360066_0001
18/10/18 07:38:12 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539847360066_0001/
18/10/18 07:38:12 INFO mapreduce.Job: Running job: job_1539847360066_0001
18/10/18 07:38:21 INFO mapreduce.Job: Job job_1539847360066_0001 running in uber mode : false
18/10/18 07:38:21 INFO mapreduce.Job:  map 0% reduce 0%
18/10/18 07:38:42 INFO mapreduce.Job:  map 9% reduce 0%
18/10/18 07:38:48 INFO mapreduce.Job:  map 15% reduce 0%
18/10/18 07:38:54 INFO mapreduce.Job:  map 20% reduce 0%
18/10/18 07:39:00 INFO mapreduce.Job:  map 25% reduce 0%
18/10/18 07:39:16 INFO mapreduce.Job:  map 34% reduce 0%
18/10/18 07:39:22 INFO mapreduce.Job:  map 37% reduce 0%
18/10/18 07:39:28 INFO mapreduce.Job:  map 42% reduce 0%
18/10/18 07:39:34 INFO mapreduce.Job:  map 47% reduce 0%
18/10/18 07:39:40 INFO mapreduce.Job:  map 50% reduce 0%
18/10/18 07:39:56 INFO mapreduce.Job:  map 59% reduce 0%
18/10/18 07:40:02 INFO mapreduce.Job:  map 65% reduce 0%
18/10/18 07:40:09 INFO mapreduce.Job:  map 70% reduce 0%
18/10/18 07:40:15 INFO mapreduce.Job:  map 75% reduce 0%
18/10/18 07:40:31 INFO mapreduce.Job:  map 84% reduce 0%
18/10/18 07:40:37 INFO mapreduce.Job:  map 90% reduce 0%
18/10/18 07:40:43 INFO mapreduce.Job:  map 95% reduce 0%
18/10/18 07:40:49 INFO mapreduce.Job:  map 100% reduce 0%
18/10/18 07:40:49 INFO mapreduce.Job: Job job_1539847360066_0001 completed successfully
18/10/18 07:40:49 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=615408
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=283296
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=141648
                Total vcore-milliseconds taken by all map tasks=283296
                Total megabyte-milliseconds taken by all map tasks=290095104
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=524
                CPU time spent (ms)=168850
                Physical memory (bytes) snapshot=2310008832
                Virtual memory (bytes) snapshot=14787457024
                Total committed heap usage (bytes)=2230321152
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    2m43.843s
user    0m9.913s
sys     0m0.566s

````

# Terasort Command

````
[gmspinheiro@sebct1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/gmspinheiro/teragen_file /user/gmspinheiro/terasort_file
18/10/18 07:45:10 INFO terasort.TeraSort: starting
18/10/18 07:45:12 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848712192, maxDate=1540453512192, sequenceNumber=57, masterKeyId=6 on ha-hdfs:sebcgmspinheiro
18/10/18 07:45:12 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848712192, maxDate=1540453512192, sequenceNumber=57, masterKeyId=6)
18/10/18 07:45:12 INFO input.FileInputFormat: Total input paths to process : 4
Spent 525ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 531ms
Sampling 10 splits of 300
Making 4 from 100000 sampled records
Computing parititions took 682ms
Spent 1216ms computing partitions.
18/10/18 07:45:13 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/18 07:45:13 INFO mapreduce.JobSubmitter: number of splits:300
18/10/18 07:45:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539847360066_0002
18/10/18 07:45:13 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539848712192, maxDate=1540453512192, sequenceNumber=57, masterKeyId=6)
18/10/18 07:45:14 INFO impl.YarnClientImpl: Submitted application application_1539847360066_0002
18/10/18 07:45:14 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539847360066_0002/
18/10/18 07:45:14 INFO mapreduce.Job: Running job: job_1539847360066_0002
18/10/18 07:45:23 INFO mapreduce.Job: Job job_1539847360066_0002 running in uber mode : false
18/10/18 07:45:23 INFO mapreduce.Job:  map 0% reduce 0%
18/10/18 07:45:37 INFO mapreduce.Job:  map 1% reduce 0%
18/10/18 07:45:55 INFO mapreduce.Job:  map 2% reduce 0%
18/10/18 07:46:12 INFO mapreduce.Job:  map 3% reduce 0%
18/10/18 07:46:29 INFO mapreduce.Job:  map 4% reduce 0%
18/10/18 07:46:47 INFO mapreduce.Job:  map 5% reduce 0%
18/10/18 07:47:04 INFO mapreduce.Job:  map 6% reduce 0%
18/10/18 07:47:19 INFO mapreduce.Job:  map 7% reduce 0%
18/10/18 07:47:37 INFO mapreduce.Job:  map 8% reduce 0%
18/10/18 07:47:53 INFO mapreduce.Job:  map 9% reduce 0%
18/10/18 07:48:09 INFO mapreduce.Job:  map 10% reduce 0%
18/10/18 07:48:25 INFO mapreduce.Job:  map 11% reduce 0%
18/10/18 07:48:43 INFO mapreduce.Job:  map 12% reduce 0%
18/10/18 07:48:58 INFO mapreduce.Job:  map 13% reduce 0%
18/10/18 07:49:14 INFO mapreduce.Job:  map 14% reduce 0%
18/10/18 07:49:31 INFO mapreduce.Job:  map 15% reduce 0%
18/10/18 07:49:46 INFO mapreduce.Job:  map 16% reduce 0%
18/10/18 07:50:05 INFO mapreduce.Job:  map 17% reduce 0%
18/10/18 07:50:22 INFO mapreduce.Job:  map 18% reduce 0%
18/10/18 07:50:40 INFO mapreduce.Job:  map 19% reduce 0%
18/10/18 07:50:58 INFO mapreduce.Job:  map 20% reduce 0%
18/10/18 07:51:13 INFO mapreduce.Job:  map 21% reduce 0%
18/10/18 07:51:31 INFO mapreduce.Job:  map 22% reduce 0%
18/10/18 07:51:47 INFO mapreduce.Job:  map 23% reduce 0%
18/10/18 07:52:04 INFO mapreduce.Job:  map 24% reduce 0%
18/10/18 07:52:22 INFO mapreduce.Job:  map 25% reduce 0%
18/10/18 07:52:39 INFO mapreduce.Job:  map 26% reduce 0%
18/10/18 07:52:55 INFO mapreduce.Job:  map 27% reduce 0%
18/10/18 07:53:11 INFO mapreduce.Job:  map 28% reduce 0%
18/10/18 07:53:26 INFO mapreduce.Job:  map 29% reduce 0%
18/10/18 07:53:43 INFO mapreduce.Job:  map 30% reduce 0%
18/10/18 07:54:00 INFO mapreduce.Job:  map 31% reduce 0%
18/10/18 07:54:18 INFO mapreduce.Job:  map 32% reduce 0%
18/10/18 07:54:36 INFO mapreduce.Job:  map 33% reduce 0%
18/10/18 07:54:53 INFO mapreduce.Job:  map 34% reduce 0%
18/10/18 07:55:10 INFO mapreduce.Job:  map 35% reduce 0%
18/10/18 07:55:27 INFO mapreduce.Job:  map 36% reduce 0%
18/10/18 07:55:45 INFO mapreduce.Job:  map 37% reduce 0%
18/10/18 07:56:02 INFO mapreduce.Job:  map 38% reduce 0%
18/10/18 07:56:18 INFO mapreduce.Job:  map 39% reduce 0%
18/10/18 07:56:36 INFO mapreduce.Job:  map 40% reduce 0%
18/10/18 07:56:53 INFO mapreduce.Job:  map 41% reduce 0%
18/10/18 07:57:08 INFO mapreduce.Job:  map 42% reduce 0%
18/10/18 07:57:26 INFO mapreduce.Job:  map 43% reduce 0%
18/10/18 07:57:43 INFO mapreduce.Job:  map 44% reduce 0%
18/10/18 07:57:58 INFO mapreduce.Job:  map 45% reduce 0%
18/10/18 07:58:15 INFO mapreduce.Job:  map 46% reduce 0%
18/10/18 07:58:32 INFO mapreduce.Job:  map 47% reduce 0%
18/10/18 07:58:49 INFO mapreduce.Job:  map 48% reduce 0%
18/10/18 07:59:08 INFO mapreduce.Job:  map 49% reduce 0%
18/10/18 07:59:24 INFO mapreduce.Job:  map 50% reduce 0%
18/10/18 07:59:41 INFO mapreduce.Job:  map 51% reduce 0%
18/10/18 07:59:58 INFO mapreduce.Job:  map 52% reduce 0%
18/10/18 08:00:14 INFO mapreduce.Job:  map 53% reduce 0%
18/10/18 08:00:30 INFO mapreduce.Job:  map 54% reduce 0%
18/10/18 08:00:45 INFO mapreduce.Job:  map 55% reduce 0%
18/10/18 08:01:02 INFO mapreduce.Job:  map 56% reduce 0%
18/10/18 08:01:18 INFO mapreduce.Job:  map 57% reduce 0%
18/10/18 08:01:34 INFO mapreduce.Job:  map 58% reduce 0%
18/10/18 08:01:51 INFO mapreduce.Job:  map 59% reduce 0%
18/10/18 08:02:09 INFO mapreduce.Job:  map 60% reduce 0%
18/10/18 08:02:25 INFO mapreduce.Job:  map 61% reduce 0%
18/10/18 08:02:42 INFO mapreduce.Job:  map 62% reduce 0%
18/10/18 08:02:58 INFO mapreduce.Job:  map 63% reduce 0%
18/10/18 08:03:15 INFO mapreduce.Job:  map 64% reduce 0%
18/10/18 08:03:32 INFO mapreduce.Job:  map 65% reduce 0%
18/10/18 08:03:47 INFO mapreduce.Job:  map 66% reduce 0%
18/10/18 08:04:04 INFO mapreduce.Job:  map 67% reduce 0%
18/10/18 08:04:20 INFO mapreduce.Job:  map 68% reduce 0%
18/10/18 08:04:36 INFO mapreduce.Job:  map 69% reduce 0%
18/10/18 08:04:54 INFO mapreduce.Job:  map 70% reduce 0%
18/10/18 08:05:10 INFO mapreduce.Job:  map 71% reduce 0%
18/10/18 08:05:28 INFO mapreduce.Job:  map 72% reduce 0%
18/10/18 08:05:45 INFO mapreduce.Job:  map 73% reduce 0%
18/10/18 08:06:02 INFO mapreduce.Job:  map 74% reduce 0%
18/10/18 08:06:18 INFO mapreduce.Job:  map 75% reduce 0%
18/10/18 08:06:34 INFO mapreduce.Job:  map 76% reduce 0%
18/10/18 08:06:51 INFO mapreduce.Job:  map 77% reduce 0%
18/10/18 08:07:07 INFO mapreduce.Job:  map 78% reduce 0%
18/10/18 08:07:25 INFO mapreduce.Job:  map 79% reduce 0%
18/10/18 08:07:43 INFO mapreduce.Job:  map 80% reduce 0%
18/10/18 08:07:59 INFO mapreduce.Job:  map 81% reduce 0%
18/10/18 08:08:16 INFO mapreduce.Job:  map 82% reduce 0%
18/10/18 08:08:33 INFO mapreduce.Job:  map 83% reduce 0%
18/10/18 08:08:51 INFO mapreduce.Job:  map 84% reduce 0%
18/10/18 08:09:08 INFO mapreduce.Job:  map 85% reduce 0%
18/10/18 08:09:26 INFO mapreduce.Job:  map 86% reduce 0%
18/10/18 08:09:43 INFO mapreduce.Job:  map 87% reduce 0%
18/10/18 08:09:59 INFO mapreduce.Job:  map 88% reduce 0%
18/10/18 08:10:14 INFO mapreduce.Job:  map 89% reduce 0%
18/10/18 08:10:32 INFO mapreduce.Job:  map 90% reduce 0%
18/10/18 08:10:50 INFO mapreduce.Job:  map 91% reduce 0%
18/10/18 08:11:06 INFO mapreduce.Job:  map 92% reduce 0%
18/10/18 08:11:23 INFO mapreduce.Job:  map 93% reduce 0%
18/10/18 08:11:39 INFO mapreduce.Job:  map 94% reduce 0%
18/10/18 08:11:56 INFO mapreduce.Job:  map 95% reduce 0%
18/10/18 08:12:13 INFO mapreduce.Job:  map 96% reduce 0%
18/10/18 08:12:31 INFO mapreduce.Job:  map 97% reduce 0%
18/10/18 08:12:47 INFO mapreduce.Job:  map 98% reduce 0%
18/10/18 08:13:04 INFO mapreduce.Job:  map 99% reduce 0%
18/10/18 08:13:20 INFO mapreduce.Job:  map 100% reduce 0%
18/10/18 08:13:41 INFO mapreduce.Job:  map 100% reduce 6%
18/10/18 08:13:49 INFO mapreduce.Job:  map 100% reduce 8%
18/10/18 08:13:55 INFO mapreduce.Job:  map 100% reduce 10%
18/10/18 08:14:01 INFO mapreduce.Job:  map 100% reduce 17%
18/10/18 08:14:07 INFO mapreduce.Job:  map 100% reduce 19%
18/10/18 08:14:13 INFO mapreduce.Job:  map 100% reduce 21%
18/10/18 08:14:19 INFO mapreduce.Job:  map 100% reduce 23%
18/10/18 08:14:24 INFO mapreduce.Job:  map 100% reduce 25%
18/10/18 08:14:39 INFO mapreduce.Job:  map 100% reduce 27%
18/10/18 08:14:45 INFO mapreduce.Job:  map 100% reduce 28%
18/10/18 08:14:51 INFO mapreduce.Job:  map 100% reduce 29%
18/10/18 08:14:57 INFO mapreduce.Job:  map 100% reduce 31%
18/10/18 08:15:03 INFO mapreduce.Job:  map 100% reduce 33%
18/10/18 08:15:09 INFO mapreduce.Job:  map 100% reduce 40%
18/10/18 08:15:15 INFO mapreduce.Job:  map 100% reduce 43%
18/10/18 08:15:21 INFO mapreduce.Job:  map 100% reduce 45%
18/10/18 08:15:27 INFO mapreduce.Job:  map 100% reduce 47%
18/10/18 08:15:33 INFO mapreduce.Job:  map 100% reduce 49%
18/10/18 08:15:39 INFO mapreduce.Job:  map 100% reduce 50%
18/10/18 08:15:59 INFO mapreduce.Job:  map 100% reduce 52%
18/10/18 08:16:05 INFO mapreduce.Job:  map 100% reduce 53%
18/10/18 08:16:17 INFO mapreduce.Job:  map 100% reduce 56%
18/10/18 08:16:23 INFO mapreduce.Job:  map 100% reduce 57%
18/10/18 08:16:29 INFO mapreduce.Job:  map 100% reduce 58%
18/10/18 08:16:35 INFO mapreduce.Job:  map 100% reduce 66%
18/10/18 08:16:41 INFO mapreduce.Job:  map 100% reduce 68%
18/10/18 08:16:47 INFO mapreduce.Job:  map 100% reduce 70%
18/10/18 08:16:53 INFO mapreduce.Job:  map 100% reduce 72%
18/10/18 08:16:59 INFO mapreduce.Job:  map 100% reduce 74%
18/10/18 08:17:02 INFO mapreduce.Job:  map 100% reduce 75%
18/10/18 08:17:18 INFO mapreduce.Job:  map 100% reduce 78%
18/10/18 08:17:30 INFO mapreduce.Job:  map 100% reduce 81%
18/10/18 08:17:36 INFO mapreduce.Job:  map 100% reduce 82%
18/10/18 08:17:42 INFO mapreduce.Job:  map 100% reduce 83%
18/10/18 08:17:48 INFO mapreduce.Job:  map 100% reduce 92%
18/10/18 08:17:54 INFO mapreduce.Job:  map 100% reduce 94%
18/10/18 08:18:00 INFO mapreduce.Job:  map 100% reduce 96%
18/10/18 08:18:06 INFO mapreduce.Job:  map 100% reduce 98%
18/10/18 08:18:12 INFO mapreduce.Job:  map 100% reduce 100%
18/10/18 08:18:18 INFO mapreduce.Job: Job job_1539847360066_0002 completed successfully
18/10/18 08:18:18 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4437083200
                FILE: Number of bytes written=8827132081
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000039000
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=912
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=4
                Data-local map tasks=298
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=2666588
                Total time spent by all reduces in occupied slots (ms)=574290
                Total time spent by all map tasks (ms)=1333294
                Total time spent by all reduce tasks (ms)=287145
                Total vcore-milliseconds taken by all map tasks=2666588
                Total vcore-milliseconds taken by all reduce tasks=574290
                Total megabyte-milliseconds taken by all map tasks=2730586112
                Total megabyte-milliseconds taken by all reduce tasks=588072960
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342785279
                Input split bytes=39000
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342785279
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1200
                Failed Shuffles=0
                Merged Map outputs=1200
                GC time elapsed (ms)=25830
                CPU time spent (ms)=1366510
                Physical memory (bytes) snapshot=148543905792
                Virtual memory (bytes) snapshot=1120270401536
                Total committed heap usage (bytes)=150973448192
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
18/10/18 08:18:18 INFO terasort.TeraSort: done

real    33m9.516s
user    0m16.389s
sys     0m1.665s
````
