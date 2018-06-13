[ec2-user@ip-172-31-19-50 ~]$ hostname -f
ip-172-31-19-50.us-east-2.compute.internal
[ec2-user@ip-172-31-19-50 ~]$ mysql -u root -p -e "status;"
Enter password: 
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:		5
Current database:	
Current user:		root@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server:			MariaDB
Server version:		5.5.56-MariaDB MariaDB Server
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	utf8
Conn.  characterset:	utf8
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			21 min 30 sec

Threads: 1  Questions: 40  Slow queries: 0  Opens: 0  Flush tables: 2  Open tables: 26  Queries per second avg: 0.031
--------------

[ec2-user@ip-172-31-19-50 ~]$ mysql -u root  -p -e "show databases;"
Enter password: 
+--------------------+
| Database           |
+--------------------+
| information_schema |
| cmserver           |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
| test               |
+--------------------+
[ec2-user@ip-172-31-19-50 ~]$ 
