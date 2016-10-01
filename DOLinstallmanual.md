DOL框架描述说明  
==

&nbsp; &nbsp; &nbsp; &nbsp; （以下内容描述于2016-10-1）  
&nbsp; &nbsp; &nbsp; &nbsp; DOL也称为Distributed Operation Layer，是一个软件开发框架，用以特化基于Kahn程序网络计算模型的应用仿真软件（就目前所学尚不清楚这是什么），其引擎源于SystemC，DOL提供了基于xml文件的规格格式去描述其实现的多线程系统的可行性与效率分析。  
&nbsp; &nbsp; &nbsp; &nbsp; 目前的框架是这样的：“应用规格”（基于XML 或者是C）经过“功能仿真生成”进行基于工作站的仿真，利用数据抽象与校正提取进行反馈修复，使得该应用规格得以调整得更好。  

DOL安装手册
==

&nbsp; &nbsp; &nbsp; &nbsp; 请按照下列代码进行：
> sudo apt-get update

![image](http://p1.bpimg.com/567571/a554fdbb3e560c2f.jpg)

> sudo apt-get install ant
>

![image](http://i1.piimg.com/567571/2d58c64b5b1396a8.jpg)
![image](http://i1.piimg.com/567571/9ce3b4585e1148c3.jpg)

> sudo apt-get install openjdk-7-jdk
> 

![](http://i1.piimg.com/567571/14ad240b4fd235a7.jpg)

&nbsp; &nbsp; &nbsp; &nbsp; 发现无法获得该数据包，于是我放弃了16.0版本的乌班图了，我改用了14.0版本的乌班图（幸好没有因为操作系统的结课而卸载）。重新继续到该步骤，得到：


![](http://p1.bqimg.com/567571/4300b3d4d64eef05.png)


> sudo apt-get install g++
>

![](http://p1.bqimg.com/567571/7af77f66e8b6afbb.png)


> sudo apt-get install unzip
>

![](http://p1.bqimg.com/567571/dbb457c8e7bb0e53.png)

> sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
>

![](http://p1.bqimg.com/567571/a16ac007decf4961.png)

> sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip
>

![](http://p1.bqimg.com/567571/731e86c8f99a8cb5.png)

&nbsp; &nbsp;  &nbsp; &nbsp; mkdir dol 创建目录dol

![](http://p1.bqimg.com/567571/54a4b36a1f7ec8a8.png)

> unzip dol_ethz.zip -d dol
>

![](http://p1.bqimg.com/567571/fb691b324fd3bf88.png)

> unzip -zxvf systemc-2.3.1.tgz
>

![](http://p1.bqimg.com/567571/49b2126fd31139ce.png)
进入到systemc-2.3.1的目录：

![](http://p1.bqimg.com/567571/a652e08bf27d8e5e.png)
> mkdir objdir
>

&nbsp; &nbsp; &nbsp; &nbsp; 随后cd至该目录  
> ../configure CXX=g++ --disable-update-async-updates
>
![](http://p1.bqimg.com/567571/392472c442d0998e.png)


![](http://p1.bqimg.com/567571/68acfd1f9205d124.png)

&nbsp; &nbsp; &nbsp; &nbsp; 特此说明：上图和ppt提供的一致

> sudo make install (开始编译systemc)
>

![](http://p1.bqimg.com/567571/b84ce0f9256cdba0.png)

> gedit build_zip.xml 以文本编辑模式打开文件
>

![](http://p1.bqimg.com/567571/b84ce0f9256cdba0.png)
&nbsp; &nbsp;  &nbsp; &nbsp; 并且修改：
![](http://p1.bqimg.com/567571/dc4162854b459149.png)
> ant -f build_zip.xml all 利用ant为dol进行编译
>


![](http://p1.bqimg.com/567571/a0bbd8e10a68a47e.png)

&nbsp; &nbsp; &nbsp; &nbsp; 显示build successful。
进入到/jack/dol/build/bin/main之后执行：  
> ant -f runexample.xml -Dnumber=1
>
&nbsp; &nbsp; &nbsp; &nbsp; 通过修改property name = "systemc.lib" value = "YYY"，其中的路径原先设置为64，经过查询发现本人的应该是32，更改之后即完成了测试。最后显示运行成功（不要误会风格的变化，因为我发现最后一张没有及时截图，随后几天我更换了风格）。

![](http://i1.piimg.com/567571/af977f0a21ffc4db.png)

&nbsp; &nbsp; &nbsp; &nbsp; 感谢TA批阅。


——邹文杰 14353439 13763361932 zouwj5@mail2.sysu.edu.cn