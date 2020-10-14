# Python数据类型

### 一、Python介绍

####  1、Python的出生和应用

​		python的创始人为吉多·范罗苏姆（Guido van Rossum）。1989年的圣诞节期间，吉多·范罗苏姆（中文名字：龟叔）为了在阿姆斯特丹打发时间，决心开发一个新的脚本解释程序，作为ABC语言的一种继承。 

Python可以应用于众多领域，如：数据分析、组件集成、网络服务、图像处理、数值计算和科学计算等众多领域。目前业内几乎所有大中型互联网企业都在使用Python，如：Youtube、Dropbox、BT、Quora（中国知乎）、豆瓣、知乎、Google、Yahoo!、Facebook、NASA、百度、腾讯、汽车之家、美团等。

**目前Python主要应用领域：**

- **云计算**: 云计算最火的语言， 典型应用OpenStack
- **WEB开发**: 众多优秀的WEB框架，众多大型网站均为Python开发，Youtube, Dropbox, 豆瓣。。。， 典型WEB框架有Django
- **科学运算、人工智能**: 典型库NumPy, SciPy, Matplotlib, Enthought librarys,pandas
- **系统运维**: 运维人员必备语言
- **金融**：量化交易，金融分析，在金融工程领域，Python不但在用，且用的最多，而且重要性逐年提高。原因：作为动态语言的Python，语言结构清晰简单，库丰富，成熟稳定，科学计算和统计分析都很牛逼，生产效率远远高于c,c++,java,尤其擅长策略回测
- **图形GUI**: PyQT, WxPython,TkInter

**Python在一些公司的应用：** 

- 谷歌：Google App Engine 、code.google.com 、Google earth 、谷歌爬虫、Google广告等项目都在大量使用Python开发
- CIA: 美国中情局网站就是用Python开发的
- NASA: 美国航天局(NASA)大量使用Python进行数据分析和运算
- YouTube:世界上最大的视频网站YouTube就是用Python开发的
- Dropbox:美国最大的在线云存储网站，全部用Python实现，每天网站处理10亿个文件的上传和下载
- Instagram:美国最大的图片分享社交网站，每天超过3千万张照片被分享，全部用python开发
- Facebook:大量的基础库均通过Python实现的
- Redhat: 世界上最流行的Linux发行版本中的yum包管理工具就是用python开发的
- 豆瓣: 公司几乎所有的业务均是通过Python开发的
- 知乎: 国内最大的问答社区，通过Python开发(国外Quora)
- 春雨医生：国内知名的在线医疗网站是用Python开发的
- 除上面之外，还有搜狐、金山、腾讯、盛大、网易、百度、阿里、淘宝 、土豆、新浪、果壳等公司都在使用Python完成各种各样的任务。 

#### 2、Python是什么编程语言

编程语言分为编译型、解释型、静态语言和动态语言，强类型定义和弱类型定义的语言。

2.1编译型和解释型

**编译器**是把源程序的每一条语句都编译成机器语言,并保存成二进制文件,这样运行时计算机可以直接以机器语言来运行此程序,速度很快; 

**编译型**

优点：编译器一般会有预编译的过程对代码进行优化。因为编译只做一次，运行时不需要编译，所以编译型语言的程序执行效率高。可以脱离语言环境独立运行。
缺点：编译之后如果需要修改就需要整个模块重新编译。编译的时候根据对应的运行环境生成机器码，不同的操作系统之间移植就会有问题，需要根据运行的操作系统环境编译不同的可执行文件。

**解释器**则是只在执行程序时,才一条一条的解释成机器语言给计算机来执行,所以运行速度是不如编译后的程序运行的快的。

**解释型：**

优点：有良好的平台兼容性，在任何环境中都可以运行，前提是安装了解释器（虚拟机）。灵活，修改代码的时候直接修改就可以，可以快速部署，不用停机维护。

缺点：每次运行的时候都要解释一遍，性能上不如编译型语言。

2.2动态语言和静态语言

通常我们所说的动态语言、静态语言是指动态类型语言和静态类型语言。

（1）动态类型语言：动态类型语言是指在运行期间才去做数据类型检查的语言，也就是说，在用动态类型的语言编程时，永远也不用给任何变量指定数据类型，该语言会在你第一次赋值给变量时，在内部将数据类型记录下来。Python和Ruby就是一种典型的动态类型语言，其他的各种脚本语言如VBScript也多少属于动态类型语言。

（2）静态类型语言：静态类型语言与动态类型语言刚好相反，它的数据类型是在编译其间检查的，也就是说在写程序时要声明所有变量的数据类型，C/C++是静态类型语言的典型代表，其他的静态类型语言还有C#、JAVA等。

**2.3强类型定义语言和弱类型定义语言**

（1）强类型定义语言：强制数据类型定义的语言。也就是说，一旦一个变量被指定了某个数据类型，如果不经过强制转换，那么它就永远是这个数据类型了。举个例子：如果你定义了一个整型变量a,那么程序根本不可能将a当作字符串类型处理。强类型定义语言是类型安全的语言。

（2）弱类型定义语言：数据类型可以被忽略的语言。它与强类型定义语言相反, 一个变量可以赋不同数据类型的值。

强类型定义语言在速度上可能略逊色于弱类型定义语言，但是强类型定义语言带来的严谨性能够有效的避免许多错误。另外，“这门语言是不是动态语言”与“这门语言是否类型安全”之间是完全没有联系的！
例如：Python是动态语言，是强类型定义语言（类型安全的语言）; VBScript是动态语言，是弱类型定义语言（类型不安全的语言）; JAVA是静态语言，是强类型定义语言（类型安全的语言）。

