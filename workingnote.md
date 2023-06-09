在20230606从之前的智能硬件的产品测试，转行成为了一个偏互联网公司的测试开发岗位，接下来是在就职期间，在就职期间有不断的了解这个行业，关于测试开发的一些学习和想法

##### 20230703本周收获
前半周主要是在跑一些自动化用例的，包括xts测试，冒烟测试等等，后半周主要是开始去写一点点（抄一遍） python 和 shell 的脚本。因为收获方面大多数都是直接和公司业务相关的，就不写了，除了业务外的主要收获：
1. 主要是熟悉了一下 python 写脚本的一些用法吧，包括如何写日志的用法，SSH 连接用法，shell 脚本的特殊符号的含义等。
2. 第二个应该就是明确了短期内需要重点补上的知识点：需要在一周左右的时间内补上安卓系统内核部分的一些基本知识，包括文件结构，熟悉代码的用法；第二个是一周内上手写 python 测试脚本文件。

##### 20230626本周收获
这周的工作的话看 Jenkins 的代码和 log 比较多，不管是pipeline的代码，或者是 Jenkins 本身 workspace 文件夹中的脚本文件。最主要的原因就是在跑流水线的时候，发现连续好几次都出现在同一个 python 脚本的时候出现了 default 的错误。然后在这个找问题的过程中学会了几个新的方法吧。
1. 如果有可以将没有跑通的流水线的跑通的console output进行核对，找到在执行命令后有哪些地方是不一样的。
2. 在执行命令的目录下，cmd，执行相同命令（包括需要的参数），确定代码本身是不是有问题。
3. 在查看Jenkins代码写入的具体文件，看文件的内容。是不是目标内容，缩小范围，具体的哪一个写入出了问题。
4. 最后再是查看编译log文件。
当然，还有一些工作上的小技巧，因为上周在工作中遇到的很多很麻烦的问题，凭借我自己的能力解决起来比较困难，这个时候在**沟通**中出了一些问题，感觉*同事帮忙的意愿比较弱*。作为一名工程师，这个也是我需要提高的点。让*同事更加信任自己，提出问题前需要更多的自己的思考和尝试，问题也需要更具体一些，某个地地方，某个东西不懂*

##### 20230619本周收获
这个周主要做的事情应该就是，实际的操作去熟悉包括shell命令在内的一些实际工作。另外还大概了解了一下，自己应该如何从事目前的工作，以及找了一些自己觉得的对自己有帮助的书
- shell命令的熟悉：主要方法还是通读.sh文件不会的查和在看一些书籍来补充底层原理知识《linux命令行和shell脚本编程大全》，
1. 查看.sh通过直接读文件夹中的.sh文件，然后在通读一次后发现有某些地方不懂，例如${}的试用其实就是调用某个参数，$1就是使用某个函数等，这种方式解决当前的问题
2. 然后在比较空闲的时候，如晚上回家路上或回家后，看了看书，大概再深层一些的只是是在讲什么。
- 工作方向方面：主要是大概了解**kunit白盒测试**，**devops双环**的内容，Jenkins的作用等

##### 20230612本周收获
前一周基本上都是在搭建各种环境和完成一些权限申请的工作，还有就是初步了解了一下devops开发模式，CI/CD，一些需要用到的工具和平台等，0612这周算正式上手一点点活吧。
- 然后很明显的感觉自己需要学习的地方有：
1. 补充**adb命令，shell指令，cmd指令**的知识了
2. 补充Jenkins关于**pipeline**的学习（流水线的编写，执行情况）
3. 利用C语言完成**白盒测试**的基础知识

- 其实也是学会了一些新的东西的：
1. fastboot：在fastboot模式下，Android设备与计算机建立了低级别通信链接，允许计算机本机对Android系统进行一些操作系统级的操作，如：刷写固件，解锁引导加载程序（bootloader），刷写恢复镜像等。
2. 刷机：通过将固件或系统文件写入设备的存储器中的特定分区来替换当前系统。设备的存储器通常包括系统分区，引导分区，数据分区等。刷机过程中，首先进入引导加载程序（bootloader）模式，该模式允许与设备建立低级别通信连接，然后通过fastboot或类似工具，将新的固件或系统文件写入设备的相应分区。最后，设备重启，并加载新的固件或系统文件。
