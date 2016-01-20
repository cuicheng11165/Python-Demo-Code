

# Python


## Python中文编码问题

* Python中默认的编码格式是 ASCII 格式，在没修改编码格式时无法正确打印汉字，所以在读取中文时会报错。
解决方法为只要在文件开头加入 # -*- coding: UTF-8 -*- 或者 #coding=utf-8 就行了。

## Python标识符

* 在python里，标识符有字母、数字、下划线组成。
* 在python中，所有标识符可以包括英文、数字以及下划线（_），但不能以数字开头。
* python中的标识符是区分大小写的。
* 以下划线开头的标识符是有特殊意义的。以单下划线开头（_foo）的代表不能直接访问的类属性，需通过类提供的接口进行访问，不能用"from xxx import *"而导入；
* 以双下划线开头的（__foo）代表类的私有成员；以双下划线开头和结尾的（__foo__）代表python里特殊方法专用的标识，如__init__（）代表类的构造函数。

## 行和缩进
* 缩进用来控制流程，必须严格执行

## 多行语句

* Python中新行代表语句结束，可以用 \来把一条语句分为多行显示
total = item_one + \
        item_two + \
        item_three
		
* 语句中包含[], {} 或 () 括号就不需要使用多行连接符。如下实例：
days = ['Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday']
		
## Python引号		

* 分为单引号，双引号，三引号

## 注释

* 以#开头
## Python空行

* 函数之间或者类的方法之间用空行分隔，表示一段新的代码开始。类和函数入口之间也用一空行分隔，以突出如空开始。
空行和缩进不同。不会导致解释错误。

## 等待用户输入

* raw_input("\n\nPress the enter key to exit.")

## 同一行显示多条语句

* 用;实现

## 代码块组成代码组

* 缩进相同的一组语句构成一个代码块，我们称为代码组。像if while def class这样的复合语句，首航以关键字开始，以冒号结束，该行之后的一行或者多行代码构成代码组

## 命令行参数

* 可以查看一下基本信息 python -h

## 变量类型

* 标准数据类型
Numbers（数字）
String（字符串）
List（列表）
Tuple（元组）
Dictionary（字典）

* 用del来删除对象的引用，  del var1，var2

## 字符串

* 截取子串用[start,end]来实现。如  s='ilovepython'  s[1:5]的结果是love,具体例子见 string operation demo.py

## List（列表）

List（列表） 是 Python 中使用最频繁的数据类型。
列表可以完成大多数集合类的数据结构实现。它支持字符，数字，字符串甚至可以包含列表（所谓嵌套）。
列表用[ ]标识。是python最通用的复合数据类型。看这段代码就明白。
列表中的值得分割也可以用到变量[头下标:尾下标]，就可以截取相应的列表，从左到右索引默认0开始的，从右到左索引默认-1开始，下标可以为空表示取到头或尾。
加号（+）是列表连接运算符，星号（*）是重复操作。如下 list operation demo.py

## Tuple（元组）

元组是另一个数据类型，类似于List（列表）。元组用"()"标识。内部元素用逗号隔开。但是元素不能二次赋值，相当于只读列表。和list的主要区别在于使用 小括号 () 而不是中括号[] 

## Dictionary（字典）

* 字典用大括号标识，使用方法见 dictionary operation demo.py

## 运算符

* //表示取整除

## 成员运算符 

* in	如果在指定的序列中找到值返回True，否则返回False。	x 在 y序列中 , 如果x在y序列中返回True。
* not in	如果在指定的序列中没有找到值返回True，否则返回False。	x 不在 y序列中 , 如果x不在y序列中返回True。

## 身份运算符

* is	    is是判断两个标识符是不是引用自一个对象	x is y, 如果 id(x) 等于 id(y) , is 返回结果 1
* is not	is not是判断两个标识符是不是引用自不同对象	x is not y, 如果 id(x) 不等于 id(y). is not 返回结果 1

## 循环

* 需要用分号在关键字后
* Python中的for用法类似于c#中的foreach
* 注意缩进
* pass用来占位，不执行任何操作

## Python 函数

* Python中的自变量都是引用传递

### 参数
参数类型：
* 必备参数
* 命名参数
* 缺省参数
* 不定长参数

具体参见method parameter demo.py

### lambda

## 变量作用域

*在函数外是全局变量，函数内的局部变量

## 文件的IO
[File IO](http://www.runoob.com/python/python-files-io.html)

## 异常处理
[Exception handling](http://www.runoob.com/python/python-exceptions.html)

# 面向对象

## Python访问属性

* getattr(obj, name[, default]) : 访问对象的属性。
* hasattr(obj,name) : 检查是否存在一个属性。
* setattr(obj,name,value) : 设置一个属性。如果属性不存在，会创建一个新属性。
* delattr(obj, name) : 删除属性。

## Python 内置类属性

* 参见 buildin method

## 类的继承

* 在继承中基类的构造（__init__()方法）不会被自动调用，它需要在其派生类的构造中亲自专门调用。
* 在调用基类的方法时，需要加上基类的类名前缀，且需要带上self参数变量。区别于在类中调用普通函数时并不需要带上self参数
* Python总是首先查找对应类型的方法，如果它不能在派生类中找到对应的方法，它才开始到基类中逐个查找。（先在本类中查找调用的方法，找不到才去基类中找）

## 类属性与方法
### 私有属性
* __private_attrs：两个下划线开头，声明该属性为私有，不能在类地外部被使用或直接访问。在类内部的方法中使用时 self.__private_attrs
### 类的方法
* 在类地内部，使用def关键字可以为类定义一个方法，与一般函数定义不同，类方法必须包含参数self,且为第一个参数
### 类的私有方法
* __private_method：两个下划线开头，声明该方法为私有方法，不能在类地外部调用。在类的内部调用 self.__private_methods
















