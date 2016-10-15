DOL实验-运行并修改实例
==
说明：本文件系邹文杰 14353439(Student ID) 13763361932 zouwj5@mail2.sysu.edu.cn 中山大学数据科学与计算机学院移动信息工程专业学生大学三年级秋季学期《嵌入式导论》课作业报告。
--
&nbsp; &nbsp; 实验之初，小生先总结部分重要的知识：
dol examples才是真正的源代码，而build里面的是编译运行的代码（在随后的重新修改后，可以删除build中的文件以表示clean）。XML文件是各个组件之间的管理信息，而src文件夹则放置了重要的文件。process是模块，channel是信息通道，connection是模块和信息之间的连接处，一头连接模块，另一头连接channel。

&nbsp; &nbsp; .c和.h文件都是src文件夹里面的文件类型，是实现的模块，常常包含ini和fire文件。xml描述连接性。

&nbsp; &nbsp; 在~dol build bin main中使用ant -f runexample.xml -Dnumber=x可以运行第x个例子。重要的声明：generator（buildbinmainexamplex的src文件夹下）声明了主要动作。里面有fire和ini。

【1】例子1的修改
--
&nbsp; &nbsp; 
实验代码的修改：在example1的square.c代码中，修改如下：

![](http://i1.piimg.com/567571/208f82a0f1f0aea5.png)

&nbsp; &nbsp; 将平方修改为了立方。

&nbsp; &nbsp; 在ex1中， generator还有一个output，consumer还有一个input，square还有一个input和一个output。C1 channel以fifo形式附有一个input和一个output，C2 channel同样如此。gc connection的ori（连接pro的端口）设置为generator，port（连接channel）连接C1，以此类推。

&nbsp; &nbsp; 运行结果如下：

![](http://i1.piimg.com/567571/c17e5f12ede001f7.png)


&nbsp; &nbsp; 由于例子1没有改动，因而dot图像不变化，此处不贴出。

【2】例子2的修改
--
&nbsp; &nbsp; 在ex2中，修改xml（位于dol examples example2下）代码中的原先的模块数目value=“3”修改为“2”，如下图所示：


![](http://i1.piimg.com/567571/e52bf31cbb478fb5.png)


&nbsp; &nbsp; 运行得到如下结果（3次平方变成了2次平方）：


![](http://i1.piimg.com/567571/a5a8741c69ca212e.png)

&nbsp; &nbsp; 查看dot图像：


![](http://i1.piimg.com/567571/7389b3cf04c0e73d.png)


&nbsp; &nbsp; 实验感想：我感觉ddl未设置真的是一种享受，没有ddl逼迫然后做起作业来感觉像是自己掌握了主动权，清闲地自主地学习模式有利于严谨地掌握知识要点。因为有更多的精力去关注细节而非收到繁文缛节的分心。小生本次实验课学到的内容是范例的修改，起初遇到了一些问题，比如说文件夹的目录总是弄错（非常头疼）。经过询问助教之后，耐心听从助教指导，终于解决了这些问题。一直坐在电脑面前敲写代码并不是十分舒适的事情，耐性很容易被消磨，加之在实验的过程中会遇到许多的小挫折，大概是因为不熟练的缘故。古语有云：“有志者，事竟成。”只要我们付出了努力，就会取得成功。感激助教悉心教导，希望助教能够兼顾学业，在帮助我们之余不要忘了关心自己的身体。

&nbsp; &nbsp; 邹文杰 14353439 13763361932 zouwj5@mail2.sysu.edu.cn

&nbsp; &nbsp; 【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】【原创声明】