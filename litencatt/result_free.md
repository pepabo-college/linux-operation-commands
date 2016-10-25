[vgrant@nagios01 ~]$ free
              total        used        free      shared  buff/cache   available
Mem:         500768       71704      305724        4736      123340      392376
Swap:       1572860           0     1572860
[vagrant@nagios01 ~]$ free -b
              total        used        free      shared  buff/cache   available
Mem:      512786432    73412608   313073664     4849664   126300160   401805312
Swap:    1610608640           0  1610608640
[vagrant@nagios01 ~]$ free -k
              total        used        free      shared  buff/cache   available
Mem:         500768       71700      305728        4736      123340      392380
Swap:       1572860           0     1572860
[vagrant@nagios01 ~]$ free -m
              total        used        free      shared  buff/cache   available
Mem:            489          70         298           4         120         383
Swap:          1535           0        1535
[vagrant@nagios01 ~]$ free -g
              total        used        free      shared  buff/cache   available
Mem:              0           0           0           0           0           0
Swap:             1           0           1
[vagrant@nagios01 ~]$ free -h
              total        used        free      shared  buff/cache   available
Mem:           489M         70M        298M        4.6M        120M        383M
Swap:          1.5G          0B        1.5G
[vagrant@nagios01 ~]$ free -s 1
              total        used        free      shared  buff/cache   available
Mem:         500768       71708      305720        4736      123340      392372
Swap:       1572860           0     1572860

              total        used        free      shared  buff/cache   available
Mem:         500768       71728      305700        4736      123340      392352
Swap:       1572860           0     1572860

              total        used        free      shared  buff/cache   available
Mem:         500768       71728      305700        4736      123340      392352
Swap:       1572860           0     1572860

^C
[vagrant@nagios01 ~]$ free -t
              total        used        free      shared  buff/cache   available
Mem:         500768       71724      305704        4736      123340      392356
Swap:       1572860           0     1572860
Total:      2073628       71724     1878564
[vagrant@nagios01 ~]$ 
