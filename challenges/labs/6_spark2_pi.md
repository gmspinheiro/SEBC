````
[root@sebce1 ~]# spark2-submit --class org.apache.spark.examples.SparkPi --master yarn --deploy-mode cluster /opt/cloudera/parcels/SPARK2/lib/spark2/examples/jars/spark-examples_2.11-2.3.0.cloudera4.jar 10
18/10/19 09:25:36 INFO client.RMProxy: Connecting to ResourceManager at sebce1.madrid.es/10.0.6.4:8032
18/10/19 09:25:37 INFO yarn.Client: Requesting a new application from cluster with 3 NodeManagers
18/10/19 09:25:37 INFO yarn.Client: Verifying our application has not requested more than the maximum memory capability of the cluster (6067 MB per container)
18/10/19 09:25:37 INFO yarn.Client: Will allocate AM container, with 1408 MB memory including 384 MB overhead
18/10/19 09:25:37 INFO yarn.Client: Setting up container launch context for our AM
18/10/19 09:25:37 INFO yarn.Client: Setting up the launch environment for our AM container
18/10/19 09:25:37 INFO yarn.Client: Preparing resources for our AM container
18/10/19 09:25:37 INFO yarn.Client: Uploading resource file:/opt/cloudera/parcels/SPARK2/lib/spark2/examples/jars/spark-examples_2.11-2.3.0.cloudera4.jar -> hdfs://sebce1.madrid.es:8020/user/fullerton/.sparkStaging/application_1539940587927_0003/spark-examples_2.11-2.3.0.cloudera4.jar
18/10/19 09:25:38 INFO yarn.Client: Uploading resource file:/tmp/spark-697e3d3c-af02-41b6-9638-6790be7800d7/__spark_conf__7629070363288528514.zip -> hdfs://sebce1.madrid.es:8020/user/fullerton/.sparkStaging/application_1539940587927_0003/__spark_conf__.zip
18/10/19 09:25:38 INFO spark.SecurityManager: Changing view acls to: root,fullerton
18/10/19 09:25:38 INFO spark.SecurityManager: Changing modify acls to: root,fullerton
18/10/19 09:25:38 INFO spark.SecurityManager: Changing view acls groups to:
18/10/19 09:25:38 INFO spark.SecurityManager: Changing modify acls groups to:
18/10/19 09:25:38 INFO spark.SecurityManager: SecurityManager: authentication disabled; ui acls disabled; users  with view permissions: Set(root, fullerton); groups with view permissions: Set(); users  with modify permissions: Set(root, fullerton); groups with modify permissions: Set()
18/10/19 09:25:38 INFO security.HadoopFSDelegationTokenProvider: getting token for: DFS[DFSClient[clientName=DFSClient_NONMAPREDUCE_-2029944903_1, ugi=fullerton@GMSPINHEIRO.SG (auth:KERBEROS)]]
18/10/19 09:25:38 INFO hdfs.DFSClient: Created token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@GMSPINHEIRO.SG, renewer=yarn, realUser=, issueDate=1539941138369, maxDate=1540545938369, sequenceNumber=5, masterKeyId=2 on 10.0.6.4:8020
18/10/19 09:25:38 INFO security.HadoopFSDelegationTokenProvider: getting token for: DFS[DFSClient[clientName=DFSClient_NONMAPREDUCE_-2029944903_1, ugi=fullerton@GMSPINHEIRO.SG (auth:KERBEROS)]]
18/10/19 09:25:39 INFO hive.metastore: Trying to connect to metastore with URI thrift://sebce1.madrid.es:9083
18/10/19 09:25:39 INFO hive.metastore: Opened a connection to metastore, current connections: 1
18/10/19 09:25:39 INFO hive.metastore: Connected to metastore.
18/10/19 09:25:39 INFO hive.metastore: Closed a connection to metastore, current connections: 0
18/10/19 09:25:40 INFO yarn.Client: Submitting application application_1539940587927_0003 to ResourceManager
18/10/19 09:25:40 INFO impl.YarnClientImpl: Submitted application application_1539940587927_0003
18/10/19 09:25:41 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:41 INFO yarn.Client:
         client token: Token { kind: YARN_CLIENT_TOKEN, service:  }
         diagnostics: N/A
         ApplicationMaster host: N/A
         ApplicationMaster RPC port: -1
         queue: root.users.fullerton
         start time: 1539941140456
         final status: UNDEFINED
         tracking URL: http://sebce1.madrid.es:8088/proxy/application_1539940587927_0003/
         user: fullerton
18/10/19 09:25:42 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:43 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:44 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:45 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:46 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:47 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:48 INFO yarn.Client: Application report for application_1539940587927_0003 (state: ACCEPTED)
18/10/19 09:25:49 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:49 INFO yarn.Client:
         client token: Token { kind: YARN_CLIENT_TOKEN, service:  }
         diagnostics: N/A
         ApplicationMaster host: 10.0.6.8
         ApplicationMaster RPC port: 0
         queue: root.users.fullerton
         start time: 1539941140456
         final status: UNDEFINED
         tracking URL: http://sebce1.madrid.es:8088/proxy/application_1539940587927_0003/
         user: fullerton
18/10/19 09:25:50 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:51 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:52 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:53 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:54 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:55 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:56 INFO yarn.Client: Application report for application_1539940587927_0003 (state: RUNNING)
18/10/19 09:25:57 INFO yarn.Client: Application report for application_1539940587927_0003 (state: FINISHED)
18/10/19 09:25:57 INFO yarn.Client:
         client token: Token { kind: YARN_CLIENT_TOKEN, service:  }
         diagnostics: N/A
         ApplicationMaster host: 10.0.6.8
         ApplicationMaster RPC port: 0
         queue: root.users.fullerton
         start time: 1539941140456
         final status: SUCCEEDED
         tracking URL: http://sebce1.madrid.es:8088/proxy/application_1539940587927_0003/
         user: fullerton
18/10/19 09:25:57 INFO util.ShutdownHookManager: Shutdown hook called
18/10/19 09:25:57 INFO util.ShutdownHookManager: Deleting directory /tmp/spark-697e3d3c-af02-41b6-9638-6790be7800d7
18/10/19 09:25:57 INFO util.ShutdownHookManager: Deleting directory /tmp/spark-be2fa6ee-36f7-4678-a45f-4b99a2446bf0
````
