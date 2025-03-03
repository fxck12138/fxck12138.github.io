---
layout: post
title: 'Python3学习'
subtitle: 'Python3'
date: 2019-07-20
categories: 编程
tags: Python3
---
![](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1179406842,2804315616&fm=26&gp=0.jpg)
  
> **标识符**

1.第一个字符必须是字母表中字母或下划线 _ 。
2.标识符的其他的部分由字母、数字和下划线组成。
3.标识符对大小写敏感。
在 Python 3 中，非 ASCII 标识符也是允许的了。
> **注释**

Python中单行注释以 # 开头
多行注释可以用多个 # 号，还有 ''' 和 """

```python
#!/usr/bin/python3 

# 第一个注释
# 第二个注释 
''' 
第三注释 
第四注释
 '''
 """
 第五注释
 第六注释
 """ 
print ("Hello, Python!")
```
 
> **行与缩进**

python最具特色的就是使用缩进来表示代码块，不需要使用大括号 {} 。
缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数。

> **多行语句**

Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠(\)来实现多行语句
在 [], {}, 或 () 中的多行语句，不需要使用反斜杠(\)

> **数字(Number)类型**

python中数字有四种类型：整数、布尔型、浮点数和复数。
1.int (整数), 如 1, 只有一种整数类型 int，表示为长整型，没有 python2 中的 Long。
2.bool (布尔), 如 True。
3.float (浮点数), 如 1.23、3E-2
4.complex (复数), 如 1 + 2j、 1.1 + 2.2j

> **字符串(String)**

python中单引号和双引号使用完全相同。
使用三引号('''或""")可以指定一个多行字符串。
转义符 '\'
反斜杠可以用来转义，使用r可以让反斜杠不发生转义。。 如 r"this is a line with \n" 则\n会显示，并不是换行。
按字面意义级联字符串，如"this " "is " "string"会被自动转换为this is string。
字符串可以用 + 运算符连接在一起，用 * 运算符重复。
Python 中的字符串有两种索引方式，从左往右以 0 开始，从右往左以 -1 开始。
Python中的字符串不能改变。
Python 没有单独的字符类型，一个字符就是长度为 1 的字符串。
字符串的截取的语法格式如下：变量[头下标:尾下标:步长]
word = '字符串' 
sentence = "这是一个句子。" 
paragraph = """这是一个段落， 
可以由多行组成"""

> **空行**

函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。类和函数入口之间也用一行空行分隔，以突出函数入口的开始。
空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。
记住：空行也是程序代码的一部分。
 
