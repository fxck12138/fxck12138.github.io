---
layout: post
title: 'DOS命令'
subtitle: 'DOS'
date: 2019-08-07
categories: 编程
tags: 编程 DOS
---
1.DIR命令

作用:显示磁盘目录所包含的内容

格式:DIR[文件名][选项]

例如:

DIR D:\JDK

查询D盘下的JDK文件夹下的未隐藏文件

DIR D:\JDK /A

查询D盘下的JDK文件夹下的所有文件

DIR D:\JDK /S

查询D盘下的JDK文件夹下的包含子文件夹下的所有文件

DIR D:\JDK /B

查询D盘下的JDK文件夹下的所有文件的名字

2.Ping(因特网包探索器)命令

作用:与ip相关并检测两台计算机之间的网络是否连通

例如:

ping 127.0.0.1

显示本机网卡是否正常使用,必需为127.0.0.1(127.0.0.1是回送地址，指本地机，一般用来测试使用。回送地址（127.x.x.x）是本机回送地址（Loopback Address），即主机IP堆栈内部的IP地址，主要用于网络软件测试以及本地机进程间通信，无论什么程序，一旦使用回送地址发送数据，协议软件立即返回，不进行任何网络传输),当显示"来自..的回复"的时候,正常,若显示请求超时则本机网卡有问题.

ping 192.168.1.1

显示是否成功接入路由器,ip必须为192.168.1.1,因为192.168.1.1属于IP地址的C类地址，属于保留IP，专门用于路由器设置。

ping www.baidu.com

显示本机是否接入Internet,若显示超时,则未连入Internet

ping -a ip地址

将ip地址解析为计算机NetBIOS名

ping -n count ip地址

发送count指定的映带协议的数据包数,例如ping - n 5 112.74.127.218

ping -t ip地址

一直ping制定远程计算机,直到键盘按下[Ctrl+C]中断

3.nbtstat命令:

作用:用于查看基于TCP/IP协议的NetBIOS协议的统计资料,本地计算机和远程计算机的NetBIOS名称表 和名称缓存

格式:nbtstat[-a RemoteName] [-A IPAddress] [-c] [-n] [-r] [-R] [-RR] [-s] [-S] [Interval]

例如:

nbtstat -a remotename

显示远程计算机的 NetBIOS 名称表，其中，RemoteName 是远程计算机的 NetBIOS 计算机名称。NetBIOS 名称表是与运行在该计算机上的应用程序相对应的 NetBIOS 名称列表。

nbtstat -A IPAddress

显示远程计算机的 NetBIOS 名称表，其名称由远程计算机的 IP 地址指定（以小数点分隔）。

nbtstat -c

显示 NetBIOS 名称缓存内容、NetBIOS 名称表及其解析的各个地址。

nbtstat -n

显示本地计算机的 NetBIOS 名称表。Registered 的状态表明该名称是通过广播还是 WINS 服务器注册的。

nbtstat -r

显示 NetBIOS 名称解析统计资料。在配置为使用 WINS 且运行 Windows XP 或 Windows Server 2003 操作系统的计算机上，该参数将返回已通过广播和 WINS 解析和注册的名称号码。

nbtstat -R

清除 NetBIOS 名称缓存的内容并从 Lmhosts 文件中重新加载带有 #PRE 标记的项目。

nbtstat -RR

释放并刷新通过 WINS 服务器注册的本地计算机的 NetBIOS 名称。

nbtstat -s

显示 NetBIOS 客户端和服务器会话，并试图将目标 IP 地址转化为名称。

nbtstat -S

显示 NetBIOS 客户端和服务器会话，只通过 IP 地址列出远程计算机。

nbtstat Interval

重新显示选择的统计资料，可以在每个显示内容之间中断 Interval 中指定的秒数。按 Ctrl+C 停止重新显示统计信息。如果省略该参数，netstat 将只显示一次当前的配置信息。

nbtstat /?

在命令提示符下显示帮助.

4.netstat命令

作用:监控TCP/IP网络的命令

格式:netstat [-a][-e][-n][-o][-p Protocol][-r][-s][Interval]

例如:

netstat -a

本选项显示一个所有的有效连接信息列表，包括已建立的连接（ESTABLISHED），也包括监听连接请求（LISTENING）的那些连接。

netstat -b

该参数可显示在创建网络连接和侦听端口时所涉及的可执行程序

netstat -s

本选项能够按照各个协议分别显示其统计数据。如果你的应用程序（如Web浏览器）运行速度比较慢，或者不能显示Web页之类的数据，那么你就可以用本选项来查看一下所显示的信息。你需要仔细查看统计数据的各行，找到出错的关键字，进而确定问题所在。

netstat -e

本选项用于显示关于以太网的统计数据，它列出的项目包括传送数据报的总字节数、错误数、删除数，包括发送和接收量（如发送和接收的字节数、数据包数），或有广播的数量。可以用来统计一些基本的网络流量。

netstat -r

本选项可以显示关于路由表的信息，类似于后面所讲使用routeprint命令时看到的信息。除了显示有效路由外，还显示当前有效的连接。

netstat -n

显示所有已建立的有效连接

netstat -p

显示协议名查看某协议使用情况

5.net命令

作用:基于网络的命令,功能强大,可以管理网络环境,服务,用户等本地及远程信息

例如:

net use \\ip\ipc$ " " /user:" "

建立IPC空链接

net use \\ip\ipc$ "密码" /user:"用户名"

建立IPC非空链接

net use h: \\ip\c$ "密码" /user:"用户名"

直接登陆后映射对方C：到本地为H:

net use h: \\ip\c$

登陆后映射对方C：到本地为H:

net use \\ip\ipc$ /del

删除IPC链接

net use h: /del

删除映射对方到本地的为H:的映射

net user 用户名　密码　/add

建立用户

net user guest /active:yes

激活guest用户

net user

看有哪些用户

net user 帐户名

查看帐户的属性

net localgroup administrators 用户名 /add

把“用户”添加到管理员中使其具有管理员权限,注意：administrator后加s用复数

net start \

查看开启了哪些服务

net start 服务名　

开启服务；(如:net start telnet， net start schedule)

net stop

服务名 停止某服务

net time \\目标ip

查看对方时间

net time \\目标ip /set

设置本地计算机时间与“目标IP”主机的时间同步,加上参数/yes可取消确认信息

net view

看本地局域网内开启了哪些共享

net view \\ip

查看对方局域网内开启了哪些共享

net config

显示系统网络设置

net logoff

断开连接的共享

net pause

服务名 暂停某服务

net share

查看本地开启的共享

net share ipc$

开启ipc$共享

net share ipc$ /del

删除ipc$共享

net user guest 12345

用guest用户登陆后用将密码改为12345

net password 密码

更改系统登陆密码