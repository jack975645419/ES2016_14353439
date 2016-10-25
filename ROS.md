说明：本文件系邹文杰 14353439(Student ID) 13763361932zouwj5@mail2.sysu.edu.cn 中山大学数据科学与计算机学院移动信息工程专业学生大学三年级秋季学期《嵌入式导论》课作业报告。
--
&nbsp; &nbsp; Main是指权威开源；
Universe是指社区维护的开源
Restricted是驱动程序；
Multiverse是由于版权而受限的软件

&nbsp; &nbsp; 运行指定的命令得到：


> root@14353439_wenjie:/home/jack# sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list
> ^C
root@14353439_wenjie:/home/jack# sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
root@14353439_wenjie:/home/jack# sudo sh -c '. /etc/lsb-release && echo "deb http://mirror.sysu.edu.cn/ros/ubuntu/ $DISTRIB_CODENAME main" > /etc/apt/sources.list.d/ros-latest.list'
root@14353439_wenjie:/home/jack# sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
Executing: gpg --ignore-time-conflict --no-options --no-default-keyring --homedir /tmp/tmp.Du7ANV5eq5 --no-auto-check-trustdb --trust-model always --keyring /etc/apt/trusted.gpg --primary-keyring /etc/apt/trusted.gpg --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
gpg: 下载密钥‘B01FA116’，从 hkp 服务器 ha.pool.sks-keyservers.net
gpg: 密钥 B01FA116：公钥“ROS Builder <rosbuild@ros.org>”已导入
gpg: 合计被处理的数量：1
gpg:               已导入：1

运行结果如下：
![](http://p1.bpimg.com/567571/96a2902bc8ecb6a0.png)
![](http://p1.bpimg.com/567571/6b04c206b9ab89ba.png)
![](http://p1.bpimg.com/567571/be20dee712306be6.png)

【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】


——邹文杰 14353439 13763361932 zouwj5@mail2.sysu.edu.cn
