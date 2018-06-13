[ec2-user@ip-172-31-19-50 ~]$ export HADOOP_USER_NAME=hdfs
[ec2-user@ip-172-31-19-50 ~]$ hdfs dfs -mkdir /user/jimenez
[ec2-user@ip-172-31-19-50 ~]$ hdfs dfs -mkdir /user/beltran

[ec2-user@ip-172-31-19-50 ~]$ hdfs dfs -ls /user
Found 6 items
drwxr-xr-x   - hdfs   supergroup          0 2018-05-17 03:57 /user/beltran
drwxrwxrwx   - mapred hadoop              0 2018-05-17 03:47 /user/history
drwxrwxr-t   - hive   hive                0 2018-05-17 03:47 /user/hive
drwxrwxr-x   - hue    hue                 0 2018-05-17 03:48 /user/hue
drwxr-xr-x   - hdfs   supergroup          0 2018-05-17 03:57 /user/jimenez
drwxrwxr-x   - oozie  oozie               0 2018-05-17 03:48 /user/oozie
[ec2-user@ip-172-31-19-50 ~]$


[ec2-user@ip-172-31-31-27 ~]$ curl -u admin:admin 'http://localhost:7180/api/v5/hosts'
{
  "items" : [ {
    "hostId" : "36df64bc-90cb-4f8b-b64f-aa7a2622cf35",
    "ipAddress" : "172.31.19.50",
    "hostname" : "ip-172-31-19-50.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/hostRedirect/36df64bc-90cb-4f8b-b64f-aa7a2622cf35",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16388530176
  }, {
    "hostId" : "2502f5ef-8cbb-4b08-b767-925414f6c611",
    "ipAddress" : "172.31.22.14",
    "hostname" : "ip-172-31-22-14.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/hostRedirect/2502f5ef-8cbb-4b08-b767-925414f6c611",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16388530176
  }, {
    "hostId" : "507665f6-c181-4d8a-8faf-8c5e03b93ebc",
    "ipAddress" : "172.31.23.117",
    "hostname" : "ip-172-31-23-117.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/hostRedirect/507665f6-c181-4d8a-8faf-8c5e03b93ebc",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16388530176
  }, {
    "hostId" : "6f5bb0ae-e12c-420c-92b3-6008a95aed4a",
    "ipAddress" : "172.31.29.95",
    "hostname" : "ip-172-31-29-95.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/hostRedirect/6f5bb0ae-e12c-420c-92b3-6008a95aed4a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16388530176
  }, {
    "hostId" : "0cb07df4-2ab7-4a69-8140-6e792ce9eee3",
    "ipAddress" : "172.31.31.27",
    "hostname" : "ip-172-31-31-27.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/hostRedirect/0cb07df4-2ab7-4a69-8140-6e792ce9eee3",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16388530176
  } ]
}[ec2-user@ip-172-31-31-27 ~]$ 


}[ec2-user@ip-172-31-31-27 ~]$curl -u admin:admin 'http://localhost:7180/api/v11/clusters/fatiaro/services'
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/zookeeper/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/oozie",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/oozie/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hue",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hue/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HUE_LOAD_BALANCER_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hdfs/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/yarn",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/yarn/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hbase",
    "type" : "HBASE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hbase",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hbase/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HBASE_MASTER_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HBASE_REGION_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HBase",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl" : "http://ip-172-31-31-27.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive",
    "entityStatus" : "GOOD_HEALTH"
  } ]
}[ec2-user@ip-172-31-31-27 ~]$ 

