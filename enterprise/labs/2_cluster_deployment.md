# Curl command
Output:
````
[sebc@sebct1 ~]$ curl -u gmspinheiro:cloudera http://localhost:7180/api/v2/cm/deployment
{
  "timestamp" : "2018-10-16T14:06:13.267Z",
  "clusters" : [ {
    "name" : "gmspinheiro",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "dataDir",
            "value" : "/data/01/zookeeper"
          }, {
            "name" : "dataLogDir",
            "value" : "/data/01/zookeeper"
          }, {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "1072693248"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3gpi58d7ni9m8rfgqyf47qddl"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "by7xkwit85kqkreyn2j5h20nj"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "611gkfybvxy4z2gn77mfn5tht"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "sebct1.madrid.es"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "1072693248"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "39gj6ac6ikekonxv0pmkzt2xa"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "sebct1.madrid.es"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-a9f6f82a22eced69d734d4bdad6d8dd3"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "safjcw7wu6t5hddrxic9lju8"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "8ec3d5f4-5c93-4790-a242-6b084f61a534"
          }, {
            "name" : "role_jceks_password",
            "value" : "1cuj3mhwrdp9ryd9o3haum1hq"
          }, {
            "name" : "secret_key",
            "value" : "zDZHS3UAougrhnAdMtflDp5La54HbF"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "1072693248"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data/01/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5314628403"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/data/01/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/data/01/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2147483648"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data/01/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2147483648"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "x6GdDPGfRijJlzPI6K2fePXqvnR6cm"
        }, {
          "name" : "dfs_replication",
          "value" : "2"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "4tjGSbliTwHqOFQv87t3yllKqYU2YA"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "Yz9i2S0mdDNT36fVulox97Dlpb2xN5"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "service_config_suppression_datanode_count_validator",
          "value" : "true"
        }, {
          "name" : "service_health_suppression_hdfs_under_replicated_blocks",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-482236f4e21ed514c20a0559f367fe3e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "20d39833-56ef-4119-9df4-79f09eff5adc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dukkq4pp4lqj4lcc7qyjbe3e6"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-4837166b7cb5dbed40c46d39ddfe5371",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "7d0fac92-df2b-489e-b900-9f97ac3841a6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dbf0zxdi7q8nt0higqtxdj78h"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5osm2qe2qlww21b4dhr0gbb6a"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "920p4b997x0t5ge1zu6stxt7n"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c8trhgwgor7yidg3ylclbvrs6"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "div8vumf0wufz13kzir8pg6bl"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "49erb9yn9pvcty5oew9v0ivfr"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bjxg3cyttxoyhdumycqfsa0wk"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebcgmspinheiro"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebcgmspinheiro"
          }, {
            "name" : "namenode_id",
            "value" : "40"
          }, {
            "name" : "role_jceks_password",
            "value" : "7fjd9mbainhiwzh014mw529b9"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebcgmspinheiro"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebcgmspinheiro"
          }, {
            "name" : "namenode_id",
            "value" : "51"
          }, {
            "name" : "role_jceks_password",
            "value" : "4r4z0psr3o2xde9rx8jtz7vve"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "4"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/data/01/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/data/01/yarn/container-logs,/mnt/resource/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "6065"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "6065"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "O8lQA3GfsmAlko5IYH52O38s1ModQu"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ac90vmb99j6174xlo1ma5z0j"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-482236f4e21ed514c20a0559f367fe3e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "20d39833-56ef-4119-9df4-79f09eff5adc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7c517epoc9b96zo8mpl2nf9d0"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4837166b7cb5dbed40c46d39ddfe5371",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "7d0fac92-df2b-489e-b900-9f97ac3841a6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9egnxv029g06s0nut6zbejhfp"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "45"
          }, {
            "name" : "role_jceks_password",
            "value" : "814vuz3eqpecj1jily8rykuah"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "3089104896"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "308910489"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "3089104896"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "5405671424"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "909"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "sebct1.madrid.es"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-a60f7c537ff825e6867ad7aab382ee3d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cf816260-7014-4225-a93d-69a8f675c455"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a9f6f82a22eced69d734d4bdad6d8dd3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1xykho42fpt1tot07nzx5ytz2"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-f4a00bceae61f1d9d933f3e2e7d50e69",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4aseylk9j86o6drr3wf8gx3wh"
          } ]
        }
      } ],
      "displayName" : "Hive"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "cad953de-8d69-487f-a892-a9196ebe8080",
    "ipAddress" : "10.0.5.4",
    "hostname" : "sebct1.madrid.es",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "cf816260-7014-4225-a93d-69a8f675c455",
    "ipAddress" : "10.0.5.8",
    "hostname" : "sebct2.madrid.es",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "8666bfcd-eeda-4a45-8a47-85bd92037d0e",
    "ipAddress" : "10.0.5.5",
    "hostname" : "sebct3.madrid.es",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "20d39833-56ef-4119-9df4-79f09eff5adc",
    "ipAddress" : "10.0.5.6",
    "hostname" : "sebct4.madrid.es",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "7d0fac92-df2b-489e-b900-9f97ac3841a6",
    "ipAddress" : "10.0.5.7",
    "hostname" : "sebct5.madrid.es",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],

````
