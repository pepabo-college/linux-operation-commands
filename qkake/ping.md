## pingコマンドについて

### 基本的な動作

* `ping 相手先のホスト名(IPアドレス)`: 相手先のホストが疎通可能な状態か確認する

オプション無しで連続実行されるため、停止する場合は「Ctrl+C」でキャンセルするまでpingを実行し続ける。
また、ホスト名を指定して実行した場合、名前解決も行ってくれる。

#### オプション

* `-c 回数`: 指定回数分のpingを実行させることが可能
* `-I インターフェイス`: 指定したインターフェイス(eth0、eth1など)からpingを実行
* `-r`: 同一セグメントのホストに対してのみ疎通確認を行う
* `-i 実行間隔（秒）`: pingの実行間隔を秒単位で指定
* `-s パケットサイズ`: pingで送信するパケットのサイズを指定
* `-q`: pingの開始・終了時のメッセージのみを表示

### ケーパビリティとは

Linux には、root が持っている絶対的な権限を小分けにし、 細かくした権限をプロセスに与えられるようにする機構がある。
その細かい権限のことを、ケーパビリティと呼ぶ。


### ケーパビリティの設定

ケーパビリティの設定や参照には、以下のパッケージが必要になる。

```
  libcap2-bin  (Ubuntu など)
  libcap       (Fedora など)
```

ファイルのケーパビリティの確認には、getcap コマンドを使用する。

  `$ for file in /usr/bin/; do getcap $file; done`
設定には、setcap コマンドを使用する。
たとえば、コピーした ping コマンドに `CAP_NET_RAW` を設定するには、 以下のように実行する。

```
  # cp `which ping` /home/ryosuke/ping
  # setcap cap_net_raw=ep /home/ryosuke/ping
  # getcap /home/ryosuke/ping
  /home/ryosuke/ping = cap_net_raw+ep
```

ちなみに、各所の ep は、前述と同様 effective と permitted です。

### ケーパビリティ・セット

プロセスは、以下の3種類のケーパビリティ・セットというものを持っていて、 それぞれに対してケーパビリティを設定できる。

* effective (実効)

プロセスの権限をチェックするときに使われるケーパビリティセット。
カーネルがこの値を見て、その操作を許可するかどうか判断する。

* permitted (許可)
プロセスが持つことを許可されているケーパビリティセット。

* inheritable (継承可能)
コマンドを実行するときに継承されるケーパビリティセット。

### ケーパビリティを設定するとどうなるか

通常、ping コマンドには root の setuid が設定されているため、 一般ユーザでも実行することができます。

```
  $ ls -l `which ping`
  -rwsr-xr-x 1 root root 34756 2010-03-12 08:12 /bin/ping
```

さきほどコピーした ping コマンドには、setuid が設定されてないけど、 `CAP_NET_RAW` が設定されているから一般ユーザも実行できる。

```
  $ /home/ryosuke/ping localhost
  PING localhost (127.0.0.1) 56(84) bytes of data.
  64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.078 ms
  64 bytes from localhost (127.0.0.1): icmp_seq=2 ttl=64 time=0.066 ms
  .....
```


### ケーパビリティをなくす

`-r` オプションをつかう

```
  # setcap -r /home/ryosuke/ping
```

ケーパビリティがないと、当然ですが、一般人は実行できなくなります。

```
  $ /home/ryosuke/ping localhost
  ping: icmp open socket: Operation not permitted
```
