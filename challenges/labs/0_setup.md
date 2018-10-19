# Setup

Cloud Provider: Azure

OS: CentOS 7.3

**Note:** **Ansible** was installed in the host `sebce1.madrid.es` to facilitate the distribution of operations.

```
yum install -y epel-release
yum install ansible
```

##### Internal IP/Hostnames
| Private IP | Hostname |
|:--|:--|
| 10.0.6.4 | sebce1.madrid.es |
| 10.0.6.5 | sebce2.madrid.es |
| 10.0.6.6 | sebce3.madrid.es |
| 10.0.6.7 | sebce4.madrid.es |
| 10.0.6.8 | sebce5.madrid.es |

##### Public IP/DNS
| Public IP  |  Public DNS |
|:--|:--|
|40.123.44.113  |  sebce1.eastus2.cloudapp.azure.com |
|104.46.122.40  |  sebce2.eastus2.cloudapp.azure.com |
|104.209.236.98 |  sebce3.eastus2.cloudapp.azure.com |
|104.46.114.221 |  sebce4.eastus2.cloudapp.azure.com |
|104.209.243.2  |  sebce5.eastus2.cloudapp.azure.com |


#### CentOS Release
````
[root@sebce1 ~]# ansible all -a "cat /etc/centos-release"
sebce1.madrid.es | CHANGED | rc=0 >>
CentOS Linux release 7.3.1611 (Core)

sebce5.madrid.es | CHANGED | rc=0 >>
CentOS Linux release 7.3.1611 (Core)

sebce3.madrid.es | CHANGED | rc=0 >>
CentOS Linux release 7.3.1611 (Core)

sebce4.madrid.es | CHANGED | rc=0 >>
CentOS Linux release 7.3.1611 (Core)

sebce2.madrid.es | CHANGED | rc=0 >>
CentOS Linux release 7.3.1611 (Core)
````

## Disk Space

````
[root@sebce1 ~]# ansible all -a "df -h"
sebce4.madrid.es | CHANGED | rc=0 >>
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        40G  1.2G   39G   3% /
devtmpfs        7.9G     0  7.9G   0% /dev
tmpfs           7.9G     0  7.9G   0% /dev/shm
tmpfs           7.9G  8.4M  7.9G   1% /run
tmpfs           7.9G     0  7.9G   0% /sys/fs/cgroup
/dev/sda1       497M   62M  436M  13% /boot
/dev/sdc1       100G   33M  100G   1% /data/01
/dev/sdb1        32G   49M   30G   1% /mnt/resource
tmpfs           1.6G     0  1.6G   0% /run/user/1000
tmpfs           1.6G     0  1.6G   0% /run/user/0

sebce3.madrid.es | CHANGED | rc=0 >>
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        40G  1.2G   39G   3% /
devtmpfs        7.9G     0  7.9G   0% /dev
tmpfs           7.9G     0  7.9G   0% /dev/shm
tmpfs           7.9G  8.4M  7.9G   1% /run
tmpfs           7.9G     0  7.9G   0% /sys/fs/cgroup
/dev/sda1       497M   62M  436M  13% /boot
/dev/sdc1       100G   33M  100G   1% /data/01
/dev/sdb1        32G   49M   30G   1% /mnt/resource
tmpfs           1.6G     0  1.6G   0% /run/user/1000
tmpfs           1.6G     0  1.6G   0% /run/user/0

sebce2.madrid.es | CHANGED | rc=0 >>
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        40G  1.2G   39G   3% /
devtmpfs        7.9G     0  7.9G   0% /dev
tmpfs           7.9G     0  7.9G   0% /dev/shm
tmpfs           7.9G  8.4M  7.9G   1% /run
tmpfs           7.9G     0  7.9G   0% /sys/fs/cgroup
/dev/sda1       497M   62M  436M  13% /boot
/dev/sdb1       100G   33M  100G   1% /data/01
/dev/sdc1        32G   49M   30G   1% /mnt/resource
tmpfs           1.6G     0  1.6G   0% /run/user/1000
tmpfs           1.6G     0  1.6G   0% /run/user/0

sebce5.madrid.es | CHANGED | rc=0 >>
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        40G  1.2G   39G   3% /
devtmpfs        7.9G     0  7.9G   0% /dev
tmpfs           7.9G     0  7.9G   0% /dev/shm
tmpfs           7.9G  8.4M  7.9G   1% /run
tmpfs           7.9G     0  7.9G   0% /sys/fs/cgroup
/dev/sda1       497M   62M  436M  13% /boot
/dev/sdc1       100G   33M  100G   1% /data/01
/dev/sdb1        32G   49M   30G   1% /mnt/resource
tmpfs           1.6G     0  1.6G   0% /run/user/1000
tmpfs           1.6G     0  1.6G   0% /run/user/0

