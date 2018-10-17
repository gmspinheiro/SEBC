## Questions and Answers

* #### What is ubertask optimization?
The ubertask optimization, runs "sufficiently small" jobs sequentially within a single JVM container and can be enabled with the property `mapreduce.job.ubertask.enable`.
"Small" is defined by the maxmaps, maxreduces, and maxbytes settings.

* #### Where in CM is the Kerberos Security Realm value displayed?
Administration > Settings > default_realm property

* #### Which CDH service(s) host a property for enabling Kerberos authentication?
All CDH core services include a property to enable Kerberos Authentication (HBase, HDFS, Hive, Hue, Impala, Zookeeper, Oozie, Spark).

  CM's Cloudera Managment Services also have settings for Kerberos authentication.

* #### How do you upgrade the CM agents?
You can upgrade agents via the Cloudera Manager by selecting the `Re-run Upgrade Wizard` in the `hosts` page. Or after a Cloudera Manager upgrade.

* #### Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName="hue"

* #### Name all the roles that make up the Hive service
Hive Metastore Server, Hiveserver2, Hive Gateway, WebHCat Server (optional).

* #### What steps must be completed before integrating Cloudera Manager with Kerberos?
In order to integrate Cloudera Manager with Kerberos, you need:
  * Install Kerberos KDC in one or more (replicated) hosts (`krb5-server krb5-libs krb5-auth-dialog krb5-workstation` CentOS packages)
  * Download and deploy jce if using AES256 and jdk < 8
  * Install Kerberos client libs on all nodes of the cluster (`krb5-workstation krb5-libs` CentOS packages)
  * Install the `openldap-clients` package in the CM host
  * Setup a realm for the cluster with renewable tickets
  * Add the principal to be used by the Cloudera Manager and setting the appropriate ACL.
  * Enable Kerberos via the wizard
  * Create the HDFS superuser principal
  * Create principals for each end-user
  * (Optional) Enable Kerberos authentication for HTTP web Consoles for Hadoop Roles.
