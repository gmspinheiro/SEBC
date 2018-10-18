# Test Results

The total execution time between all the possible combinations did not deviate much from each other. The excel workesheet with the times can be seen in the `labs\yarn_test_results.xlsx` and the original times can be seen in the `labs\YARNTest.sh.nohup.out` file.

### Slowest
The slowest run was with 1 Mapper 1 Reducer and 2048 MB and took 18m40s.

````
#Mapper containers 1
#Reducer containers: 1
#Container memory: 2048

real	2m20.608s
user	0m9.757s
sys	0m0.594s

real	16m20.683s
user	0m14.619s
sys	0m1.231s
Deleted /results/tg-10GB-1-1-2048
Deleted /results/ts-10GB-1-1-2048
````

````
18/10/17 16:42:27 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794547015, maxDate=1540399347015, sequenceNumber=6, masterKeyId=4 on ha-hdfs:sebcgmspinheiro
18/10/17 16:42:27 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794547015, maxDate=1540399347015, sequenceNumber=6, masterKeyId=4)
18/10/17 16:42:27 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/17 16:42:27 INFO terasort.TeraGen: Generating 102400000 using 1
18/10/17 16:42:27 INFO mapreduce.JobSubmitter: number of splits:1
18/10/17 16:42:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539787370805_0005
18/10/17 16:42:27 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794547015, maxDate=1540399347015, sequenceNumber=6, masterKeyId=4)
18/10/17 16:42:28 INFO impl.YarnClientImpl: Submitted application application_1539787370805_0005
18/10/17 16:42:28 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539787370805_0005/
18/10/17 16:42:28 INFO mapreduce.Job: Running job: job_1539787370805_0005
18/10/17 16:42:36 INFO mapreduce.Job: Job job_1539787370805_0005 running in uber mode : false
18/10/17 16:42:36 INFO mapreduce.Job:  map 0% reduce 0%
18/10/17 16:42:55 INFO mapreduce.Job:  map 10% reduce 0%
18/10/17 16:43:01 INFO mapreduce.Job:  map 15% reduce 0%
18/10/17 16:43:07 INFO mapreduce.Job:  map 21% reduce 0%
18/10/17 16:43:13 INFO mapreduce.Job:  map 26% reduce 0%
18/10/17 16:43:19 INFO mapreduce.Job:  map 31% reduce 0%
18/10/17 16:43:25 INFO mapreduce.Job:  map 36% reduce 0%
18/10/17 16:43:32 INFO mapreduce.Job:  map 41% reduce 0%
18/10/17 16:43:38 INFO mapreduce.Job:  map 47% reduce 0%
18/10/17 16:43:44 INFO mapreduce.Job:  map 52% reduce 0%
18/10/17 16:43:50 INFO mapreduce.Job:  map 58% reduce 0%
18/10/17 16:43:56 INFO mapreduce.Job:  map 63% reduce 0%
18/10/17 16:44:02 INFO mapreduce.Job:  map 68% reduce 0%
18/10/17 16:44:08 INFO mapreduce.Job:  map 72% reduce 0%
18/10/17 16:44:14 INFO mapreduce.Job:  map 75% reduce 0%
18/10/17 16:44:20 INFO mapreduce.Job:  map 79% reduce 0%
18/10/17 16:44:26 INFO mapreduce.Job:  map 85% reduce 0%
18/10/17 16:44:32 INFO mapreduce.Job:  map 90% reduce 0%
18/10/17 16:44:38 INFO mapreduce.Job:  map 95% reduce 0%
18/10/17 16:44:44 INFO mapreduce.Job:  map 100% reduce 0%
18/10/17 16:44:44 INFO mapreduce.Job: Job job_1539787370805_0005 completed successfully
18/10/17 16:44:44 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=154010
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=83
		HDFS: Number of bytes written=10240000000
		HDFS: Number of read operations=4
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=2
	Job Counters
		Launched map tasks=1
		Other local map tasks=1
		Total time spent by all maps in occupied slots (ms)=249906
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=124953
		Total vcore-milliseconds taken by all map tasks=249906
		Total megabyte-milliseconds taken by all map tasks=255903744
	Map-Reduce Framework
		Map input records=102400000
		Map output records=102400000
		Input split bytes=83
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=420
		CPU time spent (ms)=146320
		Physical memory (bytes) snapshot=564158464
		Virtual memory (bytes) snapshot=3697725440
		Total committed heap usage (bytes)=156237824
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=219910918972852281
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=10240000000
18/10/17 16:44:45 INFO terasort.TeraSort: starting
18/10/17 16:44:47 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794687440, maxDate=1540399487440, sequenceNumber=7, masterKeyId=4 on ha-hdfs:sebcgmspinheiro
18/10/17 16:44:47 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794687440, maxDate=1540399487440, sequenceNumber=7, masterKeyId=4)
18/10/17 16:44:47 INFO input.FileInputFormat: Total input paths to process : 1
18/10/17 16:44:48 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/17 16:44:48 INFO mapreduce.JobSubmitter: number of splits:77
18/10/17 16:44:49 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539787370805_0006
18/10/17 16:44:49 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539794687440, maxDate=1540399487440, sequenceNumber=7, masterKeyId=4)
18/10/17 16:44:49 INFO impl.YarnClientImpl: Submitted application application_1539787370805_0006
18/10/17 16:44:49 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539787370805_0006/
18/10/17 16:44:49 INFO mapreduce.Job: Running job: job_1539787370805_0006
18/10/17 16:44:58 INFO mapreduce.Job: Job job_1539787370805_0006 running in uber mode : false
18/10/17 16:44:58 INFO mapreduce.Job:  map 0% reduce 0%
18/10/17 16:45:10 INFO mapreduce.Job:  map 1% reduce 0%
18/10/17 16:45:20 INFO mapreduce.Job:  map 3% reduce 0%
18/10/17 16:45:30 INFO mapreduce.Job:  map 4% reduce 0%
18/10/17 16:45:38 INFO mapreduce.Job:  map 5% reduce 0%
18/10/17 16:45:47 INFO mapreduce.Job:  map 6% reduce 0%
18/10/17 16:45:56 INFO mapreduce.Job:  map 8% reduce 0%
18/10/17 16:46:05 INFO mapreduce.Job:  map 9% reduce 0%
18/10/17 16:46:14 INFO mapreduce.Job:  map 10% reduce 0%
18/10/17 16:46:23 INFO mapreduce.Job:  map 12% reduce 0%
18/10/17 16:46:32 INFO mapreduce.Job:  map 13% reduce 0%
18/10/17 16:46:41 INFO mapreduce.Job:  map 14% reduce 0%
18/10/17 16:46:50 INFO mapreduce.Job:  map 16% reduce 0%
18/10/17 16:46:59 INFO mapreduce.Job:  map 17% reduce 0%
18/10/17 16:47:08 INFO mapreduce.Job:  map 18% reduce 0%
18/10/17 16:47:17 INFO mapreduce.Job:  map 19% reduce 0%
18/10/17 16:47:26 INFO mapreduce.Job:  map 21% reduce 0%
18/10/17 16:47:35 INFO mapreduce.Job:  map 22% reduce 0%
18/10/17 16:47:44 INFO mapreduce.Job:  map 23% reduce 0%
18/10/17 16:47:53 INFO mapreduce.Job:  map 25% reduce 0%
18/10/17 16:48:02 INFO mapreduce.Job:  map 26% reduce 0%
18/10/17 16:48:11 INFO mapreduce.Job:  map 27% reduce 0%
18/10/17 16:48:20 INFO mapreduce.Job:  map 29% reduce 0%
18/10/17 16:48:29 INFO mapreduce.Job:  map 30% reduce 0%
18/10/17 16:48:38 INFO mapreduce.Job:  map 31% reduce 0%
18/10/17 16:48:47 INFO mapreduce.Job:  map 32% reduce 0%
18/10/17 16:48:56 INFO mapreduce.Job:  map 34% reduce 0%
18/10/17 16:49:05 INFO mapreduce.Job:  map 35% reduce 0%
18/10/17 16:49:15 INFO mapreduce.Job:  map 36% reduce 0%
18/10/17 16:49:24 INFO mapreduce.Job:  map 38% reduce 0%
18/10/17 16:49:33 INFO mapreduce.Job:  map 39% reduce 0%
18/10/17 16:49:42 INFO mapreduce.Job:  map 40% reduce 0%
18/10/17 16:49:51 INFO mapreduce.Job:  map 42% reduce 0%
18/10/17 16:50:00 INFO mapreduce.Job:  map 43% reduce 0%
18/10/17 16:50:09 INFO mapreduce.Job:  map 44% reduce 0%
18/10/17 16:50:18 INFO mapreduce.Job:  map 45% reduce 0%
18/10/17 16:50:27 INFO mapreduce.Job:  map 47% reduce 0%
18/10/17 16:50:36 INFO mapreduce.Job:  map 48% reduce 0%
18/10/17 16:50:45 INFO mapreduce.Job:  map 49% reduce 0%
18/10/17 16:50:54 INFO mapreduce.Job:  map 51% reduce 0%
18/10/17 16:51:03 INFO mapreduce.Job:  map 52% reduce 0%
18/10/17 16:51:12 INFO mapreduce.Job:  map 53% reduce 0%
18/10/17 16:51:21 INFO mapreduce.Job:  map 55% reduce 0%
18/10/17 16:51:30 INFO mapreduce.Job:  map 56% reduce 0%
18/10/17 16:51:38 INFO mapreduce.Job:  map 57% reduce 0%
18/10/17 16:51:48 INFO mapreduce.Job:  map 58% reduce 0%
18/10/17 16:51:57 INFO mapreduce.Job:  map 60% reduce 0%
18/10/17 16:52:05 INFO mapreduce.Job:  map 61% reduce 0%
18/10/17 16:52:15 INFO mapreduce.Job:  map 62% reduce 0%
18/10/17 16:52:24 INFO mapreduce.Job:  map 64% reduce 0%
18/10/17 16:52:33 INFO mapreduce.Job:  map 65% reduce 0%
18/10/17 16:52:42 INFO mapreduce.Job:  map 66% reduce 0%
18/10/17 16:52:51 INFO mapreduce.Job:  map 68% reduce 0%
18/10/17 16:53:00 INFO mapreduce.Job:  map 69% reduce 0%
18/10/17 16:53:08 INFO mapreduce.Job:  map 70% reduce 0%
18/10/17 16:53:17 INFO mapreduce.Job:  map 71% reduce 0%
18/10/17 16:53:27 INFO mapreduce.Job:  map 73% reduce 0%
18/10/17 16:53:35 INFO mapreduce.Job:  map 74% reduce 0%
18/10/17 16:53:45 INFO mapreduce.Job:  map 75% reduce 0%
18/10/17 16:53:53 INFO mapreduce.Job:  map 77% reduce 0%
18/10/17 16:54:02 INFO mapreduce.Job:  map 78% reduce 0%
18/10/17 16:54:11 INFO mapreduce.Job:  map 79% reduce 0%
18/10/17 16:54:20 INFO mapreduce.Job:  map 81% reduce 0%
18/10/17 16:54:29 INFO mapreduce.Job:  map 82% reduce 0%
18/10/17 16:54:40 INFO mapreduce.Job:  map 83% reduce 0%
18/10/17 16:54:48 INFO mapreduce.Job:  map 84% reduce 0%
18/10/17 16:54:57 INFO mapreduce.Job:  map 86% reduce 0%
18/10/17 16:55:06 INFO mapreduce.Job:  map 87% reduce 0%
18/10/17 16:55:15 INFO mapreduce.Job:  map 88% reduce 0%
18/10/17 16:55:24 INFO mapreduce.Job:  map 90% reduce 0%
18/10/17 16:55:33 INFO mapreduce.Job:  map 91% reduce 0%
18/10/17 16:55:46 INFO mapreduce.Job:  map 92% reduce 0%
18/10/17 16:55:58 INFO mapreduce.Job:  map 94% reduce 0%
18/10/17 16:56:10 INFO mapreduce.Job:  map 95% reduce 0%
18/10/17 16:56:22 INFO mapreduce.Job:  map 96% reduce 0%
18/10/17 16:56:28 INFO mapreduce.Job:  map 97% reduce 0%
18/10/17 16:56:40 INFO mapreduce.Job:  map 99% reduce 0%
18/10/17 16:56:51 INFO mapreduce.Job:  map 100% reduce 0%
18/10/17 16:57:07 INFO mapreduce.Job:  map 100% reduce 6%
18/10/17 16:57:13 INFO mapreduce.Job:  map 100% reduce 9%
18/10/17 16:57:19 INFO mapreduce.Job:  map 100% reduce 11%
18/10/17 16:57:25 INFO mapreduce.Job:  map 100% reduce 14%
18/10/17 16:57:31 INFO mapreduce.Job:  map 100% reduce 16%
18/10/17 16:57:37 INFO mapreduce.Job:  map 100% reduce 19%
18/10/17 16:57:43 INFO mapreduce.Job:  map 100% reduce 22%
18/10/17 16:57:49 INFO mapreduce.Job:  map 100% reduce 24%
18/10/17 16:57:55 INFO mapreduce.Job:  map 100% reduce 27%
18/10/17 16:58:01 INFO mapreduce.Job:  map 100% reduce 29%
18/10/17 16:58:07 INFO mapreduce.Job:  map 100% reduce 32%
18/10/17 16:58:13 INFO mapreduce.Job:  map 100% reduce 47%
18/10/17 16:58:19 INFO mapreduce.Job:  map 100% reduce 68%
18/10/17 16:58:25 INFO mapreduce.Job:  map 100% reduce 69%
18/10/17 16:58:31 INFO mapreduce.Job:  map 100% reduce 71%
18/10/17 16:58:37 INFO mapreduce.Job:  map 100% reduce 73%
18/10/17 16:58:43 INFO mapreduce.Job:  map 100% reduce 74%
18/10/17 16:58:49 INFO mapreduce.Job:  map 100% reduce 76%
18/10/17 16:58:55 INFO mapreduce.Job:  map 100% reduce 78%
18/10/17 16:59:01 INFO mapreduce.Job:  map 100% reduce 79%
18/10/17 16:59:07 INFO mapreduce.Job:  map 100% reduce 81%
18/10/17 16:59:13 INFO mapreduce.Job:  map 100% reduce 83%
18/10/17 16:59:19 INFO mapreduce.Job:  map 100% reduce 84%
18/10/17 16:59:25 INFO mapreduce.Job:  map 100% reduce 86%
18/10/17 16:59:31 INFO mapreduce.Job:  map 100% reduce 88%
18/10/17 16:59:43 INFO mapreduce.Job:  map 100% reduce 89%
18/10/17 16:59:49 INFO mapreduce.Job:  map 100% reduce 90%
18/10/17 17:00:01 INFO mapreduce.Job:  map 100% reduce 91%
18/10/17 17:00:13 INFO mapreduce.Job:  map 100% reduce 92%
18/10/17 17:00:19 INFO mapreduce.Job:  map 100% reduce 94%
18/10/17 17:00:25 INFO mapreduce.Job:  map 100% reduce 95%
18/10/17 17:00:37 INFO mapreduce.Job:  map 100% reduce 96%
18/10/17 17:00:43 INFO mapreduce.Job:  map 100% reduce 97%
18/10/17 17:00:50 INFO mapreduce.Job:  map 100% reduce 98%
18/10/17 17:00:56 INFO mapreduce.Job:  map 100% reduce 99%
18/10/17 17:01:02 INFO mapreduce.Job:  map 100% reduce 100%
18/10/17 17:01:05 INFO mapreduce.Job: Job job_1539787370805_0006 completed successfully
18/10/17 17:01:05 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=4570677273
		FILE: Number of bytes written=9058445393
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10240009625
		HDFS: Number of bytes written=10240000000
		HDFS: Number of read operations=234
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=2
	Job Counters
		Launched map tasks=77
		Launched reduce tasks=1
		Data-local map tasks=75
		Rack-local map tasks=2
		Total time spent by all maps in occupied slots (ms)=1269256
		Total time spent by all reduces in occupied slots (ms)=502932
		Total time spent by all map tasks (ms)=634628
		Total time spent by all reduce tasks (ms)=251466
		Total vcore-milliseconds taken by all map tasks=1269256
		Total vcore-milliseconds taken by all reduce tasks=502932
		Total megabyte-milliseconds taken by all map tasks=1299718144
		Total megabyte-milliseconds taken by all reduce tasks=515002368
	Map-Reduce Framework
		Map input records=102400000
		Map output records=102400000
		Map output bytes=10444800000
		Map output materialized bytes=4475619530
		Input split bytes=9625
		Combine input records=0
		Combine output records=0
		Reduce input groups=102400000
		Reduce shuffle bytes=4475619530
		Reduce input records=102400000
		Reduce output records=102400000
		Spilled Records=204800000
		Shuffled Maps =77
		Failed Shuffles=0
		Merged Map outputs=77
		GC time elapsed (ms)=9477
		CPU time spent (ms)=785190
		Physical memory (bytes) snapshot=40892686336
		Virtual memory (bytes) snapshot=287365414912
		Total committed heap usage (bytes)=43097522176
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=10240000000
	File Output Format Counters
		Bytes Written=10240000000
