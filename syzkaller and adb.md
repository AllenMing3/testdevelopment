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
mkdir -p /src/google/github.com/
cd /src/google/github.com/
git clone https://github.com/google/syzkaller.git

4. 配置adb.cfg文件
5. 添加udev规则文件
