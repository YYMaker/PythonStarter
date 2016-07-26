# ex1 笔记

tags: print 字符串 引号 错误提示 字符编码

##1. 字符串的引号

在print中的字符串, 可以使用多种引号
单引号 ' 
双引号 "
三引号 ''' """ 三个单引号/三个双引号

当在字符串中使用到 单引号 或者 双引号 时可以使用 双引号 或者 单引号 引用字符串, 如果同时使用了单双引号在字符串中 可以使用三引号引用标注字符串. 

##2. python 错误提示

现代的编译器解释器更加人性化. 直接指出代码中可能出错的位置.

python 中的错误提示:

```
  File "ex1.py", line 3
    print "I Like typing this.
                             ^
SyntaxError: EOL while scanning string literal
```

***SyntaxError 格式错误 语法错误***


在之前GCC编译器是出了名的不说人话, 据说 Apple 多次向GCC提出需求, GCC的态度就是: 爱用不用, 我就这样. Apple 被逼无奈使用了LLVM做了编译器的前端, 和GCC合体. 

##3. 字符编码

Warning 如果你来自另外一个国家,而且你看到关于 ASCII 编码的错误,那就在你的 python 脚本的最上面加入 这一行:

```
# -*- coding: utf-8 -*-
```
这样你就在脚本中使用了 unicode UTF-8 编码,这些错误就不会出现了。

***为什么会起作用? 什么原理? 字符编码很有问题***

##4. 注释

在要注释的行首加井号:

```
#

```
井号英文名: 

octothorpe(八角帽)
pound(英镑符)
hash(电话的#键)
mesh(网)


# ex2 笔记

tags: 注释

## 1. 注释的作用

1. 使用自然语言描述某段代码的功能
2. 用注释将不需要的语言临时去掉

## 2. 可以注释的地方

1. 行首可以注释
2. 代码行尾也可以注释

##3. 注释多行
没有什么好方法, 每行前面加一个#


***作者在这里提出一个倒着读代码检查错误的方法, 有什么好处???***

多行注释, 可以用三引号

编辑器多行注释:
vim
1. 进入命令行模式，按ctrl + v进入 visual block模式，然后按j, 或者k选中多行，把需要注释的行标记起来
2. 按大写字母I，再插入注释符，例如//
3. 按esc键就会全部注释了



# ex3 笔记

tags: 运算符 浮点数 布尔值 运算符有优先级

## 1. 运算符


```
+ plus加号
- minus减号
/ slash斜杠
* asterisk星号
% percent百分号
< less-than小于号
> greater-than大于号
<= less-than-equal小于等于号
>= greater-than-equal大于等于号
```
## 2. 浮点数
浮点数(floating point number)

```
并不是说小数叫做浮点数。准确的来说：“浮点数”是一种表示数字的标准，整数也可以用浮点数的格式来存储。

当代大部分计算机和程序在处理浮点数时所遵循的标准是由IEEE和ANSI制定的。比如，单精度的浮点数以4个字节来表示，这4个字节可以分为三个部分：1位的符号位(0代表正数，1代表负数)，8位用作指数，最后的23位表示有效数字。

“浮点数”的定义是相对于“定点数”来说的，它们是两种表示小数的方式。

所谓“定点”是指小数点的位置总是在数的某个特定位置。
比如在银行系统中，小数点的位置总是在两位小数之前(这两位小数用来表示角和分)。其可以使用BCD码来对小数进行编码。

浮点格式则是基于科学计数法的，它是存储极大或极小数的理想方式。但使用浮点数来表示数据的时候，由于其标准制定方面的原因可能会带来一些问题，例如：某两个不同的整数在单精度浮点数的表示方法下很可能无法区分。

作者：vetch
链接：https://www.zhihu.com/question/19848808/answer/22219209
来源：知乎
著作权归作者所有，转载请联系作者获得授权。

“浮点数”的定义是相对于“定点数”来说的。
在计算机内部，数据以二进制的形式存储和运算，而计算机内表示的数，又被分成整数和实数两大类。
其中整数一般用定点数表示，定点数指小数点在数中有固定的位置（一般来说整数的小数点都在最末位数后）。
实数一般用浮点数表示，因为它的小数点位置不固定。浮点数是既有整数又有小数的数，纯小数可以看作实数的特例。

作者：梁白开
链接：https://www.zhihu.com/question/19848808/answer/19978437
来源：知乎
著作权归作者所有，转载请联系作者获得授权。
```
## 3. 布尔类型

boolean 布尔值

True 真
False 假

## 4. 运算符优先级

美国我们用 PEMDAS 这个简称来辅助记忆,它的意思是“括号、指数、乘、除、加、减”—— Parentheses Exponents Multiplication Division Addition Subtraction ——这也是 Python 里的运算优先级。



# ex4 笔记

## 1. 变量名

程序员通过使用变量名可以让他们的程序读起来更像英语。变量名可以让程序的内容更加明了。

变量名不能以数字开始.

```
4. 记住 = 的名字是等于(equal),它的作用是为数据取名。
```


***思考:
在C语言中, 变量名标记的是一块内存空间, 或者是内存空间的地址.
看到书中出现的这句, 觉得在python中更多的是为数据起名字, 应为在python中定义变量非常的随意. 并且python中的变量是弱类型的, 也就是说python中一个变量可以存放任何内容.***

## 2. 变量未定义错误

```
Traceback (most recent call last):  File "ex4.py", line 8, in <module>   average_passengers_per_car = car_pool_capacity / passengerNameError: name 'car_pool_capacity' is not defined
```
not defined 未定义

## 3. 变量赋值

```
= single-equal (单个等号, 表示赋值)

== double-equal (双等号, 用来判断两边是否相等)
```


***为什么倒着读代码?
正着读代码, 大脑会根据前文意思自动脑补缺失错误的信息, 从而不容易发现错误. 而倒着读就会只注意到单字, 单词, 更容易发现错误.***

研表究明，汉字的序顺并不定一能影阅响读，比如当你看完这句话后，才发这现里的字全是都乱的、。



# ex5 笔记

tags: 

## 0. code

```
#ex5
my_name = 'xxxx'
my_age = 35 #not a lie ^_^
my_height = 74 #inches
my_weight = 180 #lbs
my_eyes = 'Blue'
my_teeth = 'White'
my_hair = 'Brown'

print "Let's talk about %s." % my_name
print "He's %d inches tall." % my_height
print "He's %d pounds heavy." % my_weight
print "Actually that's not too heavy."
print "He's got %s eyes and %s hair." % (my_eyes, my_hair)
print "His teeth are usually %s depending on the coffee." % my_teeth


# this line is tricky, try to get it exactly right
print "If I add %d, %d, and %d I get %d." % (my_age, my_weight, my_height, my_age + my_weight + my_height)
```

## 1. 格式化字符串

format string 格式化字符串

字符串是程序传递信息最主要的一种方式. 展示内容, 打印, 传输

## 2. 格式控制工具

%d 十进制
%s 字符串
%r 无论什么都输出 (通常用来debug) representation

## 3. 四舍五入

round函数
round(1.7333)

四舍五入, 变整数

***问题: 小数位保留四舍五入怎么做?***

round(1.7333, 2)
第二个参数代表保留小数点后几位. 

# ex6 笔记

tags: 字符串

## 0. code

```
#ex6 
x = "There are %d types of people." % 10
binary  = "binary"
do_not = "don't"
y = "Those who know %s and those who %s." % (binary, do_not)

print x
print y

print "I said: %r." % x
print "I also said: '%s'. " % y

hilarious = False
joke_evaluation = "Isn't that joke so funny?! %r"

print joke_evaluation % hilarious

w = "This is the left side of..."
e = "a string with a right side."

print w + e
```

## 1. 字符串拼接

```
print str1 + str2
```

## 2. 格式化字符串

print 中多个参数拼接

```
print "%d, %d, %d", % (xxx , xxx, xxx)
```

## 3. 错误

没有足够的参数提供给格式化字符串使用

```
Traceback (most recent call last):
  File "ex6.py", line 10, in <module>
    print "I also said: '%s'. %d" % y
TypeError: not enough arguments for format string
```


格式化字符串中没有把所有的参数输出

```
Traceback (most recent call last):
  File "ex6.py", line 10, in <module>
    print "I also said: ''. " % y
TypeError: not all arguments converted during string formatting
```



# ex7 笔记

## 0. code

```
#ex7

print "Mary had a little lamb."
print "Its fleece was white as %s." % 'snow'
print "And everywhere that Mary went."
print "." * 10 # what'd that do?

end1 = "C"
end2 = "h"
end3 = "e"
end4 = "e"
end5 = "s"
end6 = "e"
end7 = "B"
end8 = "u"
end9 = "r"
end10 = "g"
end11 = "e"
end12 = "r"

# watch that comma at the end. try removing it to see what happens
print end1 + end2 + end3 + end4 + end5 + end6,
print end7 + end8 + end9 + end10 + end11 + end12
```
运行结果:

```
YY:LPTHW Y2Maker$ python ex7.py
Mary had a little lamb.
Its fleece was white as snow.
And everywhere that Mary went.
..........
Cheese Burger
```

## 1. 逗号的作用

看起来像是连接字符串的作用. 不是默认输出换行符, 而是输出一个空格. 不可多个连用.


## 2. 输出多次

print 'Hello' * 10



# Ex8: printing, printing

## 0. code

```
#ex8

formatter = "%r %r %r %r"

print formatter % (1, 2, 3, 4)
print formatter % ("one", "two", "three", "four")
print formatter % (True, False, False, True)
print formatter % (formatter, formatter, formatter, formatter)
print formatter % (
    "I had this thing.",
    "That you could type up right.",
    "But it didn't sing.",
    "So I said goodnight."
)
```

运行结果:

```
YY:LPTHW Y2Maker$ python ex8.py
1 2 3 4
'one' 'two' 'three' 'four'
True False False True
'%r %r %r %r' '%r %r %r %r' '%r %r %r %r' '%r %r %r %r'
'I had this thing.' 'That you could type up right.' "But it didn't sing." 'So I said goodnight.'
```

## 1. %r 的作用

%r 通常用作获取debug信息
The %r will give you the "raw programmer's" version of variable, also known as the "representation."
获取程序员级的数据

## 2. True False
True 和 False 在 python 中被当做keywords(关键字)代表布尔值的真和假, 如果加引号就变成了字符串. 



# Ex.9 printing, printing, printing

## 0. code

```
# Here's some new strange stuff, remember type it exactly

days = "Mon Tue Wed Thu Fri Sat Sun"
months = "\nJan\nFeb\nMar\nApr\nMay\nJun\nJul\nAug"

print "Here are the days: ", days
print "Here are the months: ", months

print """
There's something going on here.
With the three double-quotes.
We'll be able to type as much as we like.
Even 4 lines if we want, or 5, or 6.
"""

print "%r" % months
```

输出结果:

```
YY:LPTHW Y2Maker$ python ex9.py
Here are the days:  Mon Tue Wed Thu Fri Sat Sun
Here are the months:
Jan
Feb
Mar
Apr
May
Jun
Jul
Aug

There's something going on here.
With the three double-quotes.
We'll be able to type as much as we like.
Even 4 lines if we want, or 5, or 6.

'\nJan\nFeb\nMar\nApr\nMay\nJun\nJul\nAug'
```



# Ex.10 What Was That?

## 0. code

```
tabby_cat = "\tI'm tabbed in."
persian_cat = "I'm split\non a line."
backslash_cat = "I'm \\ a \\ cat."

fat_cat = """
I'll do a list:
\t* Cat food
\t* Fishies
\t* Catnip\n\t* Grass
"""

print tabby_cat
print persian_cat
print backslash_cat
print fat_cat
```
运行结果:

```
YY:LPTHW Y2Maker$ python ex10.py
	I'm tabbed in.
I'm split
on a line.
I'm \ a \ cat.

I'll do a list:
	* Cat food
	* Fishies
	* Catnip
	* Grass
```

## 1.转译字符

```
\\   Backslash () 反斜杠￼￼￼￼\'   Single quote (‘) 单引号￼￼￼￼\"   Double quote (”) 双引号￼￼￼￼\a   ASCII Bell (BEL) 响铃符￼￼￼￼\b   ASCII Backspace (BS) 退格符￼￼￼￼\f   ASCII Formfeed (FF) 进纸符￼￼￼￼\n   ASCII Linefeed (LF) 换行符\N{name} 
Unicode 数据 库中的字符名, 其中 name 就 是它的名字 (Unicodeonly)\r   ASCII Carriage Return (CR) 回车符￼￼￼￼\t   ASCII Horizontal Tab (TAB) 水 平制表符￼￼￼￼
\uxxxx    
值为 16 位十 六进制值 xxxx 的字符 (Unicode only)

￼￼￼￼\Uxxxxxxxx
值为 32 位十 六进制值 xxxx 的字符 (UnicodeUnicode 数据 库中的字符名, 其中 name 就 是它的名字 (Unicodeonly)

\v    ASCII Vertical Tab (VT) 垂直制 表符\ooo  值为八进制值 ooo 的字符\xhh  值为十六进制 数 hh 的字符

```

## 2. 换行
在python中代码中的换行可以体现在最终输入内容中, 区别于C语言. 
在python代码中, 字符串在代码中换行就相当于输入了 '\n' 


# Ex.11 Asking Questions

## 0. Code


```
print "How old are you?",
age = raw_input()
print "How tall are you?",
height = raw_input()
print "How much do you weigh?",
weight = raw_input()

print "So, you're %r old, %r tall and %r heavy." % (age, height, weight)
```

运行结果:

```
How old are you? 10
How tall are you? 10
How much do you weigh? 10
So, you're '10' old, '10' tall and '10' heavy.
```

## 1. print逗号的作用

在print 后加 逗号, 似乎可以消掉 '\n'

## 2. 获取数字 字符串转数字

```
a = int(raw_input())
print a * 10

b = raw_input()
print b * 10

```

## 3. input 和 raw_input 的区别

***TODO***


# Ex. 12 Prompting People

## 0. Code

```
age = raw_input("How old are you? ")
height = raw_input("How tall are you? ")
weight  = raw_input("How much do you weigh? ")

print "So, you're %r old, %r tall and %r heavy." % (
       age, height, weight)
```





## 1. raw_input

pydoc raw_input

```
Help on built-in function raw_input in module __builtin__:

raw_input(...)
    raw_input([prompt]) -> string

    Read a string from standard input.  The trailing newline is stripped.
    If the user hits EOF (Unix: Ctl-D, Windows: Ctl-Z+Return), raise EOFError.
    On Unix, GNU readline is used if enabled.  The prompt string, if given,
    is printed without a trailing newline before reading.
```

## 2. pydoc 命令



Windows下怎么运行pydoc? 

```
$ python -m pydoc raw_input
```



# Ex. 13 Parameters, Unpacking, Variables 参数, 解包, 变量

## 0. Code

```
from sys import argv

script, first, second, third = argv

print "The script is called:", script
print "Your first variable is:", first
print "Your second variable is:", second
print "Yout third variable is:", third
```

运行结果:

```
YY:LPTHW Y2Maker$ python ex13.py hehe haha heihei
The script is called: ex13.py
Your first variable is: hehe
Your second variable is: haha
Yout third variable is: heihei
```

## 1. import 引入

import 可以引入 python的各种模块 (modules)

unpack 解包


## 2. 不定参数的情况怎么处理?



## 3. 错误


```
Traceback (most recent call last):
  File "ex13.py", line 3, in <module>
    script, first, second, third = argv
ValueError: need more than 3 values to unpack
```

拆解的参数个数大于参数总数, 缺少参数的错误提示


# Ex. 14 Prompting And passing 提示和传递


## 0. Code

```
from sys import argv

script, user_name = argv
prompt = '>>>'

print "Hi %s, I'm the %s script." % (user_name, script)
print "I'd like to ask you a few questions."
print "Do you like me %s?" % user_name
likes = raw_input(prompt)

print "Where do you live %s?" % user_name
lives = raw_input(prompt)

print "What kind of computer do you have?"
computer = raw_input(prompt)

print """
Alright, so you said %r about liking me.
You live in %r. Not sure where that is.
And you have a %r computer. Nice.
""" % (likes, lives, computer)
```

# Ex. 15 Reading Files 读取文件

## 0. Code

```
from sys import argv

script, filename = argv

txt = open(filename)

print "Here's your file %r:" % filename
print txt.read()

print "Type the filename again:"
file_again = raw_input("> ")

txt_again = open(file_again)

print txt_again.read()
```

## 1. open

open() 打开文件

```
open(...)
    open(name[, mode[, buffering]]) -> file object

    Open a file using the file() type, returns a file object.  This is the
    preferred way to open a file.  See file.__doc__ for further information.
```
多个参数:
参数1 : 打开文件的, 文件名

## 2. txt.read()

txt.read()

打开文件后赋值给txt, 使其执行read, 读取文件内容. 


# Ex.16 Reading and Writing Files 读写文件

## 0. Code


```
from sys import argv

script, filename = argv

print "We're going to erase %r." % filename
print "If you don't want that, hit CTRL-C(^C)."
print "If you do want that, hit RETURN."

raw_input("?")

print "Opening the file..."
target = open(filename, 'w')

print "Truncating the file. Goodbye!"
target.truncate()

print "Now I'm going to ask you for three lines."
line1 = raw_input("line 1: ")
line2 = raw_input("line 2: ")
line3 = raw_input("line 3: ")

print "I'm going to write these to the file."

target.write(line1)
target.write('\n')
target.write(line2)
target.write('\n')
target.write(line3)
target.write('\n')

print "And finally, we close it."
target.close()
```

运行结果:

argv 传入 filename, 通过 truncate 清空文件内容, 之后使用 write 将数据写入文件


## 1. open 参数

不指定参数, open 默认是以只读的方式打开. 

w 写入
r 读取
a 追加

w+
r+
a+

*** 同时以读写的方式打开 ***


# Ex. 17 More Files 更多文件操作

## 0. Code

```
from sys import argv
from os.path import exists

script, form_file, to_file = argv

print "Copying from %s to %s" % (from_file, to_file)

# we could do these two on one line too, how?

in_file = open(from_file)
indata = in_file.read()

print "The input file is %d bytes long" % len(indata)

print "Does the output file exist? %r" % exists(to_file)
print "Ready, hit RETURN to continue, CTRL-C to abort."
raw_input()

out_file = open(to_file, 'w')
out_file.write(indata)

print "Alright, all done."

out_file.close()
in_file.close()

```

运行结果:

输入 两个文件名, 将第一个文件的内容, 写入到第二个文件中

## 1. len函数 

len()
统计字符串长度, 文件内容是 "hello"为什么是 6
应为使用vim编辑之后 在行尾会加上'0x0a'的字符, 也就是换行. 

## 2. exists
exists 判断文件是否存在, 返回布尔值

属于模块 from os.path import exists


## 3. open w参数

w参数会直接创建文件.

## 4. close

关闭打开的文件

*** 使用read 读到文件末尾, 会自动关闭文件吗? ***


# Ex.18 Names, Variables, Code, Functions 命名 变量 代码 函数

## 0. Code

```
# this one is like your scripts with argv
def print_two(*args):
    arg1, arg2 = args
    print "arg1: %r, arg2: %r" % (arg1, arg2)

# ok, thar *args is actually pointless, we can just do this
def print_two_again(arg1, arg2):
    print "arg1: %r, arg2: %r" % (arg1, arg2)

# this just takes one argument
def print_one(arg1):
    print "arg1: %r" %arg1

# this one takes no arguments
def print_none():
    print "I got nothin'."

print_two("Zed", "Shaw")
print_two_again("Zed", "Shaw")
print_one("First!")
print_none()
```
输出结果:

```
arg1: 'Zed', arg2: 'Shaw'
arg1: 'Zed', arg2: 'Shaw'
arg1: 'First!'
I got nothin'.
```

## 1. 函数定义与参数

使用def 定义函数
函数的参数 可以是定参, 也可以是不定参. 

不定参定义方法: 

```
def print_two(*args):
    arg1, arg2 = args
    print "arg1: %r, arg2: %r" % (arg1, arg2)
```
*** 同样, 不定参如何控制参数?? ***

*args  将参数放入参数列表

# Ex.19 Functions and Variables 函数和参数

## 0. Code

```
def cheese_and_crackers(cheese_count, boxes_of_crackers):
    print "You have %d cheesee!" % cheese_count
    print "You have %d boxes of crackers!" % boxes_of_crackers
    print "Man that's enough for a party!"
    print "Get a blanket.\n"

print "We can just give the function numbers directly:"
cheese_and_crackers(20, 30)

print"OR, we can use variables from our script:"
amount_of_cheese = 10
amount_of_crackers = 50

cheese_and_crackers(amount_of_cheese, amount_of_crackers)

print "We can even do math inside too:"
cheese_and_crackers(10 + 20, 5 + 6)

print "And we can combine the two, variables and math:"
cheese_and_crackers(amount_of_cheese + 100, amount_of_crackers + 1000)
```



## 1. 函数传参



# Ex.20 Functions And Files 函数和文件

## 0. Code

```
from sys import argv

script, input_file = argv

def print_all(f):
    print f.read()

def rewind(f):
    f.seek(0)

def print_a_line(line_count, f):
    print line_count, f.readline()

current_file = open(input_file)

print "First let's print the whole file:\n"

print_all(current_file)

print "Now let's rewind, kind of like a tape."

rewind(current_file)

print "Let's print three lines:"

current_line = 1
print_a_line(current_line, current_file)

current_line = current_line + 1
print_a_line(current_line, current_file)

current_line = current_line + 1
print_a_line(current_line, current_file)

```
运行结果

```
YY:LPTHW Y2Maker$ python ex20.py test.txt
First let's print the whole file:

hehe
haha
heihei

Now let's rewind, kind of like a tape.
Let's print three lines:
1 hehe

2 haha

3 heihei

```

## 1. seek

偏移文件读写指针

## 2. readline

读取一行


































<br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> <br /> 
