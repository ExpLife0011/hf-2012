NetWall防火墙简易版：netwall
============================================================================
运行环境：	Windows 2000  10M/100M的以太网  一块或多块网卡
作者：		陈尧军
发行时间：	2003-03-10
Email：		info@netwall.cn
网址：		http://www.netwall.cn
版权所有：	耐威技术


目录和部分文件说明
============================================================================
[bin]   编译好的二进制文件和驱动安装文件
    netwall.inf      驱动安装程序
    netwall_m.inf    驱动安装程序
    netwall.sys      驱动程序
    NetWall_d.dll    动态链接库
    NetWall_d.exe    操作控制程序
[doc]   文档目录    
[dll]   动态链接库源代码
[exe]   用户操作界面源代码
[inc]   公共头文件
[sys]   驱动程序源代码（在这个发行包中不存在，如果您感兴趣，请发邮件到
        mailto: info@netwall.cn, 我们将尽快将源码发送给您。）


注意事项
===========================================================================
系统内核（netwall.sys）是一个NDIS中间层驱动程序，用它来截获网络封包，
在安装前，系统中最好不要装有第三方NDIS中间层驱动程序。另外，这属于开
放源代码，作者不提供任何保障，如果对您的机器造成任何损害，我们不负任
何责任。如果您在安装过程中或在使用过程中有什么问题或任何疑问，请发邮
件到: info@netwall.cn, 我们将尽快解决。


驱动安装方法：	
===========================================================================
1．	打开网卡连接属性面板
2．	按“安装”按钮，弹出“选择网络组件类型”对话框
3．	选中“服务”后按“添加按钮”，弹出“选择网络服务”对话框
4．	按“从磁盘安装” 按钮，弹出“从磁盘安装”对话框
5．	按“浏览”按钮，弹出“查找文件”对话框
6．	通过对话框找到压缩包释放后bin目录下的netwall.inf文件，
	按“打开”按钮后弹出“选择网络服务”对话框
7．	按“确定”后系统便会自动复制所需文件，安装完成后回到第一步的界面，
	上面会多出一个“NetWall Driver”的服务，这就是NetWall防火墙。
8．	这个发行包只包含调试版本，您可以使用drivermonitor.exe或dbgview(发行
    包没有提供)获取驱动程序输出的调试信息。	
9． 卸载。在第一步的界面上选中“NetWall Driver”后按“卸载”按钮
	完成NetWall的卸载。


使用方法：
===========================================================================
1.  按以上方法安装驱动。
2.  运行NetWall_d.exe，这是用户界面操作程序，可以设置规则，如果打开日志
    记录功能，系统将会记录所有的网络流量，日志文件放在系统目录下，文件
    名为NetWall.log。在操作控制程序中可以装载显示日志信息。您可以随意
    控制日志的装载和显示。
    