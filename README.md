trtool
======
[python version](https://github.com/knownsec/rtcp)
Socket data transport tool
----
```
* by bkbll(bkbll@cnhonker.net)
* [bkbll@mobile socket]$ uname -a
* Linux mobile 2.4.18-14 #1 Wed Sep 4 13:35:50 EDT 2002 i686 i686 i386 GNU/Linux
* [bkbll@mobile socket]$ gcc -o trtool trtool.c
* [bkbll@mobile socket]$ ./trtool
* Socket data transport tool
* by bkbll(bkbll@cnhonker.net)
* Usage:./trtool -m method [-h1 host1] -p1 port1 [-h2 host2] -p2 port2 [-v] [-log filename]
* -v: version
* -h1: host1
* -h2: host2
* -p1: port1
* -p2: port2
* -log: log the data
* -m: the action method for this tool
* 1: listen on PORT1 and connect to HOST2:PORT2
* 2: listen on PORT1 and PORT2
* 3: connect to HOST1:PORT1 and HOST2:PORT2
```

Example
----

简单的例子，加入外网主机IP为1.2.3.4，某内网主机开了22.

1.外网主机  lcx -m 2 -p1 10001  -p2 10002

2.内网主机  lcx -m 3 -h1 1.2.3.4 -p1 10001 -h2 127.0.0.1 -p2 22

3.在任何有网的地方包括自己主机都可以用`ssh`连接 1.2.3.4:10002即可以访问内网主机的22端口。
