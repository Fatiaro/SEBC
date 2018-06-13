[ec2-user@ip-172-31-17-153 5.11.2.4]$ sudo tail -1 /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-18 00:09:53,638 INFO ScmActive-0:com.cloudera.server.cmf.components.ScmActive: ScmActive completed successfully.
[ec2-user@ip-172-31-17-153 5.11.2.4]$ sudo grep -i "Started Jetty server" /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-18 00:09:52,177 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
[ec2-user@ip-172-31-17-153 5.11.2.4]$ 
