# netstat -anp コマンドについて(Linux)

## netstatとは
* ネットワーク関連の統計情報を表示する
* https://linuxjm.osdn.jp/html/net-tools/man8/netstat.8.html

## インストール
* `yum install net-tools`

## netstat -anp
* -a	全てのソケットを表示する
  * 接続待ち状態にあるソケットも、接続待ち状態にないソケットも表示する
* -n	ホスト名などを解決せずに数字で表示する
  * ホスト・ポート・ユーザーなどの名前を解決せずに、数字のアドレスで表示する
* -p	各ソケットを利用しているプログラムのプロセスIDを表示する

## どんなときに使うか？

* リッスンしているポートのプロセスを調べるとき
* 例：

````
netstat -anp | grep 22

Proto Recv-Q Send-Q Local Address               Foreign Address             State       PID/Program name
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      901/sshd
tcp        0      0 10.0.2.15:22            10.0.2.2:54948          ESTABLISHED 20268/sshd: vagrant
tcp6       0      0 :::22                   :::*                    LISTEN      901/sshd
````

* LISTENしているポートを実際に見てみる

````
ps aux | grep 901

root       901  0.0  0.7  82548  3612 ?        Ss   03:34   0:00 /usr/sbin/sshd -D
````

上記のように、`netstat -anp`はリッスンしているポートのプロセスを調べるときに使用する。

## どの情報見て出力しているのか？
*  `/etc/services` -- サービス名と番号の変換表が入ったファイル
* `/proc -- proc` ファイルシステムのマウントポイント。 このファイルシステムにより、 以下のファイルを使ってカーネルの統計情報にアクセスできる。
* `/proc/net/dev` -- デバイスの情報
* `/proc/net/raw` raw ソケットの情報
* `/proc/net/tcp` -- TCP ソケットの情報
* `/proc/net/udp` -- UDP ソケットの情報
* `/proc/net/igmp` -- IGMP マルチキャストの情報
* `/proc/net/unix` -- Unix ドメインソケットの情報
* `/proc/net/ipx` -- IPX ソケットの情報
* `/proc/net/ax25` -- AX25 ソケットの情報
* `/proc/net/appletalk` -- DDP (appletalk) ソケットの情報
* `/proc/net/nr` -- NET/ROM ソケットの情報
* `/proc/net/route` -- IP 経路情報
* `/proc/net/ax25_route` -- AX25 経路情報
* `/proc/net/ipx_route` -- IPX 経路情報
* `/proc/net/nr_nodes` -- NET/ROM ノードリスト
* `/proc/net/nr_neigh` -- NET/ROM ネイバー (neighbour)
* `/proc/net/ip_masquerade` -- マスカレード接続
* `/proc/net/snmp` -- 統計情報

## その他組み合わせ
* `netstat -tlnp`
  * tcpのプロセスのみ表示したいとき（かつ名前解決せず、PIDを表示する）
* `netstat -ulnp`
  * udpのプロセスのみ表示したいとき（かつ名前解決せず、PIDを表示する）