通过上面这些介绍，我们可以得出，**python是一门动态解释性的强类型定义语言**

#### 3、Python的优缺点

优点

1、Python的定位是“优雅”、“明确”、“简单”，所以Python程序看上去总是简单易懂，初学者学Python，不但入门容易，而且将来深入下去，可以编写那些非常非常复杂的程序。

2、开发效率非常高，Python有非常强大的第三方库，基本上你想通过计算机实现任何功能，Python官方库里都有相应的模块进行支持，直接下载调用后，在基础库的基础上再进行开发，大大降低开发周期，避免重复造轮子。

3、高级语言————当你用Python语言编写程序的时候，你无需考虑诸如如何管理你的程序使用的内存一类的底层细节

4、可移植性————由于它的开源本质，Python已经被移植在许多平台上（经过改动使它能够工 作在不同平台上）。如果你小心地避免使用依赖于系统的特性，那么你的所有Python程序无需修改就几乎可以在市场上所有的系统平台上运行

5、可扩展性————如果你需要你的一段关键代码运行得更快或者希望某些算法不公开，你可以把你的部分程序用C或C++编写，然后在你的Python程序中使用它们。

6、可嵌入性————你可以把Python嵌入你的C/C++程序，从而向你的程序用户提供脚本功能。

缺点：

