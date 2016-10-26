# ps
* プロセスの状態や親子関係を確認できるコマンド

## 実行結果
(途中で部分的に貼り付けただけなので、途中で切れている)
```
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         2  0.0  0.0      0     0 ?        S    05:51   0:00 [kthreadd]
root         3  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [ksoftirqd/0]
root         5  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kworker/0:0H]
root         6  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [kworker/u2:0]
root         7  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [migration/0]
root         8  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [rcu_bh]
root         9  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [rcuob/0]
root        10  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [rcu_sched]
root        11  0.0  0.0      0     0 ?        R    05:51   0:00  \_ [rcuos/0]
root        12  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [watchdog/0]
root        13  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [khelper]
root        14  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [kdevtmpfs]
root        15  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [netns]
root        16  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [perf]
root        17  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [writeback]
root        18  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kintegrityd]
root        19  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [bioset]
root        20  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kblockd]
root        21  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [md]
root        26  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [khungtaskd]
root        27  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [kswapd0]
root        28  0.0  0.0      0     0 ?        SN   05:51   0:00  \_ [ksmd]
root        29  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [fsnotify_mark]
root        30  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [crypto]
root        38  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kthrotld]
root        40  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kmpath_rdacd]
root        41  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kpsmoused]
root        42  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [ipv6_addrconf]
root        62  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [deferwq]
root        92  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [kauditd]
root       253  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [ata_sff]
root       257  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [scsi_eh_0]
root       261  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [scsi_tmf_0]
root       262  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [scsi_eh_1]
root       265  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [scsi_tmf_1]
root       283  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kworker/0:1H]
root       343  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kdmflush]
root       344  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [bioset]
root       353  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [kdmflush]
root       354  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [bioset]
root       369  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfsalloc]
root       370  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs_mru_cache]
root       371  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-buf/dm-0]
root       372  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-data/dm-0]
root       373  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-conv/dm-0]
root       374  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-cil/dm-0]
root       375  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-reclaim/dm-]
root       376  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-log/dm-0]
root       377  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-eofblocks/d]
root       378  0.0  0.0      0     0 ?        R    05:51   0:04  \_ [xfsaild/dm-0]
root       469  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [rpciod]
root       548  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-buf/sda2]
root       550  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-data/sda2]
root       551  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-conv/sda2]
root       552  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-cil/sda2]
root       553  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-reclaim/sda]
root       554  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-log/sda2]
root       555  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [xfs-eofblocks/s]
root       557  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [xfsaild/sda2]
root      3209  0.0  0.0      0     0 ?        S<   05:51   0:00  \_ [nfsiod]
root      3214  0.0  0.0      0     0 ?        S    05:51   0:00  \_ [lockd]
root      3370  0.0  0.0      0     0 ?        S    06:06   0:00  \_ [kworker/u2:1]
root      4339  0.0  0.0      0     0 ?        S    09:10   0:00  \_ [kworker/0:2]
root      4382  0.0  0.0      0     0 ?        S    09:20   0:00  \_ [kworker/0:0]
root      4494  0.0  0.0      0     0 ?        S    09:28   0:00  \_ [kworker/0:1]
root         1  0.0  2.3  43896  5652 ?        Ss   05:51   0:01 /usr/lib/systemd/systemd --switched-root --system --deserialize 21
root       450  0.0  1.0  32720  2500 ?        Ss   05:51   0:00 /usr/lib/systemd/systemd-journald
root       474  0.0  0.8 129132  2156 ?        Ss   05:51   0:00 /usr/sbin/lvmetad -f
root       476  0.0  1.1  45740  2676 ?        Ss   05:51   0:00 /usr/lib/systemd/systemd-udevd
root       577  0.0  0.5  51188  1324 ?        S<sl 05:51   0:00 /sbin/auditd -n
root       599  0.0  1.0 283324  2488 ?        Ssl  05:51   0:00 /usr/sbin/rsyslogd -n
dbus       602  0.0  0.6  34960  1460 ?        Ssl  05:51   0:00 /bin/dbus-daemon --system --address=systemd: --nofork --nopidfile --sys
chrony     604  0.0  0.5 100648  1360 ?        S    05:51   0:00 /usr/sbin/chronyd
root       609  0.0  0.3 203368   904 ?        Ssl  05:51   0:00 /usr/sbin/gssproxy -D
root       614  0.0  0.6  26400  1536 ?        Ss   05:51   0:00 /usr/lib/systemd/systemd-logind
root       622  0.0  2.0 508564  4956 ?        Ssl  05:51   0:00 /usr/sbin/NetworkManager --no-daemon
```

