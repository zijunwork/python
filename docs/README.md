### 第一章：愉快的开始

开始之前，熟悉一下常用的cmd命令

#### 1.0、 常用的cmd命令

+ `dir` 查看当前文件夹下的文件及文件夹
  + `d-----`表示文件夹
  + `-a----`表示文件
+ `cd` 切换目录/文件
+ `cd file` 进入当前文件夹下的file文件夹
+ `cd fold1/fold2` 或者 `cd fold1\fold2`进入多层文件夹
+ `cd ..` 进入上一层文件夹
+ `cd ../folder` 进入上一层文件夹中的folder文件夹
+ `mkdir myfolder` 或 `md myfolder` 在当前目录下创建myfolder文件夹
+ `type nul > my.txt` 创建空白的my.txt文件
+ `echo content > my.txt` 创建内容是content的my.txt文件
+ `type test1.py` 查看在当前目录下的额test1.py文件内容，把内容打印到cmd中
+ `test1.py` 直接输入文件名，用默认程序打开此文件（相当于鼠标双击）
+ `ren oldname newname` 重命名
+ `del test1.py` 删除文件
+ `del myfolder` 删除myfolder文件夹中所有文件（文件夹保留）
+ `rd myfolder` 或者 `rmdir myfolder` 删除myfolder文件夹
+ `tree myfolder` 将myfolder文件夹下的所有文件夹展示成树状结构（不展示文件）
+ `tree myfolder /f` 展示文件夹及文件树状结构
+ `tree myfolder /f > my.txt` 将结果输出到my.txt文件中（新建的文件）
+ cls 清屏

#### 1.1、Python的安装

