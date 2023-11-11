1. 配置go环境
  - cd /home/allen/syz-adb
  - mkdir gopath
  - cd gopath
  - wget [go.19](https://go.dev/dl/go1.19.12.linux-amd64.tar.gz)（试验过17版本，最后执行会报错）
  - tar -xzvf go1.19.12.linux-amd64.tar.gz
  - vim /ect/profile
    export GOOT=/home/allen/syz-adb/gopath/go
    export PATH=$PATH:$GOROOT/bin
  - source /etc/profile
note：删除syzkaller的bin文件夹后再次编译的时候会报错找不到go，需要再次配置go环境

2. 下载并编译syzkaller
- mkdir -p /src/google/github.com/
- cd /src/google/github.com/
- git clone https://github.com/google/syzkaller.git
- make CC=arrch64-linux-gnu-g++ TARGETARCH=arm64
nate:这里的make用的交叉编译，如果没有配置的话可以用apt install或者其他方式自行配置

4. 配置adb.cfg文件
[参考信息](https://github.com/google/syzkaller/blob/master/docs/linux/setup_linux-host_android-device_arm-kernel.md)
和adb相关的源码路径在vm/adb/adb.go中，遇到问题的话多去看看源码，在源码中找到解决方法

5. 一些运行成功之后的经验
  记得看fuzz time，
