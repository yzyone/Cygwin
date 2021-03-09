
# Cygwin下安装其他软件 #

一、cygwin下安装其他软件的方法
1.通过cygwin客户端安装必须的软件支持包wget tar gawk bzip2

    cd C:\cygwin64
    setup-x86_64 -q -P wget,tar,qawk,bzip2,subversion,vim

注意:此安装客户端位setupX86_64.exe,你需要到cygwin官网自己下载exe文件,安装,然后拷贝到相关安装后的目录;

2.安装apt-cyg

    lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg
	install apt-cyg /bin
    chmod.exe +x /bin/apt-cyg

此命令表示将http://rawgit.com/transcode-open/apt-cyg/master/apt-cyg中的apt-cyg拷贝到本地/bin目录下;

然后赋予可执行权限;

3.替换apt-cyg镜像源

    apt-cyg -m http://mirrors.163.com/cygwin/

4.更新镜像源

    apt-cyg update

5.安装其他软件

这里的apt-cyg基本和Ubuntu中的apt-get的使用方法是一致的;


比如安装mysql server的命令如下:

    apt-cyg install mysql-server

6、其他说明

*****注：安装apt-cyg 的另一种方法：  

apt-cyg is a simple script. To install:

    lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg
    install apt-cyg /bin

备注： 此处选择中国网站 ，否则很慢哦


为了获得最快的下载速度，我们首先在列表中寻找Cygwin中国镜像的地址：http://www.cygwin.cn，如果找到就选中这个地址；如果找不到这个地址，就在下面手动输入中国镜像的地址：http://www.cygwin.cn/pub/，再点击“Add”，然后再在列表中选中。选择完成后，点击“下一步”。

参考链接 ：

https://blog.csdn.net/huitoukest/article/details/50730259 

http://www.programarts.com/cfree_ch/doc/help/UsingCF/CompilerSupport/Cygwin/Cygwin1.htm

————————————————

版权声明：本文为CSDN博主「星月夜语」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。

原文链接：https://blog.csdn.net/ljh618625/article/details/94641612