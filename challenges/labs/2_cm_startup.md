[ec2-user@ip-172-31-31-27 ~]$ sudo tail -2 /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-17 03:31:34,179 INFO StaleEntityEviction:com.cloudera.server.cmf.StaleEntityEvictionThread: Found no commands older than 2016-05-17T07:31:34.178Z to reap.
2018-05-17 03:31:34,180 INFO StaleEntityEviction:com.cloudera.server.cmf.StaleEntityEvictionThread: Wizard is active, not reaping scanners or configurators

[ec2-user@ip-172-31-31-27 ~]$ sudo grep -i "Started Jetty server" /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-17 03:11:45,306 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
[ec2-user@ip-172-31-31-27 ~]$