## axufオプション
* a: 端末を持つ全てのプロセスを表示する
* x: 端末を持たない全てのプロセスを表示する
* u: ユーザー指向のフォーマット（加工の容易さよりも読みやすさを優先したフォーマット）で表示する
* f: 階層表示する

## カラムの意味
### USER
* ユーザID

### PID
* プロセスID

### %CPU
* CPU使用率

### %MEM
* 実メモリ使用量

### VSZ
* 仮想メモリの使用サイズ(キロバイト表示)
* プログラムが仮想メモリ領域を確保するとVSZの値は上がるが、物理メモリへの確保(RSS)はまだ行われていない。そのため、VSZの値が高いからといって物理メモリの消費が多いとは判断できない。
* 物理メモリへの確保が行われるのは、実際に書き込み処理などが発生した時に初めて行われる。

### RSS
* 物理メモリの使用サイズ(キロバイト表示)
* Linuxには、同じプログラムを複数起動した場合のバイナリファイルなど、共有できる部分は同じメモリ領域を参照する仕組みがある。そのため、RSSの値を合計値と実際の物理メモリ消費量は、イコールになるとは限らないので注意する。

### TTY
* 使用端末

### STAT
* プロセスのステータス
  * S: 割り込み可能なスリープ状態
  * s: セッションリーダ
  * D: 割り込み不可能なスリープ状態
    * killコマンドを使ってもプロセスを削除できない(killのシグナルも割り込み処理であるため)
  * R: 実行可能状態(待ち状態)
  * O: 実行中
  * I: プロセス生成中
  * Z: 親プロセスとの関係が切れた状態（ゾンビプロセス）
    * 基本的にプロセスには親プロセスがいる。親プロセスは子プロセスの終了コードを受け取る機能がある。
    * 親プロセスが終了コードを受け取れない場合に、子プロセスはゾンビプロセスになる。
    * 親プロセスが終了コードを受け取れない場合として、次のようなものが考えられる
      * 親プロセスのみが何らかの事情で終了してしまっている場合
      * 親プロセスが終了コードを受け取る処理に時間がかかっている場合(Apacheなど子プロセスが多いもので発生する。こちらの場合は、時間が経つとゾンビプロセスではない状態になる)
  * N: 優先度低い
  * \>: 優先度高い
  * +: フォアグラウンドのプロセスグループに入っている
  * T: 停止中
    * `kill STOP`を行うことで発生する状態
    * 停止解除するには、`kill CONT`を行う

### START
* プロセスの開始時刻

### TIME
* プロセスの総実行時間(CPUの累積使用時間)

### COMMAND
* 実行コマンド名とパス（シェル表記の場合もあり）

##  COMMANDカラムの[]の意味
* [] が付くプロセスは、カーネルモード（特権モード）で動作するプロセス。
* それ以外は、ユーザモードで動作するプロセス。

## 参考文献
* [psコマンドまとめ](http://qiita.com/shell/items/68ed71a7f018e5688f73)
* [「ps aux」コマンドで表示される項目の意味を知りたい](http://www.itmedia.co.jp/help/tips/linux/l0158.html)
* [psコマンドでの[]付き表示について](http://www.turbolinux.com/support/document/knowledge/556.html)
