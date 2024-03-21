# Python语法

## 编码

Python中默认情况下使用的都是 **UTF-8** 编码,其中所有的字符串都是 Unicode 字符.

以下是指定编码的语句,你需要把它写在开头.

```python
# -*- coding: cp-1252 -*-
```



## 标识符

标识符就是你给变量取得"名字",例如你有一个变量,你需要给它取名字,那你得尊重一下的规则.

- 第一个字符必须是字母表中字母或下划线 **_** 。
- 标识符的其他的部分由字母、数字和下划线组成。如果是 `_name123$` 是不行的
- 标识符对大小写敏感。Name和name不是同一个东西,name和NAme也不是同一个东西,以此类推.



## 保留字

Python中有很多名字是被用在了自己的库上的,例如False None等等,这些在很多程序中是要用到的,你不能将它们作为变量的名字.

```python
import keyword
keyword.kwlist
['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```



## 注释

Python中的注释用 `#` 符号.可以写在代码后面也可以单独一行 还有 `'''` 和` """`：

```python
# 这是一个注释
print('hello') # 这也是一个注释,这段代码的作用是输出一个hello

'''
这里是一个多行注释
换行后也不需要#符号
只要不在单引号外
'''

"""
双引号的多行注释
也是同理
"""
```



## 行和缩进

Python中和C或者Java等语言不同的地方就是很少使用 `{}` 作为代码块.而是用行和缩进

例如

```python
if name='rachel':
  print('you are rachel.')
else:
  print('i dont know who you are.')
```

其中,如果缩进不一致的话,会导致代码出现问题,本质的原因是因为编译器根据缩进辨别代码块.如果你的缩进不统一的话,会认为部分代码不属于同一代码块.

例如

```python
if name='rachel':
  print('you are rachel.')
else:
  print('i dont know who you are.')
 print('can you tell me') # 这里会报错
```

另外,在部分功能不够强大的代码编辑器中,如果同时使用了Tab和空格进行缩进,也会报错.



## 多行语句

```python
total = 1 + 2 + 3 + \
				4 + 5 + \
				6
# 请使用 \ 符号进行换行
```



## 导包

在 python 用 **import** 或者 **from...import** 来导入相应的模块。

将整个模块(somemodule)导入，格式为： **import somemodule**

从某个模块中导入某个函数,格式为： **from somemodule import somefunction**

从某个模块中导入多个函数,格式为： **from somemodule import firstfunc, secondfunc, thirdfunc**

将某个模块中的全部函数导入，格式为： **from somemodule import \***

```python
import sys
# 导入sys这个模块
from sys import argv
# 从sys导入argv这个方法
```



# 数据类型

## 基本数据类型

Python中的`=`用于给变量赋值.

**变量就是变量，它没有类型，我们所说的"类型"是变量所指的内存中对象的类型。**