sebce1.madrid.es | CHANGED | rc=0 >>
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        40G  1.5G   39G   4% /
devtmpfs        7.9G     0  7.9G   0% /dev
tmpfs           7.9G  124K  7.9G   1% /dev/shm
tmpfs           7.9G  8.4M  7.9G   1% /run
tmpfs           7.9G     0  7.9G   0% /sys/fs/cgroup
/dev/sdc1       100G   33M  100G   1% /data/01
/dev/sda1       497M   62M  436M  13% /boot
/dev/sdb1        32G   49M   30G   1% /mnt/resource
tmpfs           1.6G     0  1.6G   0% /run/user/1000
tmpfs           1.6G     0  1.6G   0% /run/user/0

````

## Yum enabled repos
````
[root@sebce1 ~]# ansible all -a "yum repolist enabled"
 [WARNING]: Consider using the yum module rather than running yum.  If you need to use command because yum is insufficient you
can add warn=False to this command task or set command_warnings=False in ansible.cfg to get rid of this message.

sebce3.madrid.es | CHANGED | rc=0 >>
Loaded plugins: fastestmirror, langpacks
Determining fastest mirrors
repo id                   repo name                                       status
base/7/x86_64             CentOS-7 - Base                                 9,911
extras/7/x86_64           CentOS-7 - Extras                                 432
openlogic/7/x86_64        CentOS-7 - openlogic packages for x86_64          115
updates/7/x86_64          CentOS-7 - Updates                              1,561
repolist: 12,019

sebce5.madrid.es | CHANGED | rc=0 >>
Loaded plugins: fastestmirror, langpacks
Determining fastest mirrors
repo id                   repo name                                       status
base/7/x86_64             CentOS-7 - Base                                 9,911
extras/7/x86_64           CentOS-7 - Extras                                 432
openlogic/7/x86_64        CentOS-7 - openlogic packages for x86_64          115
updates/7/x86_64          CentOS-7 - Updates                              1,561
repolist: 12,019

sebce2.madrid.es | CHANGED | rc=0 >>
Loaded plugins: fastestmirror, langpacks
Determining fastest mirrors
repo id                   repo name                                       status
base/7/x86_64             CentOS-7 - Base                                 9,911
extras/7/x86_64           CentOS-7 - Extras                                 432
openlogic/7/x86_64        CentOS-7 - openlogic packages for x86_64          115
updates/7/x86_64          CentOS-7 - Updates                              1,561
repolist: 12,019

sebce4.madrid.es | CHANGED | rc=0 >>
Loaded plugins: fastestmirror, langpacks
Determining fastest mirrors
repo id                   repo name                                       status
base/7/x86_64             CentOS-7 - Base                                 9,911
extras/7/x86_64           CentOS-7 - Extras                                 432
openlogic/7/x86_64        CentOS-7 - openlogic packages for x86_64          115
updates/7/x86_64          CentOS-7 - Updates                              1,561
repolist: 12,019

sebce1.madrid.es | CHANGED | rc=0 >>
Loaded plugins: fastestmirror, langpacks
Loading mirror speeds from cached hostfile
 * epel: mirror.cogentco.com
repo id                repo name                                          status
!base/7/x86_64         CentOS-7 - Base                                     9,911
!epel/x86_64           Extra Packages for Enterprise Linux 7 - x86_64     12,741
!extras/7/x86_64       CentOS-7 - Extras                                     432
!openlogic/7/x86_64    CentOS-7 - openlogic packages for x86_64              115
!updates/7/x86_64      CentOS-7 - Updates                                  1,561
repolist: 24,760
````

## Users & Groups

### Contents of `/etc/passwd`
```
[root@sebce1 ~]# ansible all -a "grep 'raffles\|fullerton' /etc/passwd"
sebce3.madrid.es | CHANGED | rc=0 >>
raffles:x:2000:1002::/home/raffles:/bin/bash
fullerton:x:3000:1001::/home/fullerton:/bin/bash

sebce2.madrid.es | CHANGED | rc=0 >>
raffles:x:2000:1002::/home/raffles:/bin/bash
fullerton:x:3000:1001::/home/fullerton:/bin/bash

sebce4.madrid.es | CHANGED | rc=0 >>
raffles:x:2000:1002::/home/raffles:/bin/bash
fullerton:x:3000:1001::/home/fullerton:/bin/bash

sebce5.madrid.es | CHANGED | rc=0 >>
raffles:x:2000:1002::/home/raffles:/bin/bash
fullerton:x:3000:1001::/home/fullerton:/bin/bash

sebce1.madrid.es | CHANGED | rc=0 >>
raffles:x:2000:1002::/home/raffles:/bin/bash
fullerton:x:3000:1001::/home/fullerton:/bin/bash

```

### Contents of `/etc/group`
```
[root@sebce1 ~]# ansible all -a "grep 'hotels\|shops' /etc/group"
sebce1.madrid.es | CHANGED | rc=0 >>
hotels:x:1001:
shops:x:1002:

sebce2.madrid.es | CHANGED | rc=0 >>
hotels:x:1001:
shops:x:1002:

sebce4.madrid.es | CHANGED | rc=0 >>
hotels:x:1001:
shops:x:1002:

sebce5.madrid.es | CHANGED | rc=0 >>
hotels:x:1001:
shops:x:1002:

sebce3.madrid.es | CHANGED | rc=0 >>
hotels:x:1001:
shops:x:1002:
```
