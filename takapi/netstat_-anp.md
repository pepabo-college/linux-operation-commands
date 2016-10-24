# netstat -anp コマンドについて(Linux)

## netstatとは
* ネットワーク関連の統計情報を表示する

## 構文
`netstat [option1] [option2]`

## netstat -anp
* -a	全てのソケットを表示する
  * 接続待ち状態にあるソケットも、接続待ち状態にないソケットも表示する。
* -n	ホスト名などを解決せずに数字で表示する
  * ホスト・ポート・ユーザーなどの名前を解決せずに、数字のアドレスで表示する。
* -p	各ソケットを利用しているプログラムのプロセスIDを表示する

## どんな時に使うか？

* リッスンしているポートのプロセスを調べるとき

````
netstat -anp | grep 22

Proto Recv-Q Send-Q Local Address               Foreign Address             State       PID/Program name
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      901/sshd
tcp        0      0 10.0.2.15:22            10.0.2.2:54948          ESTABLISHED 20268/sshd: vagrant
tcp6       0      0 :::22                   :::*                    LISTEN      901/sshd
unix  3      [ ]         STREAM     CONNECTED     16622    1330/master
unix  3      [ ]         STREAM     CONNECTED     13967    622/crond
unix  2      [ ]         DGRAM                    13981    622/crond
````

* LISTENしているポートを実際に見てみる

````
ps aux | grep 901
root       901  0.0  0.7  82548  3612 ?        Ss   03:34   0:00 /usr/sbin/sshd -D
````

上記のように、`netstat -anp`はリッスンしているポートのプロセスを調べるときに使用する。
