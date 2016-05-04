iperf3:  A TCP, UDP, and SCTP network bandwidth measurement tool
================================================================
# install
``` 
$ ./configure
$ make clean
$ make
$ sudo make install
$ sudo apt-get install libiperf-dev
```
# install on raspbian
```
$ ./configure
$ make clean
$ make
$ sudo apt-get install libiperf0
$ sudo make install
$ sudo apt-get remove libiperf0
```

# -E参数使用方法
* -E只能跟-u 和 -i同时使用, 指定一个文件, 文件内容每一行为每一个interval的速率, 单位为Kbits/s
* example: iperf3 -c 127.0.0.1 -u -t 100 -i 2 -E flow.txt
* 服务端无需安装此版本
