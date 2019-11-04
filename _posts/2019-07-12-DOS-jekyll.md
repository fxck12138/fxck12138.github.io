---
layout: post
title: '批量处理脚本'
subtitle: '.dat脚本'
date: 2019-08-07
categories: 编程
tags: 编程 DOS
---
>The darkest hour is that before the dawn.
黎明前的时分是最黑暗的。

    批处理(Batch)，也称为批处理脚本，批处理就是对某对象进行批量的处理，通常被认为是一种简化的脚本语言，它应用于DOS和Windows系统中，是由DOS或者Windows系统内嵌的命令解释器（通常是COMMAND. COM或者CMD.EXE）解释运行。类似于Unix中的Shell脚本。批处理文件具有.bat或者.cmd的扩展名，其最简单的例子，是逐行书写在命令行中会用到的各种命令。[百科解释]


> echo 命令

打开回显或关闭请求回显功能，或显示消息。如果没有任何参数，echo命令将显示当前回显设置。
语法：echo [{on|off}] [message]
Sample：
echo off (关闭回显)
echo hello world (输出hello world)

> @ 命令

表示不显示@后面的命令
Sample：
@echo off (关闭回显，且包含此句命令)

> rem 命令

注释命令，它并不会被执行，只是起一个注释的作用，只有在编辑批处理时才会被看到，主要用于方便修改。
:: 也具有rem的功能
但 :: 和rem还是有区别的，当关闭回显时，rem和::后的内容都不会显示。
但是当打开回显时，rem后的内容会显示出来，然而::后的内容仍然不会显示。
Sample：
rem poll for user input (注释poll for user input说明)

> pause 命令

暂停命令。执行后将显示消息：请按任意键继续. . .
Sample：
echo Hello
pause (输出Hello后暂停批处理程序)

> call 命令

从一个批处理程序调用另一个批处理程序，并且不终止父批处理程序。call命令接受用作调用目标的标签。如果在脚本外使用 Call，它将不会在命令行起作用。
Sample：
call copy.bat （调用同目录拷贝批处理）

> start 命令

调用外部程序，所有的DOS命令和命令行程序都可以由start命令来调用。
Sample：
start calc.exe （打开计算器程序）

> goto 命令

跳转命令。程序指针跳转到指定标签，从标签后的第一条命令开始继续执行批处理程序
语法：goto label
Sample：
:begin
start calc.exe
goto begin (循环跳转至begin标签，打开计算器)

> set 命令

显示、设置或删除变量
显示变量：set 或 set s 前者显示批处理当前已定义的所有变量及其值，后者显示所有以s开头的变量及值。

设置和调用变量：例如set aa=abcd，就是把aa定义为abcd。如果要调用这个变量，就把aa两边加上个百分号。
Sample：
set name=Application1 (设置变量name的值为Application1)
echo %name%
pause

删除变量：set name= 此句命令即可删除变量name。若变量name已被定义，则删除变量name；若name尚未定义，则此句命令无实质意义。
需要说明的是，批处理中的变量是不区分类型的，不需要像其他高级语言语言中的变量区分int、float、char等。比如执行set name=345后，变量name的值既可以被视为数字345，也可以被视为字符串345。

> 文件夹管理

cd 显示当前目录名或改变当前目录。
md 创建目录。
rd 删除一个目录。
copy 复制文件和目录树。

> 文件管理

copy 将一份或多份文件复制到另一个位置。
del 删除一个或数个文件。
move 移动文件并重命名文件和目录。（Windows XP Home Edition中没有)
ren重命名文件。
replace 替换文件。

> 重定向符号>与>>

将输出信息重定向到指定的设备或文件。系统默认输出到显示器。
符号>与>>区别为：>表示覆盖输出至设备文件，>>表示追加到设备文件末尾，不删除
Sample：
echo 名称是Application1>name.txt
(把“名称是Application1”这段信息输出到name.txt文件中)

> 重定向符号<

将输入信息来源重定向为指定的设备或文件。系统默认从显示器读取输入信息。
Sample：
set /p name=<name.txt (从naem.txt文件中读取值赋给变量name)

> 管道符号 |
将管道符号前面命令的输出结果重定向输出到管道符号后面的命令中去，作为后面命令的输入。
格式：command_1|command_2

批处理的功能完全取决于你使用的命令，而批处理命令又分别内部命令和外部命令以及一些第三方工具。想系统的了解命令类型，可以参阅百科资料