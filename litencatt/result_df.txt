[vagrant@nagios01 ~]$ df
ファイルシス                    1K-ブロック    使用   使用可 使用% マウント位置
/dev/mapper/VolGroup00-LogVol00    39498912 1172312 38326600    3% /
devtmpfs                             239320       0   239320    0% /dev
tmpfs                                250384       0   250384    0% /dev/shm
tmpfs                                250384    4424   245960    2% /run
tmpfs                                250384       0   250384    0% /sys/fs/cgroup
/dev/sda2                            508588  128636   379952   26% /boot
tmpfs                                 50080       0    50080    0% /run/user/1000
[vagrant@nagios01 ~]$ df -a
ファイルシス                    1K-ブロック    使用   使用可 使用% マウント位置
rootfs                                    -       -        -     - /
sysfs                                     0       0        0     - /sys
proc                                      0       0        0     - /proc
devtmpfs                             239320       0   239320    0% /dev
securityfs                                0       0        0     - /sys/kernel/security
tmpfs                                250384       0   250384    0% /dev/shm
devpts                                    0       0        0     - /dev/pts
tmpfs                                250384    4424   245960    2% /run
tmpfs                                250384       0   250384    0% /sys/fs/cgroup
cgroup                                    0       0        0     - /sys/fs/cgroup/systemd
pstore                                    0       0        0     - /sys/fs/pstore
cgroup                                    0       0        0     - /sys/fs/cgroup/freezer
cgroup                                    0       0        0     - /sys/fs/cgroup/cpu,cpuacct
cgroup                                    0       0        0     - /sys/fs/cgroup/perf_event
cgroup                                    0       0        0     - /sys/fs/cgroup/hugetlb
cgroup                                    0       0        0     - /sys/fs/cgroup/devices
cgroup                                    0       0        0     - /sys/fs/cgroup/net_cls
cgroup                                    0       0        0     - /sys/fs/cgroup/memory
cgroup                                    0       0        0     - /sys/fs/cgroup/cpuset
cgroup                                    0       0        0     - /sys/fs/cgroup/blkio
configfs                                  0       0        0     - /sys/kernel/config
/dev/mapper/VolGroup00-LogVol00    39498912 1172312 38326600    3% /
selinuxfs                                 0       0        0     - /sys/fs/selinux
systemd-1                                 0       0        0     - /proc/sys/fs/binfmt_misc
debugfs                                   0       0        0     - /sys/kernel/debug
hugetlbfs                                 0       0        0     - /dev/hugepages
mqueue                                    0       0        0     - /dev/mqueue
sunrpc                                    0       0        0     - /var/lib/nfs/rpc_pipefs
nfsd                                      0       0        0     - /proc/fs/nfsd
/dev/sda2                            508588  128636   379952   26% /boot
tmpfs                                 50080       0    50080    0% /run/user/1000
[vagrant@nagios01 ~]$ df -i
ファイルシス                     Iノード I使用    I残り I使用% マウント位置
/dev/mapper/VolGroup00-LogVol00 39518208 35806 39482402     1% /
devtmpfs                           59830   331    59499     1% /dev
tmpfs                              62596     1    62595     1% /dev/shm
tmpfs                              62596   391    62205     1% /run
tmpfs                              62596    13    62583     1% /sys/fs/cgroup
/dev/sda2                         512000   330   511670     1% /boot
tmpfs                              62596     1    62595     1% /run/user/1000
[vagrant@nagios01 ~]$ df -t
df: オプションには引数が必要です -- 't'
Try 'df --help' for more information.
[vagrant@nagios01 ~]$ df -x
df: オプションには引数が必要です -- 'x'
Try 'df --help' for more information.
[vagrant@nagios01 ~]$ df -h
ファイルシス                    サイズ  使用  残り 使用% マウント位置
/dev/mapper/VolGroup00-LogVol00    38G  1.2G   37G    3% /
devtmpfs                          234M     0  234M    0% /dev
tmpfs                             245M     0  245M    0% /dev/shm
tmpfs                             245M  4.4M  241M    2% /run
tmpfs                             245M     0  245M    0% /sys/fs/cgroup
/dev/sda2                         497M  126M  372M   26% /boot
tmpfs                              49M     0   49M    0% /run/user/1000
[vagrant@nagios01 ~]$ 