1. 速度慢，Python 的运行速度相比C语言确实慢很多，跟JAVA相比也要慢一些，但其实这里所指的运行速度慢在大多数情况下用户是无法直接感知到的，必须借助测试工具才能体现出来，比如你用C运一个程序花了0.01s,用Python是0.1s,这样C语言直接比Python快了10倍,算是非常夸张了，但是你是无法直接通过肉眼感知的，因为一个正常人所能感知的时间最小单位是0.15-0.4s左右。
2. 代码不能加密，因为PYTHON是解释性语言，它的源码都是以明文形式存放的。
3. 线程不能利用多CPU问题，这是Python被人诟病最多的一个缺点，GIL即全局解释器锁（Global Interpreter Lock），是[计算机程序设计语言](http://zh.wikipedia.org/wiki/计算机程序设计语言)[解释器](http://zh.wikipedia.org/wiki/解释器)用于[同步](http://zh.wikipedia.org/wiki/同步)[线程](http://zh.wikipedia.org/wiki/线程)的工具，使得任何时刻仅有一个线程在执行，Python的线程是操作系统的原生线程。在Linux上为pthread，在Windows上为Win thread，完全由操作系统调度线程的执行。一个python解释器进程内有一条主线程，以及多条用户程序的执行线程。即使在多核CPU平台上，由于GIL的存在，所以禁止多线程的并行执行。

当我们编写Python代码时，我们得到的是一个包含Python代码的以`.py`为扩展名的文本文件。要运行代码，就需要Python解释器去执行`.py`文件。

### 二、Python基础知识

#### 1、Python环境

编译型：将程序一次转成二进制。

​                缺点：开发效率低，不能跨平台。

​                优点：执行速度快。C、C++

 解释型：同声翻译，当程序执行时，一行一行的解释。

​                优点：开发效率高，可以跨平台。

​                 缺点：运行速度慢。

**Python是一门动态解释型强关联类型定义的语言**。

Python的种类：Cpython ---C语言编译字节码

​         				   JPython----java编译字节码

​        				    Pypy-----一次性编译的 

python 2 中默认编码方式是ASCII码方式

python3默认是编码方式UTF-8

Python2和Python3之间编码方式不同的解决方式：在文件首行加 # -*- encoding :utf-8 -*- 

 #### 2、Python基础

##### 2.1 常量

常量即指不变的量，如pai 3.141592653..., 或在程序运行过程中不会改变的量。一般使用大写字母表示如：

PI= 3.14

##### 2.1 变量

变量：把程序运行的中间结果临时的存在内存里，以便后续的代码调用。

2.1.1 声明变量

lux = '鲁迅本人'

lux是变量的名字，’鲁迅本人‘是变量的值。

变量的作用就是一个昵称，代指内存里某个地址中保存的内容。

<img src="/Users/mac/Library/Application Support/typora-user-images/image-20201012095744120.png" alt="image-20201012095744120" style="zoom:50%;" />

2.1.2 **变量命名规则**

- 变量名只能是 字母、数字或下划线的任意组合

- 变量名的第一个字符不能是数字

- 不能是Python的关键字

- 变量名是具有描述性的

  

2.1.3 推荐定义的方式

驼峰式：AgeOfBoy = 1

下划线：age_of_boy= 1

##### 3、注释

一行注释：#我被注释了

多行注释：‘’‘我被注释了’‘’、“”“我被注释了”“”

#### 三、Python基础数据类型

什么是数据类型？

　　我们人类可以很容易的分清数字与字符的区别，但是计算机并不能呀，计算机虽然很强大，但从某种角度上看又很傻，除非你明确的告诉它，1是数字，“汉”是文字，否则它是分不清1和‘汉’的区别的，因此，在每个编程语言里都会有一个叫数据类型的东东，其实就是对常用的各种数据类型进行了明确的划分，你想让计算机进行数值运算，你就传数字给它，你想让他处理文字，就传字符串类型给他。

Python中常用的数据类型有多种，如下

整数(int) ,字符串(str),布尔值(bool),列表(list),元组(tuple),字典(dict),集合(set).

-  int。数字：主要用于运算。1 ，2,3...
-  bool。判断真假：True, False.
-  str。简单少量的储存数据，并进行相应的操作。name = 'alex',
-  tuple。只读，不能更改。(1,'alex') 
-  list：大量有序数据，[1,'ses',True,[1,2,3],{'name':'jinxin'}]
-  dict：大量数据，且是关联性比较强的数据 {'name':'jinxin','age':18,'name_list':['张三'，'李四']}

#####1、整数类型（int）

 **1.1.1 十进制二进制转换**

  **十进制整数转换为二进制整数**采用"除2取余，逆序排列"法。具体做法是：用2整除十进制整数，可以得到一个商和余数；再用2去除商，又会得到一个商和余数，如此进行，直到商为小于1时为止，然后把先得到的余数作为二进制数的低位有效位，后得到的余数作为二进制数的高位有效位，依次排列起来。

**十进制小数转换成二进制小数**采用"乘2取整，顺序排列"法。具体做法是：用2乘十进制小数，可以得到积，将积的整数部分取出，再用2乘余下的小数部分，又得到一个积，再将积的整数部分取出，如此进行，直到积中的小数部分为零，此时0或1为二进制的最后一位。或者达到所要求的精度为止。

**二进制转化成十进制:** 

  要从右到左用二进制的每个数去乘以2的相应次方,小数点后则是从左往右

  例如：二进制数1101.01转化成十进制

  1101.01（2）=1*20+0*21+1*22+1*23 +0*2-1+1*2-2=1+0+4+8+0+0.25=13.25（10）

  所以总结起来通用公式为：

  abcd.efg(2)=d\*2^0+c\*2^1+b\*2^2+a\*2^3+e\*2^-1+f\*2^-2+g\*2^-3（10）

或者是：

  把二进制数首先写成加权系数展开式，然后按十进制加法规则求和。这种做法称为"按权相加"法。

  此时，1101=8+4+0+1=13

  再比如：二进制数100011转成十进制数可以看作这样：

  数字中共有三个1 即第一位一个，第五位一个，第六位一个，然后对应十进制数即2的0次方+2的1次方+2的5次方， 即

  100011=32+0+0+0+2+1=35

在32位机器上，整数的位数为32位，取值范围为$$-2^{31}～2^{31}-1$$，即-2147483648～2147483647

在64位系统上，整数的位数为64位，取值范围为$-2^{63}～2^{63}-1$，即-9223372036854775808～9223372036854775807

```python 
#bit_length()就是帮助你快速的计算整数在内存中占用的二进制码的长度.
a = 10
print(a.bit_length())
```

#####2、布尔值bool

布尔值就两种：True，False。就是反应条件的正确与否。

真  1  True。

假  0  False。  

**int→str→bool三者之间的转换**

```python
#int --> bool
i = 100
print(bool(i))  #True

i1 = 0
print(bool(i1))  # False 零即False

# bool ---> int
t = True
print(int(t))  # 1  True --> 1
t = False
print(int(t))  # 0  False --> 0

# int ---> str
i1 = 100
print(str(i1))  # '100'

# str ---> int  # 全部由数字组成的字符串才可以转化成数字
s1 = '90'
print(int(s1))  # 90

# str ---> bool
s1 = '太白'
s2 = ''
print(bool(s1))  # True 非空即True
print(bool(s2))  # False
# bool ---> str
t1 = True
print(str(True))  # 'True'
```

##### 3、字符串str

Python中凡是用引号引起来的数据可以称为字符串类型，组成字符串的每个元素称之为字符，将这些字符一个一个连接起来，然后在用引号起来就是字符串。

```python 
a = '基础'
#a是由两个字符组成：基、础
```

**3.1 字符串的索引与切片**

组成字符串的字符从左至右，依次排列，他们都是有顺序的，就好比是部队的队列，从左至右依次报号(从零开始) ：0,1,2,3....

索引即下标，就是字符串组成的元素从第一个开始，初始索引为0以此类推。

```python 
a = 'ABCDEFGHIJK'
print(a[0]) #A
print(a[3]) #D
print(a[5]) #F
print(a[7]) #H
```

**切片就是通过索引（索引：索引：步长）**截取字符串的一段，形成新的字符串（原则就是顾头不顾腚）。[索引1，索引2）

```python 
a = 'ABCDEFGHIJK'
print(a[0:3])  # print(a[:3]) 从开头开始取0可以默认不写
print(a[2:5])
print(a[:]) #默认到最后
print(a[:-1]) # -1 是列表中最后一个元素的索引，但是要满足顾头不顾腚的原则，所以取不到K元素
print(a[:5:2]) #加步长
print(a[-1:-5:-2]) #反向加步长
```

##### 3.2字符串常用方法

- s.capitalize()首字母大写

- s.lower()小写

- s.upper()大写

- s.swapcase() 大小写翻转

- s.title()单词中间用空格或者特殊符号或数字隔开的首字母大写

- s.center(self,宽度，填充内容）

- s.expandtabs()字符串中含有/t则前面的到/t时，每8位出现一个tab

- s.count(a) 数字符串中的元素出现的个数

- startswith ()判断是否以...开头

- endswith() 判断是否以...结尾

- split() 以什么分割，最终形成一个列表此列表不含有这个分割的元素。

- find('w')寻找这个w元素，返回索引，没有返回-1

- index('a')通过元素寻找索引找不到会报错

- strip()默认以空格去除，删除首位的空格，也可以都删除其中的东西。

  ```python
  #数字符串中的元素出现的个数。
ret3 = a1.count("a",0,4) # 可切片
print(ret3)
  
  a4 = "dkfjdkfasf54"
  #startswith 判断是否以...开头
  #endswith 判断是否以...结尾
ret4 = a4.endswith('jdk',3,6)  # 顾头不顾腚
print(ret4)  # 返回的是布尔值
 ret5 = a4.startswith("kfj",1,4)
print(ret5)
  
  #split 以什么分割，最终形成一个列表此列表不含有这个分割的元素。
ret9 = 'title,Tilte,atre,'.split('t')
print(ret9)
ret91 = 'title,Tilte,atre,'.rsplit('t',1)
print(ret91)
  
  #strip
  name='*barry**'
  print(name.strip('*'))
  print(name.lstrip('*'))
  print(name.rstrip('*'))
  
  #replace
  name='alex say :i have one tesla,my name is alex'
  print(name.replace('alex','SB',1))
  
  #####is系列
  name='taibai123'
  print(name.isalnum()) #字符串由字母或数字组成
  print(name.isalpha()) #字符串只由字母组成
  print(name.isdecimal()) #字符串只由十进制组成
  
  #寻找字符串中的元素是否存在
  # ret6 = a4.find("fjdk",1,6)
  # print(ret6)  # 返回的找到的元素的索引，如果找不到返回-1
  
  # ret61 = a4.index("fjdk",4,6)
  # print(ret61) # 返回的找到的元素的索引，找不到报错。
  
  #captalize,swapcase,title
  print(name.capitalize()) #首字母大写
  print(name.swapcase()) #大小写翻转
  msg='taibai say hi'
  print(msg.title()) #每个单词的首字母大写
  
  # 内同居中，总长度，空白处填充
  ret2 = a1.center(20,"*")
  print(ret2)
  ```

##### format用法

```Python
#format的三种玩法 格式化输出
res='{} {} {}'.format('egon',18,'male')
res='{1} {0} {1}'.format('egon',18,'male')
res='{name} {age} {sex}'.format(sex='male',name='egon',age=18)
```

##### 4、列表list  **以[ ]形式扩充，‘，’分隔**

  1、字符串只能存储少量的数据，对于大量的数据用字符串操作不方便也不易存储。

  2、字符串存储的数据类型太单一，只能是字符串类型。

python提供了一类数据类型，他能承载多种数据类型，这类数据类型被称作容器类数据类型可以存储大量的数据。列表就属于容器类的数据类型。

列表是python的基础数据类型之一 ,其他编程语言也有类似的数据类型.比如JS中的数组, java中的数组等等. 它是**以[ ]括起来, 每个元素用' , '隔开**而且可以存放各种数据类型: 列表是python中的基础数据类型之一。**列表是有序的，有索引值，可切片，方便取值。**

**4.1列表的创建**

```Python
# 创建一个列表有三种方式：

# 方式一：（常用）
l1 = [1, 2, '太白']

# 方式二：（不常用）
l1 = list()  # 空列表
# l1 = list(iterable)  # 可迭代对象
l1 = list('123')
print(l1)  # ['1', '2', '3']

# 方式三：列表推导式（后面的课程会讲到）
l1 = [i for i in range(1,5)]
print(l1)  # [1, 2, 3, 4]
```

**4.2列表的索引切片**

```Python
l1 = ['a', 'b', '太白', 3, 666]
print(l1[0])  # 'a'
print(l1[-1])  # 666
print(l1[1:3])  # ['b', '太白']
print(l1[:-1])  # ['a', 'b', '太白', 3]
print(l1[::2])  # ['a', '太白', 666]
print(l1[::-1])  # [666, 3, '太白', 'b', 'a']
```

**4.3增**

```python
# append 追加，给列表的最后面追加一个元素
l = [1, 2, 'a']
l.append(666)
print(l) # [1, 2, 'a', 666]

# insert  插入在列表的任意位置插入元素
l = [1, 2, 'a']
l.insert(1,'太白')
print(l) # [1, '太白', 2, 'a']

# extend  迭代着追加，在列表的最后面迭代着追加一组数据
l = [1, 2, 'a']
l.extend('太白a')
print(l)  #[1, 2, 'a', '太', '白', 'a']
```

**4.4 删**

```Python
# pop  通过索引删除列表中对应的元素，该方法有返回值，返回值为删除的元素
l = ['太白', 'alex', 'WuSir', '女神']
ret = l.pop(1)
print(ret,l) # alex ['太白', 'WuSir', '女神']

# remove  通过元素删除列表中该元素
l = ['太白', 'alex', 'WuSir', '女神']
l.remove('alex')
print(l) # ['太白', 'WuSir', '女神']

# clear 清空列表
l = ['太白', 'alex', 'WuSir', '女神']
l.clear()
print(l) # []  

# del
#按照索引删除该元素
l = ['太白', 'alex', 'WuSir', '女神']
del l[2]
print(l) # ['太白', 'alex', '女神']

# 切片删除该元素
l = ['太白', 'alex', 'WuSir', '女神']
del l[1:]
print(l) # ['太白']

# 切片(步长)删除该元素
l = ['太白', 'alex', 'WuSir', '女神']
del l[::2]
print(l) # ['alex', '女神']
```

**4.5改**

```Python
# 按照索引改值
l = ['太白', 'alex', 'WuSir', '女神']
l[0] = '男神'
print(l) # ['男神', 'alex', 'WuSir', '女神']

# 按照切片改值(迭代着增加)
l = ['太白', 'alex', 'WuSir', '女神']
l[1:3] = 'abcdefg'
print(l) # ['太白', 'a', 'b', 'c', 'd', 'e', 'f', 'g', '女神'] 

# 按照切片(步长)改值(必须一一对应)
l = ['太白', 'alex', 'WuSir', '女神']
l[::2] = '对应'
print(l) # ['对', 'alex', '应', '女神']
```

- count（数）（方法统计某个元素在列表中出现的次数）
- index（方法用于从列表中找出某个值第一个匹配项的索引位置）
- sort （方法用于在原位置对列表进行排序）。
- reverse （方法将列表中的元素反向存放）。

```Python
 #count
  a = ["q","w","q","r","t","y"]
 print(a.count("q")) # 6

#index
a = ["q","w","r","t","y"]
print(a.index("r"))  #2

#sort 
a = [2,1,3,4,5]
a.sort()# 他没有返回值，所以只能打印a
print(a)#[1, 2, 3, 4, 5]

a.reverse()#他也没有返回值，所以只能打印a
print(a)#[5, 4, 3, 2, 1]

#列表也可以相加与整数相乘
l1 = [1, 2, 3]
l2 = [4, 5, 6]
# print(l1+l2)  # [1, 2, 3, 4, 5, 6]
print(l1*3)  # [1, 2, 3, 1, 2, 3, 1, 2, 3]
```

**4.6嵌套**

```python 
li  = ['taibai',18,'武藤兰',['alex','egon','89'],23]
#找藤字
print(li[2][1])
#将taibai的首字母大写
print(li[0],capitalize())

```

应用：

​		你需要存储大量的数据，且需要这些数据有序的时候。

​		制定一些特殊的数据群体：按顺序，按规则，自定制设计数据。

##### 5、元祖tuple

对于容器型数据类型list，无论谁都可以对其增删改查，那么有一些重要的数据放在list中是不安全的，所以需要一种容器类的数据类型存放重要的数据，创建之初只能查看而不能增删改，这种数据类型就是元组。**元祖数据是不可以增删查改只能查看，但是对于元祖内部的列表之类的数据是可以修改，也就是说元祖中的‘儿子’不可修改，但是‘孙子’可以修改**

**元祖的切片**

```Python
tu1 = ('a', 'b', '太白', 3, 666)
print(tu1[0])  # 'a'
print(tu1[-1])  # 666
print(tu1[1:3])  # ('b', '太白')
print(tu1[:-1])  # ('a', 'b', '太白', 3)
print(tu1[::2])  # ('a', '太白', 666)
print(tu1[::-1])  # (666, 3, '太白', 'b', 'a')
```

**元组的for循环查找**

```python
# 可以利用for循环查询

tu1 = ('a', 'b', '太白', 3, 666)
for i in tu1:
    print(i)
```

**range（起点，终点，步长）**

```python 
for i in range(0,10):
    print(i)  #0123456789
```

**join可迭代对象**

s.join()中的s表示的是这个使用什么字符连接

```python 
a = 'apple'
b = '_'.join(a)
print(b)
#a_p_p_l_e
```

##### 6、字典dict  用{}来，以键值对的方式对存储

目前已经学习到的容器型数据类型只有list，那么list够用？他有什么缺点呢？

  1. 列表可以存储大量的数据类型，但是如果数据量大的话，他的查询速度比较慢。

2. 列表只能按照顺序存储，数据与数据之间关联性不强。

所以针对于上的缺点，说咱们需要引入另一种容器型的数据类型，解决上面的问题，这就需要dict字典。

数据类型可以按照多种角度进行分类，就跟咱们人一样，人按照地域可以划分分为亚洲人，欧洲人，美洲人等，但是按照肤色又可以分为白种人，黄种人，黑种人，等等，数据类型可以按照不同的角度进行分类，先给大家按照可变与不可变的数据类型的分类：

- 不可变（可哈希）的数据类型：int，str，bool，tuple。

- 可变（不可哈希）的数据类型：list，dict，set。

字典是Python语言中的映射类型，他是**以{}括起来，里面的内容是以键值对的形式储存的：**

  **Key: 不可变（可哈希）的数据类型.并且键是唯一的，不重复的。**

  **Value:任意数据(int，str，bool，tuple，list，dict，set)，包括后面要学的实例对象等。**

　在Python3.5版本（包括此版本）之前，字典是无序的。

　在Python3.6版本之后，**字典会按照初建字典时的顺序排列(即第一次插入数据的顺序排序)。**

　当然，字典也有缺点：他的缺点就是内存消耗巨大。

**字典的查询速度非常快，简单解释一下原因**：字典的键值对会存在一个散列表（稀疏数组）这样的空间中，每一个单位称作一个表元，表元里面记录着key：value,如果你想要找到这个key对应的值，先要对这个key进行hash获取一串数字咱们简称为门牌号（非内存地址），然后通过门牌号，确定表元，对比查询的key与被锁定的key是否相同，如果相同，将值返回，如果不同，报错。

**6.1 创建字典**

```python
# 方式1:
dic = dict((('one', 1),('two', 2),('three', 3)))
# dic = dict([('one', 1),('two', 2),('three', 3)])
print(dic)  # {'one': 1, 'two': 2, 'three': 3}


# 方式2:
dic = dict(one=1,two=2,three=3)
print(dic)  # {'one': 1, 'two': 2, 'three': 3}


# 方式3:
dic = dict({'one': 1, 'two': 2, 'three': 3})
print(dic)  # {'one': 1, 'two': 2, 'three': 3}

# 方式5: 后面会讲到先了解
dic = dict(zip(['one', 'two', 'three'],[1, 2, 3]))
print(dic)

# 方式6: 字典推导式 后面会讲到
# dic = { k: v for k,v in [('one', 1),('two', 2),('three', 3)]}
# print(dic)

# 方式7:利用fromkey后面会讲到。
# dic = dict.fromkeys('abcd','太白')
# print(dic)  # {'a': '太白', 'b': '太白', 'c': '太白', 'd': '太白'}
```

**6.2字典合法性**

```Python 
# 合法
dic = {123: 456, 
       True: 999, 
       "id": 1,
       "name": 'sylar',
       "age": 18, 
       "stu": ['帅哥', '美⼥'],
       (1, 2, 3): '麻花藤'}
print(dic[123])#456
print(dic[True])#999
print(dic['id'])#1
print(dic['stu'])#['帅哥', '美⼥']
print(dic[(1, 2, 3)])#麻花藤

# 不合法
# dic = {[1, 2, 3]: '周杰伦'} # list是可变的. 不能作为key
# dic = {{1: 2}: "哈哈哈"} # dict是可变的. 不能作为key
dic = {{1, 2, 3}: '呵呵呵'} # set是可变的, 不能作为key
```

 **接下来咱们就进入字典的学习环节，字典对于咱们小白来说可能相对于列表是不好理解的，因为列表是有序的一个一个排列的，但是字典的键值对对于大家来说是比较陌生的，所以咱们可以把字典比喻成一个公寓，公寓里面有N多个房间，房间号就是键，房间里面具体的东西就值：比如房间001号：对应的房间住着两个人，也就是2person，简称2P，房间99号：3P， 房间78号：有人还有小动物....... 这样，咱们就能通过房间号（也就是键）找到对应的房间，查看里面的内容，也就是值。**

**增**

```Python
# 通过键值对直接增加
dic = {'name': '太白', 'age': 18}
dic['weight'] = 75 # 没有weight这个键，就增加键值对
print(dic) # {'name': '太白', 'age': 18, 'weight': 75}
dic['name'] = 'barry' # 有name这个键，就成了字典的改值
print(dic) # {'name': 'barry', 'age': 18, 'weight': 75}

# setdefault
dic = {'name': '太白', 'age': 18}
dic.setdefault('height',175) # 没有height此键，则添加
print(dic) # {'name': '太白', 'age': 18, 'height': 175}
dic.setdefault('name','barry') # 有此键则不变
print(dic) # {'name': '太白', 'age': 18, 'height': 175}
#它有返回值
dic = {'name': '太白', 'age': 18}
ret = dic.setdefault('name')
print(ret)  # 太白
```

**删**

```Python 
# pop 通过key删除字典的键值对，有返回值，可设置返回值。
dic = {'name': '太白', 'age': 18}
# ret = dic.pop('name')
# print(ret,dic) # 太白 {'age': 18}
ret1 = dic.pop('n',None)
print(ret1,dic) # None {'name': '太白', 'age': 18}

#popitem 3.5版本之前，popitem为随机删除，3.6之后为删除最后一个，有返回值
dic = {'name': '太白', 'age': 18}
ret = dic.popitem()
print(ret,dic) # ('age', 18) {'name': '太白'}

#clear 清空字典
dic = {'name': '太白', 'age': 18}
dic.clear()
print(dic) # {}

# del
# 通过键删除键值对
dic = {'name': '太白', 'age': 18}
del dic['name']
print(dic) # {'age': 18}
#删除整个字典
del dic
```

**改**

```Python
# 通过键值对直接改
dic = {'name': '太白', 'age': 18}
dic['name'] = 'barry'
print(dic) # {'name': 'barry', 'age': 18}

# update
dic = {'name': '太白', 'age': 18}
dic.update(sex='男', height=175)
print(dic) # {'name': '太白', 'age': 18, 'sex': '男', 'height': 175}

dic = {'name': '太白', 'age': 18}
dic.update([(1, 'a'),(2, 'b'),(3, 'c'),(4, 'd')])
print(dic) # {'name': '太白', 'age': 18, 1: 'a', 2: 'b', 3: 'c', 4: 'd'}

dic1 = {"name":"jin","age":18,"sex":"male"}
dic2 = {"name":"alex","weight":75}
dic1.update(dic2)
print(dic1) # {'name': 'alex', 'age': 18, 'sex': 'male', 'weight': 75}
print(dic2) # {'name': 'alex', 'weight': 75} 
```

**查**

```Python
# 通过键查询
# 直接dic[key](没有此键会报错)
dic = {'name': '太白', 'age': 18}
print(dic['name']) # 太白

# get
dic = {'name': '太白', 'age': 18}
v = dic.get('name')
print(v) # '太白'
v = dic.get('name1')
print(v) # None
v = dic.get('name2','没有此键')
print(v) # 没有此键 


keys()
dic = {'name': '太白', 'age': 18}
print(dic.keys()) # dict_keys(['name', 'age']) 

values()
dic = {'name': '太白', 'age': 18}
print(dic.values()) # dict_values(['太白', 18])

items()
dic = {'name': '太白', 'age': 18}
print(dic.items()) # dict_items([('name', '太白'), ('age', 18)])
```

**formkeys**

```python 
dic = dict.fromkeys('abcd','太白')
print(dic) # {'a': '太白', 'b': '太白', 'c': '太白', 'd': '太白'}

dic = dict.fromkeys([1, 2, 3],'太白')
print(dic) # {1: '太白', 2: '太白', 3: '太白'} 
```

字典的嵌套是非常重要的知识点，这个必须要建立在熟练使用字典的增删改查的基础上，而且字典的嵌套才是咱们在工作中经常会遇到的字典，工作中遇到的字典不是简简单单一层，而就像是葱头一样，一层接一层，但一般都是很有规律的嵌套，那么接下来我们就学习一下字典的嵌套：

```python 
dic = {
    'name':'汪峰',
    'age':48,
    'wife':[{'name':'国际章','age':38}],
    'children':{'girl_first':'小苹果','girl_second':'小怡',
                'girl_three':'顶顶'}
}

#1. 获取汪峰的名字。
# 这个比较简单，汪峰就是dic的一个键对应的值，我们通过这个key就可以获取到汪峰这个值。
print(dic['name'])
#2.获取这个字典：{'name':'国际章','age':38}。
#想要获取这个字典，先要看字典从属于谁？这个字典从属于一个列表，而这个列表是字典wife对应的键，所以咱们应该先通过wife获取到对应的这个列表，然后通过这个列表按照所以取值取到对应的这个字典
print(dic['wife'][0])
#3. 获取汪峰妻子的名字。
#想要获取汪峰妻子的名字：国际章，那么他是一个字典的键对应的值，所以我们通过'name'这个键就可以获取到对应的值，这个题的难点是获取到这个小字典，而上一个题我们已经获取了这个小字典，所以在上面的基础上再执行就可以了。
print(dic['wife'][0]['name'])
#4. 获取汪峰的第三个孩子名字。
#汪峰的孩子们是在一个字典中的，你要想获取汪峰的第三个孩子，你应该先获取到它从属于的这个字典，然后再通过这个字典获取第三个孩子的名字。
print(dic['children']['girl_three'])
```

##### 7、集合set

**集合是无序的，不重复的数据集合**，它里面的元素是可哈希的(不可变类型)，但是集合本身是不可哈希（所以集合做不了字典的键）的。以下是集合最重要的两点：

　　**去重**，**把一个列表变成集合**，就自动去重了。

　　关系测试，测试两组数据之前的交集、差集、并集等关系。

**7.1集合的创建**

```Python
set1 = set({1,2,'barry'})
set2 = {1,2,'barry'}
print(set1,set2)  # {1, 2, 'barry'} {1, 2, 'barry'}
```

**7.2集合的增**

```Python
set1 = {'alex','wusir','ritian','egon','barry'}
set1.add('景女神')
print(set1)#{'alex', 'wusir', '景女神', 'barry', 'ritian', 'egon'}

#update：迭代着增加
set1.update('A')
#{'alex', 'wusir', '景女神', 'barry', 'ritian', 'A', 'egon'}
print(set1)
set1.update('老师')
#{'师', '老', 'alex', 'wusir', '景女神', 'barry', 'ritian', 'A', 'egon'}
print(set1)
set1.update([1,2,3])
#{'师', 1, 2, 3, '老', 'alex', 'wusir', '景女神', 'barry', 'ritian', 'A', 'egon'}
print(set1)
```

**7.3集合的删**

```python
set1 = {'alex','wusir','ritian','egon','barry'}

set1.remove('alex')  # 删除一个元素
print(set1)
#{'egon', 'wusir', 'barry', 'ritian'}
set1.pop()  # 随机删除一个元素
print(set1)
#{'wusir', 'barry', 'ritian'}
set1.clear()  # 清空集合
print(set1)
#set()
del set1  # 删除集合
print(set1)
```

**7.4交集。（& 或者 intersection）**

```python 
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}
print(set1 & set2)  # {4, 5}
print(set1.intersection(set2))  # {4, 5}
```

　　**7.5并集。（| 或者 union）**

```python 
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}
print(set1 | set2)  # {1, 2, 3, 4, 5, 6, 7,8}

print(set2.union(set1))  # {1, 2, 3, 4, 5, 6, 7,8}
```

　　**7.6 差集。（- 或者 difference）**

```python
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}
print(set1 - set2)  # {1, 2, 3}
print(set1.difference(set2))  # {1, 2, 3}
```

 　**7.7反交集。 （^ 或者 symmetric_difference）**

```python
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}
print(set1 ^ set2)  # {1, 2, 3, 6, 7, 8}
print(set1.symmetric_difference(set2))  # {1, 2, 3, 6, 7, 8}
```

　　**7.8子集与超集**

```python
set1 = {1,2,3}
set2 = {1,2,3,4,5,6}

print(set1 < set2)
print(set1.issubset(set2))  # 这两个相同，都是说明set1是set2子集。

print(set2 > set1)
print(set2.issuperset(set1))  # 这两个相同，都是说明set2是set1超集。
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

**7.9 frozenset不可变集合，让集合变成不可变类型。**

```python 
s = frozenset('barry')
print(s,type(s))  # frozenset({'a', 'y', 'b', 'r'}) <class 'frozenset'>
```

# 

| 数据类型 | 名称   | 示例             |
| -------- | ------ | ---------------- |
| int      | 整型   | 10               |
| float    | 浮点型 | 3.12             |
| bool     | 布尔型 | True，False      |
| str      | 字符串 | ‘F’ ‘二哥’       |
| list     | 列表   | [1,2,3,4,'A']    |
| dict     | 字典   | {'name'：'二哥'} |
| set      | 集合   | {1,2,'S'}        |
| tuple    | 元祖   | （1，2，3，4）   |

# 

#### 四、运算符

运算符分为简单运算符和逻辑运算符两种

 

##### 1、简单运算符

| 操作符 | 名称 | 示例               |
| ------ | ---- | ------------------ |
| +      | 加   | 1 + 1              |
| -      | 减   | 2 - 1              |
| *      | 乘   | 3 * 4              |
| /      | 除   | 11/3 = 3.666666665 |
| //     | 整除 | 3//4 =0            |
| %      | 取余 | 3%4 = 0...余3      |
| **     | 幂   | 3**2 = 9           |

 

##### 2、 比较运算符：

在Python中返回为True 和False两种答案

| 操作符 | 名称     | 示例   |
| ------ | -------- | ------ |
| >      | 大于     | 2 > 1  |
| >=     | 大于等于 | 4 >= 1 |
| <      | 小于     | 1 < 2  |
| <=     | 小于等于 | 1 <= 2 |
| ==     | 等于     | 1 == 1 |
| !=     | 不等于   | 1 != 2 |

##### 3、逻辑运算符：

返回值为True and False

| 操作符 | 名称 | 示例             |                    |
| ------ | ---- | ---------------- | ------------------ |
| and    | 与   | （2>1) and (3>7) | 两个为真才为真     |
| or     | 或   | (1>3)or(2<9)     | 一个为真就是真     |
| not    | 非   | not(2>1)         | 真就是假，假就是真 |

 逻辑运算符之间存在有优先级关系：

（）> not > and > or

```Python
x or y #如果x非0则返回x，反之则返回y
x and y # 如果X为true则返回y反之则返回x
int →bool #非0的是true，0为false
bool → int # false 是0 true是1

#示例：
print(0 or 4 and 3 or 2)  #答案为3
'''
分解步骤：
0 or 4 ：0是0 返回y也就是4
4 and 3 ：4是非0 返回y 就是3 
3 or 2 ：2是非0 返回x 就是3因此答案为3
'''
 
```

##### 4 位运算符

| 操作符 | 名称     | 示例                                                 |
| ------ | -------- | ---------------------------------------------------- |
| ~      | 按位取反 | ~1 =0                                                |
| &      | 按位与   | 1&1 = 11&0 = 00&0= 00&1 = 0                          |
| \|     | 按位或   | 1\|1=11\|0 = 10\|1 = 10\|0= 0                        |
| ^      | 按位异或 | 1^1 = 01 ^ 0=10^1 =10^0 =0                           |
| <<     | 左移     | 4<<2 指的是将4先转换为二进制后向左移动两位之后的结果 |
| >>     | 右移     | 4 >>2 将4转为二进制想有移动两位之后的结果            |

 

##### 5、 三元运算符

| 操作符 | 名称   | 示例               |
| ------ | ------ | ------------------ |
| is     | 是     | 'hello' is 'hello' |
| not is | 不是   | 3 not is 5         |
| in     | 存在   | 5 in [1,2,3,4,5,6] |
| not in | 不存在 | 2 not in [1,4,5]   |

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
x ,y = 4,5

if x < y:
    small = x
else:
    small = y
print(small)# 4

#三元运算
small =  x if x < y else y



letters=['A','B','C','D','E','F','G']

if 'A' in letters:
    print('A' + ' exists') 
if 'h' not in letters:
    print('h' + ' not exists')

# A exists # h not exists


a = 'hello'
b='hello'
print(a is b, a == b)#True True
a=["hello"]
b=["hello"]
print(a is b, a == b)#False True

is 和not is是对比的变量的内存地址
== 与!=对比的是值
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

也就是说这两个变量若是地址不可变的类型就相同，如果地址可变就有区别。

 

#### 五、输入输出函数

##### 1、 input函数

```
name = input('请输入你的名字’)
print(name)

print(’我的名字是'+name',我的年龄是'+age+'岁’)
```

1、等待输入。

2、将输入的内容赋值给了变量.

3、input出来的数据类型都是str（字符串）。

 

##### 2、print()函数

```
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
1.将对象以字符串表示的方式格式化输出到流文件对象file里。其中所有非关键字参数都按str()方式进行转换为字符串输出;

2.关键字参数sep是实现分隔符，比如多个参数输出时想要输出中间的分隔字符;

3.关键字参数end是输出结束时的字符，默认是换行符\n ;

4.关键字参数file是定义流输出的文件，可以是标准的系统输出sys. stdout，也可以重定义为别的文件;

5.关键字参数flush是立即把内容输出到流文件，不作缓存。
```

格式化输出%：

1 %为占位符 s是字符串型 d是数数值型

2、需要输入的地方为 % + 这个值的类型

例子：msg = "名字： %s" %(name)

3、若要程序单纯表达% 需要使用%% 即可。

#### 六、判断、循环结构

##### 1、for 

```python 
for i in range(10):
	pass
```

##### 2、while

```Python
while 条件：
	语句
```

##### 3、if

```Python
if 条件：
	语句1
elif 条件2:
	语句2
	.
	.
	.
else：
	语句n
```