18/10/17 17:01:05 INFO terasort.TeraSort: done

````

### Fastest
The fastest run was with 1 Mapper 4 Reducer and 1024 MB and took 16m58s.

````
#Mapper containers 1
#Reducer containers: 4
#Container memory: 1024

real	2m15.367s
user	0m9.862s
sys	0m0.580s

real	14m43.330s
user	0m14.375s
sys	0m1.141s
Deleted /results/tg-10GB-1-4-1024
Deleted /results/ts-10GB-1-4-1024
````

````
18/10/17 18:14:36 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800076581, maxDate=1540404876581, sequenceNumber=16, masterKeyId=4 on ha-hdfs:sebcgmspinheiro
18/10/17 18:14:36 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800076581, maxDate=1540404876581, sequenceNumber=16, masterKeyId=4)
18/10/17 18:14:36 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/17 18:14:37 INFO terasort.TeraGen: Generating 102400000 using 1
18/10/17 18:14:37 INFO mapreduce.JobSubmitter: number of splits:1
18/10/17 18:14:37 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539787370805_0015
18/10/17 18:14:37 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800076581, maxDate=1540404876581, sequenceNumber=16, masterKeyId=4)
18/10/17 18:14:37 INFO impl.YarnClientImpl: Submitted application application_1539787370805_0015
18/10/17 18:14:37 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539787370805_0015/
18/10/17 18:14:37 INFO mapreduce.Job: Running job: job_1539787370805_0015
18/10/17 18:14:47 INFO mapreduce.Job: Job job_1539787370805_0015 running in uber mode : false
18/10/17 18:14:47 INFO mapreduce.Job:  map 0% reduce 0%
18/10/17 18:15:06 INFO mapreduce.Job:  map 10% reduce 0%
18/10/17 18:15:12 INFO mapreduce.Job:  map 16% reduce 0%
18/10/17 18:15:18 INFO mapreduce.Job:  map 21% reduce 0%
18/10/17 18:15:24 INFO mapreduce.Job:  map 26% reduce 0%
18/10/17 18:15:30 INFO mapreduce.Job:  map 32% reduce 0%
18/10/17 18:15:36 INFO mapreduce.Job:  map 37% reduce 0%
18/10/17 18:15:42 INFO mapreduce.Job:  map 42% reduce 0%
18/10/17 18:15:48 INFO mapreduce.Job:  map 48% reduce 0%
18/10/17 18:15:54 INFO mapreduce.Job:  map 53% reduce 0%
18/10/17 18:16:00 INFO mapreduce.Job:  map 58% reduce 0%
18/10/17 18:16:06 INFO mapreduce.Job:  map 64% reduce 0%
18/10/17 18:16:12 INFO mapreduce.Job:  map 69% reduce 0%
18/10/17 18:16:18 INFO mapreduce.Job:  map 74% reduce 0%
18/10/17 18:16:24 INFO mapreduce.Job:  map 80% reduce 0%
18/10/17 18:16:30 INFO mapreduce.Job:  map 85% reduce 0%
18/10/17 18:16:36 INFO mapreduce.Job:  map 90% reduce 0%
18/10/17 18:16:42 INFO mapreduce.Job:  map 95% reduce 0%
18/10/17 18:16:47 INFO mapreduce.Job:  map 100% reduce 0%
18/10/17 18:16:48 INFO mapreduce.Job: Job job_1539787370805_0015 completed successfully
18/10/17 18:16:48 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=154009
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=83
		HDFS: Number of bytes written=10240000000
		HDFS: Number of read operations=4
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=2
	Job Counters
		Launched map tasks=1
		Other local map tasks=1
		Total time spent by all maps in occupied slots (ms)=118627
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=118627
		Total vcore-milliseconds taken by all map tasks=237254
		Total megabyte-milliseconds taken by all map tasks=121474048
	Map-Reduce Framework
		Map input records=102400000
		Map output records=102400000
		Input split bytes=83
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=528
		CPU time spent (ms)=144250
		Physical memory (bytes) snapshot=352571392
		Virtual memory (bytes) snapshot=2795216896
		Total committed heap usage (bytes)=150994944
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=219910918972852281
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=10240000000
18/10/17 18:16:50 INFO terasort.TeraSort: starting
18/10/17 18:16:51 INFO hdfs.DFSClient: Created token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800211677, maxDate=1540405011677, sequenceNumber=17, masterKeyId=4 on ha-hdfs:sebcgmspinheiro
18/10/17 18:16:51 INFO security.TokenCache: Got dt for hdfs://sebcgmspinheiro; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800211677, maxDate=1540405011677, sequenceNumber=17, masterKeyId=4)
18/10/17 18:16:51 INFO input.FileInputFormat: Total input paths to process : 1
18/10/17 18:16:52 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm58
18/10/17 18:16:53 INFO mapreduce.JobSubmitter: number of splits:77
18/10/17 18:16:53 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539787370805_0016
18/10/17 18:16:53 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:sebcgmspinheiro, Ident: (token for gmspinheiro: HDFS_DELEGATION_TOKEN owner=gmspinheiro@SEBC.MADRID.ES, renewer=yarn, realUser=, issueDate=1539800211677, maxDate=1540405011677, sequenceNumber=17, masterKeyId=4)
18/10/17 18:16:53 INFO impl.YarnClientImpl: Submitted application application_1539787370805_0016
18/10/17 18:16:53 INFO mapreduce.Job: The url to track the job: http://sebct3.madrid.es:8088/proxy/application_1539787370805_0016/
18/10/17 18:16:53 INFO mapreduce.Job: Running job: job_1539787370805_0016
18/10/17 18:17:03 INFO mapreduce.Job: Job job_1539787370805_0016 running in uber mode : false
18/10/17 18:17:03 INFO mapreduce.Job:  map 0% reduce 0%
18/10/17 18:17:16 INFO mapreduce.Job:  map 1% reduce 0%
18/10/17 18:17:24 INFO mapreduce.Job:  map 3% reduce 0%
18/10/17 18:17:32 INFO mapreduce.Job:  map 4% reduce 0%
18/10/17 18:17:40 INFO mapreduce.Job:  map 5% reduce 0%
18/10/17 18:17:48 INFO mapreduce.Job:  map 6% reduce 0%
18/10/17 18:17:56 INFO mapreduce.Job:  map 8% reduce 0%
18/10/17 18:18:04 INFO mapreduce.Job:  map 9% reduce 0%
18/10/17 18:18:12 INFO mapreduce.Job:  map 10% reduce 0%
18/10/17 18:18:21 INFO mapreduce.Job:  map 12% reduce 0%
18/10/17 18:18:29 INFO mapreduce.Job:  map 13% reduce 0%
18/10/17 18:18:37 INFO mapreduce.Job:  map 14% reduce 0%
18/10/17 18:18:45 INFO mapreduce.Job:  map 16% reduce 0%
18/10/17 18:18:53 INFO mapreduce.Job:  map 17% reduce 0%
18/10/17 18:19:01 INFO mapreduce.Job:  map 18% reduce 0%
18/10/17 18:19:09 INFO mapreduce.Job:  map 19% reduce 0%
18/10/17 18:19:17 INFO mapreduce.Job:  map 21% reduce 0%
18/10/17 18:19:25 INFO mapreduce.Job:  map 22% reduce 0%
18/10/17 18:19:33 INFO mapreduce.Job:  map 23% reduce 0%
18/10/17 18:19:41 INFO mapreduce.Job:  map 25% reduce 0%
18/10/17 18:19:49 INFO mapreduce.Job:  map 26% reduce 0%
18/10/17 18:19:57 INFO mapreduce.Job:  map 27% reduce 0%
18/10/17 18:20:04 INFO mapreduce.Job:  map 29% reduce 0%
18/10/17 18:20:14 INFO mapreduce.Job:  map 30% reduce 0%
18/10/17 18:20:22 INFO mapreduce.Job:  map 31% reduce 0%
18/10/17 18:20:30 INFO mapreduce.Job:  map 32% reduce 0%
18/10/17 18:20:37 INFO mapreduce.Job:  map 34% reduce 0%
18/10/17 18:20:45 INFO mapreduce.Job:  map 35% reduce 0%
18/10/17 18:20:53 INFO mapreduce.Job:  map 36% reduce 0%
18/10/17 18:21:02 INFO mapreduce.Job:  map 38% reduce 0%
18/10/17 18:21:09 INFO mapreduce.Job:  map 39% reduce 0%
18/10/17 18:21:17 INFO mapreduce.Job:  map 40% reduce 0%
18/10/17 18:21:26 INFO mapreduce.Job:  map 42% reduce 0%
18/10/17 18:21:33 INFO mapreduce.Job:  map 43% reduce 0%
18/10/17 18:21:41 INFO mapreduce.Job:  map 44% reduce 0%
18/10/17 18:21:49 INFO mapreduce.Job:  map 45% reduce 0%
18/10/17 18:21:58 INFO mapreduce.Job:  map 47% reduce 0%
18/10/17 18:22:05 INFO mapreduce.Job:  map 48% reduce 0%
18/10/17 18:22:13 INFO mapreduce.Job:  map 49% reduce 0%
18/10/17 18:22:21 INFO mapreduce.Job:  map 51% reduce 0%
18/10/17 18:22:29 INFO mapreduce.Job:  map 52% reduce 0%
18/10/17 18:22:37 INFO mapreduce.Job:  map 53% reduce 0%
18/10/17 18:22:45 INFO mapreduce.Job:  map 55% reduce 0%
18/10/17 18:22:53 INFO mapreduce.Job:  map 56% reduce 0%
18/10/17 18:23:01 INFO mapreduce.Job:  map 57% reduce 0%
18/10/17 18:23:09 INFO mapreduce.Job:  map 58% reduce 0%
18/10/17 18:23:17 INFO mapreduce.Job:  map 60% reduce 0%
18/10/17 18:23:25 INFO mapreduce.Job:  map 61% reduce 0%
18/10/17 18:23:33 INFO mapreduce.Job:  map 62% reduce 0%
18/10/17 18:23:41 INFO mapreduce.Job:  map 64% reduce 0%
18/10/17 18:23:49 INFO mapreduce.Job:  map 65% reduce 0%
18/10/17 18:23:57 INFO mapreduce.Job:  map 66% reduce 0%
18/10/17 18:24:05 INFO mapreduce.Job:  map 68% reduce 0%
18/10/17 18:24:13 INFO mapreduce.Job:  map 69% reduce 0%
18/10/17 18:24:21 INFO mapreduce.Job:  map 70% reduce 0%
18/10/17 18:24:29 INFO mapreduce.Job:  map 71% reduce 0%
18/10/17 18:24:37 INFO mapreduce.Job:  map 73% reduce 0%
18/10/17 18:24:45 INFO mapreduce.Job:  map 74% reduce 0%
18/10/17 18:24:53 INFO mapreduce.Job:  map 75% reduce 0%
18/10/17 18:25:01 INFO mapreduce.Job:  map 77% reduce 0%
18/10/17 18:25:09 INFO mapreduce.Job:  map 78% reduce 0%
18/10/17 18:25:17 INFO mapreduce.Job:  map 79% reduce 0%
18/10/17 18:25:26 INFO mapreduce.Job:  map 81% reduce 0%
18/10/17 18:25:34 INFO mapreduce.Job:  map 82% reduce 0%
18/10/17 18:25:42 INFO mapreduce.Job:  map 83% reduce 0%
18/10/17 18:25:50 INFO mapreduce.Job:  map 84% reduce 0%
18/10/17 18:25:58 INFO mapreduce.Job:  map 86% reduce 0%
18/10/17 18:26:06 INFO mapreduce.Job:  map 87% reduce 0%
18/10/17 18:26:14 INFO mapreduce.Job:  map 88% reduce 0%
18/10/17 18:26:23 INFO mapreduce.Job:  map 90% reduce 0%
18/10/17 18:26:31 INFO mapreduce.Job:  map 91% reduce 0%
18/10/17 18:26:39 INFO mapreduce.Job:  map 92% reduce 0%
18/10/17 18:26:47 INFO mapreduce.Job:  map 94% reduce 0%
18/10/17 18:26:55 INFO mapreduce.Job:  map 95% reduce 0%
18/10/17 18:27:03 INFO mapreduce.Job:  map 96% reduce 0%
18/10/17 18:27:09 INFO mapreduce.Job:  map 97% reduce 0%
18/10/17 18:27:20 INFO mapreduce.Job:  map 99% reduce 0%
18/10/17 18:27:31 INFO mapreduce.Job:  map 100% reduce 0%
18/10/17 18:27:46 INFO mapreduce.Job:  map 100% reduce 5%
18/10/17 18:27:52 INFO mapreduce.Job:  map 100% reduce 8%
18/10/17 18:27:58 INFO mapreduce.Job:  map 100% reduce 18%
18/10/17 18:28:04 INFO mapreduce.Job:  map 100% reduce 20%
18/10/17 18:28:10 INFO mapreduce.Job:  map 100% reduce 21%
18/10/17 18:28:16 INFO mapreduce.Job:  map 100% reduce 23%
18/10/17 18:28:22 INFO mapreduce.Job:  map 100% reduce 25%
18/10/17 18:28:38 INFO mapreduce.Job:  map 100% reduce 27%
18/10/17 18:28:44 INFO mapreduce.Job:  map 100% reduce 28%
18/10/17 18:28:50 INFO mapreduce.Job:  map 100% reduce 30%
18/10/17 18:28:56 INFO mapreduce.Job:  map 100% reduce 33%
18/10/17 18:29:02 INFO mapreduce.Job:  map 100% reduce 43%
18/10/17 18:29:08 INFO mapreduce.Job:  map 100% reduce 45%
18/10/17 18:29:14 INFO mapreduce.Job:  map 100% reduce 47%
18/10/17 18:29:20 INFO mapreduce.Job:  map 100% reduce 48%
18/10/17 18:29:26 INFO mapreduce.Job:  map 100% reduce 50%
18/10/17 18:29:43 INFO mapreduce.Job:  map 100% reduce 52%
18/10/17 18:29:49 INFO mapreduce.Job:  map 100% reduce 53%
18/10/17 18:29:55 INFO mapreduce.Job:  map 100% reduce 55%
18/10/17 18:30:01 INFO mapreduce.Job:  map 100% reduce 58%
18/10/17 18:30:07 INFO mapreduce.Job:  map 100% reduce 67%
18/10/17 18:30:13 INFO mapreduce.Job:  map 100% reduce 69%
18/10/17 18:30:19 INFO mapreduce.Job:  map 100% reduce 71%
18/10/17 18:30:25 INFO mapreduce.Job:  map 100% reduce 73%
18/10/17 18:30:31 INFO mapreduce.Job:  map 100% reduce 75%
18/10/17 18:30:48 INFO mapreduce.Job:  map 100% reduce 78%
18/10/17 18:30:54 INFO mapreduce.Job:  map 100% reduce 80%
18/10/17 18:31:00 INFO mapreduce.Job:  map 100% reduce 83%
18/10/17 18:31:06 INFO mapreduce.Job:  map 100% reduce 92%
18/10/17 18:31:12 INFO mapreduce.Job:  map 100% reduce 94%
18/10/17 18:31:18 INFO mapreduce.Job:  map 100% reduce 96%
18/10/17 18:31:25 INFO mapreduce.Job:  map 100% reduce 98%
18/10/17 18:31:31 INFO mapreduce.Job:  map 100% reduce 100%
18/10/17 18:31:32 INFO mapreduce.Job: Job job_1539787370805_0016 completed successfully
18/10/17 18:31:32 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=4557627622
		FILE: Number of bytes written=9045862313
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10240009625
		HDFS: Number of bytes written=10240000000
		HDFS: Number of read operations=243
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters
		Launched map tasks=77
		Launched reduce tasks=4
		Data-local map tasks=75
		Rack-local map tasks=2
		Total time spent by all maps in occupied slots (ms)=558085
		Total time spent by all reduces in occupied slots (ms)=236604
		Total time spent by all map tasks (ms)=558085
		Total time spent by all reduce tasks (ms)=236604
		Total vcore-milliseconds taken by all map tasks=1116170
		Total vcore-milliseconds taken by all reduce tasks=473208
		Total megabyte-milliseconds taken by all map tasks=571479040
		Total megabyte-milliseconds taken by all reduce tasks=242282496
	Map-Reduce Framework
		Map input records=102400000
		Map output records=102400000
		Map output bytes=10444800000
		Map output materialized bytes=4475616091
		Input split bytes=9625
		Combine input records=0
		Combine output records=0
		Reduce input groups=102400000
		Reduce shuffle bytes=4475616091
		Reduce input records=102400000
		Reduce output records=102400000
		Spilled Records=204800000
		Shuffled Maps =308
		Failed Shuffles=0
		Merged Map outputs=308
		GC time elapsed (ms)=9714
		CPU time spent (ms)=753790
		Physical memory (bytes) snapshot=43650605056
		Virtual memory (bytes) snapshot=226401243136
		Total committed heap usage (bytes)=45316308992
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=10240000000
	File Output Format Counters
		Bytes Written=10240000000
18/10/17 18:31:32 INFO terasort.TeraSort: done

````
