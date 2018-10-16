# Teragen Command
````
[gmspinheiro@sebct1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000  /user/gmspinheiro/teragen_file
18/10/16 09:28:22 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
18/10/16 09:28:22 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
18/10/16 09:28:23 INFO terasort.TeraGen: Generating 100000000 using 1
18/10/16 09:28:23 INFO mapreduce.JobSubmitter: number of splits:1
18/10/16 09:28:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local786074279_0001
18/10/16 09:28:23 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
18/10/16 09:28:23 INFO mapreduce.Job: Running job: job_local786074279_0001
18/10/16 09:28:23 INFO mapred.LocalJobRunner: OutputCommitter set in config null
18/10/16 09:28:23 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
18/10/16 09:28:23 INFO output.FileOutputCommitter: FileOutputCommitter skip cleanup _temporary folders under output directory:false, ignore cleanup failures: false
18/10/16 09:28:23 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
18/10/16 09:28:23 INFO mapred.LocalJobRunner: Waiting for map tasks
18/10/16 09:28:23 INFO mapred.LocalJobRunner: Starting task: attempt_local786074279_0001_m_000000_0
18/10/16 09:28:23 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
18/10/16 09:28:23 INFO output.FileOutputCommitter: FileOutputCommitter skip cleanup _temporary folders under output directory:false, ignore cleanup failures: false
18/10/16 09:28:23 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
18/10/16 09:28:23 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@2fa54393
18/10/16 09:28:24 INFO mapreduce.Job: Job job_local786074279_0001 running in uber mode : false
18/10/16 09:28:24 INFO mapreduce.Job:  map 0% reduce 0%
18/10/16 09:28:35 INFO mapred.LocalJobRunner: map > map
18/10/16 09:28:36 INFO mapreduce.Job:  map 10% reduce 0%
18/10/16 09:28:41 INFO mapred.LocalJobRunner: map > map
18/10/16 09:28:42 INFO mapreduce.Job:  map 16% reduce 0%
18/10/16 09:28:47 INFO mapred.LocalJobRunner: map > map
18/10/16 09:28:48 INFO mapreduce.Job:  map 21% reduce 0%
18/10/16 09:28:53 INFO mapred.LocalJobRunner: map > map
18/10/16 09:28:54 INFO mapreduce.Job:  map 24% reduce 0%
18/10/16 09:28:59 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:00 INFO mapreduce.Job:  map 29% reduce 0%
18/10/16 09:29:05 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:06 INFO mapreduce.Job:  map 32% reduce 0%
18/10/16 09:29:11 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:12 INFO mapreduce.Job:  map 35% reduce 0%
18/10/16 09:29:17 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:18 INFO mapreduce.Job:  map 39% reduce 0%
18/10/16 09:29:23 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:24 INFO mapreduce.Job:  map 43% reduce 0%
18/10/16 09:29:29 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:30 INFO mapreduce.Job:  map 48% reduce 0%
18/10/16 09:29:35 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:36 INFO mapreduce.Job:  map 52% reduce 0%
18/10/16 09:29:41 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:42 INFO mapreduce.Job:  map 55% reduce 0%
18/10/16 09:29:47 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:48 INFO mapreduce.Job:  map 58% reduce 0%
18/10/16 09:29:53 INFO mapred.LocalJobRunner: map > map
18/10/16 09:29:54 INFO mapreduce.Job:  map 61% reduce 0%
18/10/16 09:29:59 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:00 INFO mapreduce.Job:  map 64% reduce 0%
18/10/16 09:30:05 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:06 INFO mapreduce.Job:  map 65% reduce 0%
18/10/16 09:30:11 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:12 INFO mapreduce.Job:  map 69% reduce 0%
18/10/16 09:30:17 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:18 INFO mapreduce.Job:  map 73% reduce 0%
18/10/16 09:30:23 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:24 INFO mapreduce.Job:  map 76% reduce 0%
18/10/16 09:30:29 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:30 INFO mapreduce.Job:  map 79% reduce 0%
18/10/16 09:30:35 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:36 INFO mapreduce.Job:  map 81% reduce 0%
18/10/16 09:30:41 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:42 INFO mapreduce.Job:  map 82% reduce 0%
18/10/16 09:30:47 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:48 INFO mapreduce.Job:  map 86% reduce 0%
18/10/16 09:30:53 INFO mapred.LocalJobRunner: map > map
18/10/16 09:30:54 INFO mapreduce.Job:  map 91% reduce 0%
18/10/16 09:30:59 INFO mapred.LocalJobRunner: map > map
18/10/16 09:31:00 INFO mapreduce.Job:  map 94% reduce 0%
18/10/16 09:31:05 INFO mapred.LocalJobRunner: map > map
18/10/16 09:31:06 INFO mapreduce.Job:  map 98% reduce 0%
18/10/16 09:31:07 INFO mapred.LocalJobRunner: map > map
18/10/16 09:31:07 INFO mapred.Task: Task:attempt_local786074279_0001_m_000000_0 is done. And is in the process of committing
18/10/16 09:31:07 INFO mapred.LocalJobRunner: map > map
18/10/16 09:31:07 INFO mapred.Task: Task attempt_local786074279_0001_m_000000_0 is allowed to commit now
18/10/16 09:31:07 INFO output.FileOutputCommitter: Saved output of task 'attempt_local786074279_0001_m_000000_0' to hdfs://sebct2.madrid.es:8020/user/gmspinheiro/teragen_file/_temporary/0/task_local786074279_0001_m_000000
18/10/16 09:31:07 INFO mapred.LocalJobRunner: map
18/10/16 09:31:07 INFO mapred.Task: Task 'attempt_local786074279_0001_m_000000_0' done.
18/10/16 09:31:07 INFO mapred.LocalJobRunner: Finishing task: attempt_local786074279_0001_m_000000_0
18/10/16 09:31:07 INFO mapred.LocalJobRunner: map task executor complete.
18/10/16 09:31:08 INFO mapreduce.Job:  map 100% reduce 0%
18/10/16 09:31:08 INFO mapreduce.Job: Job job_local786074279_0001 completed successfully
18/10/16 09:31:08 INFO mapreduce.Job: Counters: 21
        File System Counters
                FILE: Number of bytes read=276519
                FILE: Number of bytes written=626275
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=0
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=4
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=83
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=460
                Total committed heap usage (bytes)=145752064
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    2m48.133s
user    2m9.940s
sys     0m14.989s
````

# Terasort Command

Due to the time taken and the extensive log messages, only the command used and parts of the progress output are shown.

````
[gmspinheiro@sebct1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/gmspinheiro/ter
18/10/16 09:34:48 INFO terasort.TeraSort: starting
18/10/16 09:34:49 INFO input.FileInputFormat: Total input paths to process : 1
Spent 210ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 216ms
Sampling 10 splits of 298
Making 1 from 100000 sampled records
Computing parititions took 739ms
Spent 958ms computing partitions.
18/10/16 09:34:50 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
18/10/16 09:34:50 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
18/10/16 09:34:50 INFO mapreduce.JobSubmitter: number of splits:298
18/10/16 09:34:51 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local1752328624_0001
18/10/16 09:34:51 INFO mapred.LocalDistributedCacheManager: Creating symlink: /tmp/hadoop-gmspinheiro/mapred/local/1539682491298/_partition.lst <
18/10/16 09:34:51 INFO mapred.LocalDistributedCacheManager: Localized hdfs://sebct2.madrid.es:8020/user/gmspinheiro/teragen_sorted/_partition.lstal/1539682491298/_partition.lst
18/10/16 09:34:52 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
18/10/16 09:34:52 INFO mapreduce.Job: Running job: job_local1752328624_0001

(...)

18/10/16 09:53:38 INFO mapreduce.Job: Job job_local1752328624_0001 completed successfully
18/10/16 09:53:38 INFO mapreduce.Job: Counters: 35
        File System Counters
                FILE: Number of bytes read=27435534530
                FILE: Number of bytes written=1582278177541
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1508105727400
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=97176
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=600
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=10400001788
                Input split bytes=40528
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=10400001788
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=261069061
                Shuffled Maps =298
                Failed Shuffles=0
                Merged Map outputs=298
                GC time elapsed (ms)=22514
                Total committed heap usage (bytes)=309950152704
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
18/10/16 09:53:38 INFO terasort.TeraSort: done

real    18m51.774s
user    10m43.378s
sys     1m29.059s
````