安装Python非常容易，在官网（[https://www.python.org/](https://www.python.org/)）找到Download字样，点击Latest:Phton 3.x.x 下载 Window x86-64 exeecutable installer 安装包并选择默认安装即可。

![1_1_001](./_images/1_001.jpg)

![1_1_002](./_images/1_002.jpg)

#### 1.2、shell使用Python

打开cmd/power shell命令窗口，键入`python` 便会进入Python以`>>>`开始的工作环境。

`>>>`提示符的含义是： Python已经准备好了，等你输入指令了！

然后键入

```python
print("I love SZ")
```

即可打印数据。需要注意的是，Python3.x 版本并不支持2.x版本的语法！

```python
print("I love SZ") # Python 3.x的语法
print "I love SZ" # Python 2.x的语法 不兼容
```



![1_1_003](./_images/1_003.jpg)

![](./_images/1_004.jpg)

#### 1.3、Python的其他尝试

Python可以做数字的加减乘除，字符串的连接，重复等普通语言都可以做的操作，不足为奇。

![](./_images/1_005.jpg)



### 第二章：用Python设计一个小游戏

#### 2.1、第一个小游戏

```python
# test1.py
temp = input("不妨猜下我现在心里想得是哪个数字：")
guess = int(temp)
if guess == 8:
    print("你是我心里的蛔虫吗？！")
    print("哼，即使你猜对了也没有奖励！")
else:
    print("猜错啦，我心里现在想的数字是8！")
print('游戏结束，不玩啦^_^')
```

cmd中切换到test1.py所在的目录，然后键入`test1.py`运行此python文件，即可开始游戏。

从上面可以看到python声明变量是不需要任何事先声明的。

![](./_images/2_001.jpg)

#### 2.2、缩进

python中采用缩进取代大括号，缩进与冒号（:）快速构成和判断python的语法。

#### 2.3、BIF

BIF(Built-in Functions),内置函数的意思。内置函数就是此语言自带的一些函数，只需要直接调用即可实现。例如：

+ `print()`就是一个内置函数，功能就是‘打印到屏幕’。
+ `input()` 也是一个BIF，作用是接受用户输入并将其返回
+ `dir(__builtins__)` 可以看到Python所有的BIF
+ `help()` 这个BIF用于显示BIF的功能描述

![](./_images/2_002.jpg)

![](./_images/2_003.jpg)

#### 2.4、Test-001

> 编写程序：hello.py , 要求用户输入姓名并打印“你好，姓名！”

```python
# hello.py
temp = input('请输入您的姓名：')
if temp != "":
    print("你好，" + temp + "!")
else:
    print("姓名不能为空哦！")
```

```bash
D:\code_dev>hello.py
请输入您的姓名：
姓名不能为空哦！

D:\code_dev>hello.py
请输入您的姓名：devin
你好，devin!
```

#### 2.5、Test-002

> 编写程序：calc.py，要求用于输入1到100之间数字并判断，输入符号要求打印“你妹好漂亮”，不符合要求则打印“你大爷好丑”

```python
# calc.py
temp = input("请输入1到100之间的数字：")
if 1 <= int(temp) <= 100:
    print("你妹好漂亮")
else:
    print("你大爷好丑")
```

```bash
D:\code_dev>calc.py
请输入1到100之间的数字：0
你大爷好丑

D:\code_dev>calc.py
请输入1到100之间的数字：18
你妹好漂亮

D:\code_dev>calc.py
请输入1到100之间的数字：101
你大爷好丑
```



### 第三章：基础知识-语法

#### 3.0、 注释

+ 单行注释： 以 `#`开头
+ 多行注释： 用三个单引号（‘’’）或三个双引号（“”“）将注释括起来

#### 3.1、变量

在大多数语言中，当我们定义一个变量时，会把这个变量存储在内存中，也就是变量赋值。但是在Python中，没有存储内存一说，也就是变量就是一个名字。
==值得注意==：

+ 在使用变量之前，需要对其先赋值

+ 变量名可以包括字母、数字、下划线，但是变量名不能以数字开头

+ 字母可以是大写或小写，但是大、小写是不同的

+ 等号（=）是赋值的意思

+ 变量命名尽量意义化

  ```python
  # test1.py
  
  # 数字变量
  x = 1
  print(x)  # > 1
  x = 2
  print(x)  # > 2
  
  # 字符串变量
  x = 'hello'
  y = 'world'
  print(x + y)  # >= helloworld
  ```

#### 3.2、改进小游戏

三大方面建议：

1. 猜错提示，比如告诉用户当前输入值和答案相比是大了还是小了
2. 如果猜错了，要多提供几次机会，至少3次机会
3. 每次运行，答案都是随机的

```python
# test1.py
import random
answer = random.randint(1, 10)
print("我想的数字是：" + answer)
temp = input("不妨猜下我现在心里想得是哪个数字：")
guess = int(temp)
times = 1
while (guess != answer) and (times < 3):
    if guess > answer:
        print("猜错啦，比我心里现在想的数字要大！")
    else:
        print("猜错啦，比我心里现在想的数字要小！")
    temp = input("再试试猜猜看吧：")
    guess = int(temp)
    times = times + 1

if (guess == answer) and (times <= 3):
    print("你是我心里的蛔虫吗？！")
    print("哼，即使你猜对了也没有奖励！")
else:
    print('三次都没有猜对，游戏结束，不玩啦^_^')
```

![](./_images/2_004.jpg)

#### 3.3、数据类型

Python中有6个标准的数据类型：

1. Numbers (数字)
2. String (字符串)
3. List (列表)
4. Tuple (元组)
5. Sets (集合)
6. Dictionaries (字典)

#### 3.4、Numbers(数字)

Python支持int(整型)、float(浮点型)、bool(布尔型)、complex(复数)。BIF`type()` 可以用来查询变量所指的对象类型。但是推荐是`isinstance()`这个BIF来判断变量类型。

==需要注意：==

+ Python可以同时为多个变量赋值，比如：`a, b = 1, 2`
+ 一个变量可以通过赋值指向不同类型的对象
+ 数值的除法（/）总是返回一个浮点数，要获取整数使用（//）操作符
+ 在混合计算时，Python会把整型转换为浮点数

```python
# type() 查询变量类型
a = 1
b = 1.1
c = True
d = 4 + 3j
print(type(a), type(b), type(c), type(d))
# > <class 'int'> <class 'float'> <class 'bool'> <class 'complex' >

# isinstance(v, type) 判断变量类型
e = 'hello'
print(isinstance(e, str))  # > True
f = 33
print(isinstance(f, float))  # > False
```

```python
# 数值运算
print(5 + 4)  # 加法 > 9
print(4.2 - 2)  # 减法 > 2.2
print(3 * 7)  # 乘法 > 21
print(8 / 4)  # 除法，取浮点数 > 2.0
print(2 // 5)  # 除法，取整数 > 0
print(17 % 3)  # 除法，取余 > 2
print(2 ** 5)  # 乘方 > 32
print(True + True)  # 布尔运算 > 2
print(True * False)  # 布尔运算 > 0
```

#### 3.5、 String(字符串)

Python中的字符串str用单引号（’‘）或双引号（“”）括起来，同时使用反斜杠（\）转义特殊字符。

字符串就是引号内的一切东西。字符串也成为文本，文本和数字是截然不同的。

字符串需要出现特殊字符如何处理？比如:

```python
# 处理字符串中特殊字符的两种方案
# e.g. Let's go

# 方案一：转义
print('Let\'s go') # > Let's go

# 方案二：嵌套
print("Let's go") # > Let's go
```

**原始字符串**

原始字符串定义：`r'xxx'`

```python
# 原始字符串
print(r'c:\\now') # > c:\\now
```

**长字符串**

长字符串定义：```“““String”””``` (三重引号) 

```python
# 长字符串
article = """
这是第一段
这是第二段

这是第三段

这是第四段
"""
print(article)
```

Python中的字符串有两种索引方式，第一种是从左往右，从0开始一次增加；第二种是从右往左，从-1开始依次减少。Python还可以对字符串进行切片，获取一段子串。用冒号分割两个索引，形式为变量[头下标:尾下标]。截取的范围是前闭后开的。

```python
# 字符串索引
str = 'I love SZ'
print(str[0], str[1], str[-1])  # > I   Z

# 字符串切片
str = "I love SZ"
print(str[0:6])  # > I love

# 字符串的值不能改变
str = "I love SZ"
# tr[0] = "i" !!报错
```

==需要注意==：

+ 反斜杠可以用来转义，使用`r`可以让反斜杠不发生转义
+ 字符串可以用`+`运算符连接在一起，用`*`运算符重复
+ Python中的字符串有两种索引方式，从左往右从0开始，从右往左以-1开始
+ Python中字符串不能改变











































