---
layout: post
title: 'Java学习笔记菜鸟入门到精通第一练'
subtitle: '学习使我快乐'
date: 2020-01-11
categories: java学习
tags: java
---
#### 什么是Java？
> Java是由SUN公司于1995年5月推出，现在依旧很火的完全面向对象的程序设计语言。
SUN公司将Java划分为三个技术平台，它们分别是JavaSE、JavaEE和JavaME。
#### Java SE （Java Platform Standard Edition）标准版
  JavaSE是为开发普通桌面和商务应用程序提供的解决方案。 JavaEE和JavaME都是从JavaSE的基础上发展而来的，它是三个平台中最核心的部分，包括了Java最核心的类库，如集合、IO、数据库连接以及网络编程等。

#### Java EE (Java Platform Enterprise Edition) 企业版
  JavaEE是为开发企业级应用程序提供的解决方案。JavaEE可被看作一个技术平台，用于开发、装配以及部署企业级应用程序。其中主要包括Servlet、JSP 、JavaBean 、JDBC、EJB、Web Service等技术。
#### Java ME(Java Platform Micro Edition) 小型版
  JavaME是为开发电子消费产品和嵌入式设备提供的解决方案，主要用于小型数字电子设备软件程序的开发。此外，提供了HTTP等高级Internet协议。

#### 有什么特点？
> 1.简单性

> 2.面向对象型

> 3.安全性

> 4.跨平台性

> 5.支持多线程

#### Java环境搭建
#### 1.安装JDK。
JDK安装目录下的子目录介绍。

1.bin目录：该目录用于存放一些可执行程序，如javac.exe（Java编译器）、java.exe（Java运行工具）、jar.exe（打包工具）和javadoc.exe（文档生成工具）等。


2.db目录：db目录是一个小型的数据库。从JDK 6.0开始，Java中引入了一个新的成员JavaDB，这是一个纯 Java 实现、开源的数据库管理系统。这个数据库不仅很轻便，而且支持JDBC 4.0所有的规范，在学习JDBC时，不再需要额外地安装一个数据库软件，选择直接使用JavaDB即可。


3.jre目录：“jre”是Java Runtime Environment的缩写，意为Java程序运行时环境。此目录是Java运行时环境的根目录，它包含Java虚拟机，运行时的类包、Java应用启动器以及一个bin目录，但不包含开发环境中的开发工具。


4.include目录：由于JDK是通过C和C++实现的，因此在启动时需要引入一些C语言的头文件，该目录就是用于存放这些头文件的。


5.lib目录：lib是library的缩写，意为Java类库或库文件，是开发工具使用的归档包文件。


6.src.zip文件：src.zip为src文件夹的压缩文件，src中放置的是JDK核心类的源代码，通过该文件可以查看Java基础类的源代码。


javac.exe是Java编译器工具，它可以将编写好的Java文件编译成Java字节码文件（可执行的Java程序）。Java源文件的扩展名为.java，如“HelloWorld.java”。编译后生成对应的Java字节码文件，文件的扩展名为.class，如“HelloWorld.class”。


java.exe是Java运行工具，它会启动一个Java虚拟机（JVM）进程，Java虚拟机相当于一个虚拟的操作系统，它专门负责运行由Java编译器生成的字节码文件（.class文件）。


#### 2.环境配置
（1）path环境变量
         path环境变量是系统环境变量中的一种，它用于保存一系列的路径，每个路径之间以分号分隔。当在命令行窗口运行一个可执行文件时，操作系统首先会在当前目录下查找是否存在该文件，如果不存在会继续在path环境变量中定义的路径下寻找这个文件，如果仍未找到，系统会报错。

（2）classpath环境变量
         classpath环境变量也用于保存一系列路径，它和path环境变量的查看与配置的方式完全相同。当Java虚拟机需要运行一个类时，会在classpath环境变量中所定义的路径下寻找所需的class文件。

1.点击 系统变量 下的 新建 按钮，然后输入
变量名：JAVA_HOME
变量值：JDK安装路径

2.在 系统变量 中找到 Path
点击弹出框的 新建 按钮，输入
%JAVA_HOME%\bin
%JAVA_HOME%\jre\bin

3.点击新建系统变量，输入
变量名：CLASSPATH
变量值：.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar

### 第一个Java程序
```java
class HelloWorld {
	public static void main(String[] args) {
		System.out.println(“Hello World!");
	}
}
```


1.class是一个关键字，它用于定义一个类。在Java中，类就相当于一个程序，所有的代码都需要在类中书写。


2.HelloWorld是类的名称，简称类名。class关键字与类名之间需要用空格、制表符、换行符等任意的空白字符进行分隔。类名之后要写一对大括号，它定义了当前这个类的管辖范围。


3.“public static void main(String [] args){}”定义了一个main()方法，该方法是Java程序的执行入口，程序将从main()方法所属大括号内的代码开始执行。
在


4.main()方法中编写了一条执行语句“System.out.println(“Hello World！");”，它的作用是打印一段文本信息，执行完这条语句会在命令行窗口中打印“Hello World！”。




