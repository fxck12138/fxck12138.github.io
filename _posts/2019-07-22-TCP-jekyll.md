---
layout: post
title: 'TCP/IP学习笔记'
subtitle: 'TCP/IP协议'
date: 2019-07-22
categories: 网络原理
tags: 网络通信
---
> ***什么是TCP/IP？***

TCP/IP 是供已连接因特网的计算机进行通信的通信协议。
TCP/IP 指传输控制协议/网际协议（Transmission Control Protocol / Internet Protocol）。
TCP/IP 定义了电子设备（比如计算机）如何连入因特网，以及数据如何在它们之间传输的标准。
![OSI模型](https://static.runoob.com/images/mix/v2-854e3df8ea850c977c30cb1deb1f64db_r.jpg)

> ***在TCP/IP内部***

在 TCP/IP 中包含一系列用于处理数据通信的协议：
TCP (传输控制协议) - 应用程序之间通信
UDP (用户数据报协议) - 应用程序之间的简单通信
IP (网际协议) - 计算机之间的通信
ICMP (因特网消息控制协议) - 针对错误和状态
DHCP (动态主机配置协议) - 针对动态寻址

>  ***TCP/IP寻址***

TCP/IP 使用 32 个比特或者 4 组 0 到 255 之间的数字来为计算机编址。
TCP/IP 使用 32 个比特来编址。一个计算机字节是 8 比特。所以 TCP/IP 使用了 4 个字节。