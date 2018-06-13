Run the uptime command on every node

22:56:12 up 18 min,  1 user,  load average: 0.00, 0.01, 0.05
22:56:12 up 18 min,  1 user,  load average: 0.00, 0.01, 0.05
22:56:12 up 18 min,  1 user,  load average: 0.00, 0.01, 0.05
22:56:12 up 18 min,  1 user,  load average: 0.00, 0.01, 0.05
22:56:12 up 18 min,  1 user,  load average: 0.00, 0.01, 0.05

List the cloud provider you are using

Amazon Web Service

List your instances by IP address and DNS name (don't use /etc/hosts for this)

Public
ec2-18-191-83-35.us-east-2.compute.amazonaws.com 
ec2-18-222-69-30.us-east-2.compute.amazonaws.com 
ec2-18-191-101-43.us-east-2.compute.amazonaws.com 
ec2-18-191-84-206.us-east-2.compute.amazonaws.com 
ec2-52-15-103-123.us-east-2.compute.amazonaws.com 

Privat
172.31.31.117
172.31.17.153
172.31.26.198
172.31.22.241
172.31.17.77

List the Linux release you are using

[ec2-user@ip-172-31-31-117 ~]$ cat /etc/redhat-release
Red Hat Enterprise Linux Server release 7.3 (Maipo)

List the file system capacity for the first node

[ec2-user@ip-172-31-31-117 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       50G  980M   50G   2% /
devtmpfs        7.8G     0  7.8G   0% /dev
tmpfs           7.7G     0  7.7G   0% /dev/shm
tmpfs           7.7G   17M  7.7G   1% /run
tmpfs           7.7G     0  7.7G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/1000


[ec2-user@ip-172-31-31-117 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
rhui-REGION-client-config-server-7                                                                                                              | 2.9 kB  00:00:00     
rhui-REGION-rhel-server-releases                                                                                                                | 3.5 kB  00:00:00     
rhui-REGION-rhel-server-rh-common                                                                                                               | 3.8 kB  00:00:00     
(1/7): rhui-REGION-client-config-server-7/x86_64/primary_db                                                                                     | 3.3 kB  00:00:00     
(2/7): rhui-REGION-rhel-server-releases/7Server/x86_64/group                                                                                    | 855 kB  00:00:00     
(3/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/group                                                                                   |  104 B  00:00:00     
(4/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/primary_db                                                                              | 120 kB  00:00:00     
(5/7): rhui-REGION-rhel-server-releases/7Server/x86_64/updateinfo                                                                               | 2.8 MB  00:00:00     
(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/updateinfo                                                                              |  33 kB  00:00:00     
(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/primary_db                                                                               |  51 MB  00:00:00     
repo id                                                                  repo name                                                                               status
rhui-REGION-client-config-server-7/x86_64                                Red Hat Update Infrastructure 2.0 Client Configuration Server 7                              2
rhui-REGION-rhel-server-releases/7Server/x86_64                          Red Hat Enterprise Linux Server 7 (RPMs)                                                20,399
rhui-REGION-rhel-server-rh-common/7Server/x86_64                         Red Hat Enterprise Linux Server 7 RH Common (RPMs)                                         231
repolist: 20,632



User thanos with a UID of 2500
User hulk with a UID of 2600
User groot with a UID of 2700
Create the group blackorder and add thanos to it
Create the group avengers and add hulk, groot to it


sudo groupadd -g 501 blackorder
sudo groupadd -g 502 avengers

sudo useradd -u 2500 -g blackorder thanos
sudo useradd -u 2600 -g avengers hulk
sudo useradd -u 2700 -g avengers groot

sudo cat /etc/passwd

thanos:x:2500:501::/home/thanos:/bin/bash
hulk:x:2600:502::/home/hulk:/bin/bash
groot:x:2700:502::/home/groot:/bin/bash

sudo cat /etc/group

blackorder:x:501:
avengers:x:502:
