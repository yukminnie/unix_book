
**Table of Contents**

- [Python语言特性](#python语言特性)
    - [1 Python的函数参数传递](#1-python的函数参数传递)
    - [2 Python中的元类(metaclass)](#2-python中的元类metaclass)
    - [3 @staticmethod和@classmethod](#3-staticmethod和classmethod)
    - [4 类变量和实例变量](#4-类变量和实例变量)
    - [5 Python自省](#5-python自省)
    - [6 字典推导式](#6-字典推导式)
    - [7 Python中单下划线和双下划线](#7-python中单下划线和双下划线)
    - [8 字符串格式化:%和.format](#8-字符串格式化和format)
    - [9 迭代器和生成器](#9-迭代器和生成器)
    - [10 `*args` and `**kwargs`](#10-args-and-kwargs)
    - [11 面向切面编程AOP和装饰器](#11-面向切面编程aop和装饰器)
    - [12 鸭子类型](#12-鸭子类型)
    - [13 Python中重载](#13-python中重载)
    - [14 新式类和旧式类](#14-新式类和旧式类)
    - [15 `__new__`和`__init__`的区别](#15-__new__和__init__的区别)
    - [16 单例模式](#16-单例模式)
        - [1 使用`__new__`方法](#1-使用__new__方法)
        - [2 共享属性](#2-共享属性)
        - [3 装饰器版本](#3-装饰器版本)
        - [4 import方法](#4-import方法)
    - [17 Python中的作用域](#17-python中的作用域)
    - [18 GIL线程全局锁](#18-gil线程全局锁)
    - [19 协程](#19-协程)
    - [20 闭包](#20-闭包)
    - [21 lambda函数](#21-lambda函数)
    - [22 Python函数式编程](#22-python函数式编程)
    - [23 Python里的拷贝](#23-python里的拷贝)
    - [24 Python垃圾回收机制](#24-python垃圾回收机制)
        - [1 引用计数](#1-引用计数)
        - [2 标记-清除机制](#2-标记-清除机制)
        - [3 分代技术](#3-分代技术)
    - [25 Python的List](#25-python的list)
    - [26 Python的is](#26-python的is)
    - [27 read,readline和readlines](#27-readreadline和readlines)
    - [28 Python2和3的区别](#28-python2和3的区别)
    - [29 super.`__init__`()](#29-super-init)
    - [30 range-and-xrange](#30-range-and-xrange)
- [操作系统](#操作系统)
    - [1 select,poll和epoll](#1-selectpoll和epoll)
    - [2 调度算法](#2-调度算法)
    - [3 死锁](#3-死锁)
    - [4 程序编译与链接](#4-程序编译与链接)
        - [1 预处理](#1-预处理)
        - [2 编译](#2-编译)
        - [3 汇编](#3-汇编)
        - [4 链接](#4-链接)
    - [5 静态链接和动态链接](#5-静态链接和动态链接)
    - [6 虚拟内存技术](#6-虚拟内存技术)
    - [7 分页和分段](#7-分页和分段)
        - [分页与分段的主要区别](#分页与分段的主要区别)
    - [8 页面置换算法](#8-页面置换算法)
    - [9 边沿触发和水平触发](#9-边沿触发和水平触发)
- [数据库](#数据库)
    - [1 事务](#1-事务)
    - [2 数据库索引](#2-数据库索引)
    - [3 Redis原理](#3-redis原理)
    - [4 乐观锁和悲观锁](#4-乐观锁和悲观锁)
    - [5 MVCC](#5-mvcc)
    - [6 MyISAM和InnoDB](#6-myisam和innodb)
- [网络](#网络)
    - [1 三次握手](#1-三次握手)
    - [2 四次挥手](#2-四次挥手)
    - [3 ARP协议](#3-arp协议)
    - [4 urllib和urllib2的区别](#4-urllib和urllib2的区别)
    - [5 Post和Get](#5-post和get)
    - [6 Cookie和Session](#6-cookie和session)
    - [7 apache和nginx的区别](#7-apache和nginx的区别)
    - [8 网站用户密码保存](#8-网站用户密码保存)
    - [9 HTTP和HTTPS](#9-http和https)
    - [10 XSRF和XSS](#10-xsrf和xss)
    - [11 幂等 Idempotence](#11-幂等-idempotence)
    - [12 RESTful架构(SOAP,RPC)](#12-restful架构soaprpc)
    - [13 SOAP](#13-soap)
    - [14 RPC](#14-rpc)
    - [15 CGI和WSGI](#15-cgi和wsgi)
    - [16 中间人攻击](#16-中间人攻击)
    - [17 c10k问题](#17-c10k问题)
    - [18 socket](#18-socket)
    - [19 浏览器缓存](#19-浏览器缓存)
    - [20 HTTP1.0和HTTP1.1](#20-http10和http11)
    - [21 Ajax](#21-ajax)
- [*NIX](#nix)
    - [unix进程间通信方式(IPC)](#unixipc)
- [数据结构](#数据结构)
    - [1 红黑树](#1-红黑树)
- [编程题](#编程题)
    - [1 台阶问题/斐波纳挈](#1-台阶问题斐波纳挈)
    - [2 变态台阶问题](#2-变态台阶问题)
    - [3 矩形覆盖](#3-矩形覆盖)
    - [4 杨氏矩阵查找](#4-杨氏矩阵查找)
    - [5 去除列表中的重复元素](#5-去除列表中的重复元素)
    - [6 链表成对调换](#6-链表成对调换)
    - [7 创建字典的方法](#7-创建字典的方法)
        - [1 直接创建](#1-直接创建)
        - [2 工厂方法](#2-工厂方法)
        - [3 fromkeys()方法](#3-fromkeys方法)
    - [8 合并两个有序列表](#8-合并两个有序列表)
    - [9 交叉链表求交点](#9-交叉链表求交点)
    - [10 二分查找](#10-二分查找)
    - [11 快排](#11-快排)
    - [12 找零问题](#12-找零问题)
    - [13 广度遍历和深度遍历二叉树](#13-广度遍历和深度遍历二叉树)
    - [14 二叉树节点](#14-)
    - [15 层次遍历](#15-)
    - [16 深度遍历](#16-)
    - [17 前中后序遍历](#17-前中后序遍历)
    - [18 求最大树深](#18-求最大树深)
    - [19 求两棵树是否相同](#19-求两棵树是否相同)
    - [20 前序中序求后序](#20-前序中序求后序)
    - [21 单链表逆置](#21-单链表逆置)
    - [22 两个字符串是否是变位词](#22-两个字符串是否是变位词)

# Python语言特性

## 1 Python的函数参数传递

看两个例子:

```python
a = 1
def fun(a):
    a = 2
fun(a)
print a  # 1
```

```python
a = []
def fun(a):
    a.append(1)
fun(a)
print a  # [1]
```

所有的变量都可以理解是内存中一个对象的“引用”，或者，也可以看似c中void*的感觉。

通过`id`来看引用`a`的内存地址可以比较理解：

```python
a = 1
def fun(a):
    print "func_in",id(a)   # func_in 41322472
    a = 2
    print "re-point",id(a), id(2)   # re-point 41322448 41322448
print "func_out",id(a), id(1)  # func_out 41322472 41322472
fun(a)
print a  # 1
```

注：具体的值在不同电脑上运行时可能不同。

可以看到，在执行完`a = 2`之后，`a`引用中保存的值，即内存地址发生变化，由原来`1`对象的所在的地址变成了`2`这个实体对象的内存地址。

而第2个例子`a`引用保存的内存值就不会发生变化：

```python
a = []
def fun(a):
    print "func_in",id(a)  # func_in 53629256
    a.append(1)
print "func_out",id(a)     # func_out 53629256
fun(a)
print a  # [1]
```

这里记住的是类型是属于对象的，而不是变量。而对象有两种,“可更改”（mutable）与“不可更改”（immutable）对象。在python中，strings, tuples, 和numbers是不可更改的对象，而list,dict等则是可以修改的对象。(这就是这个问题的重点)

当一个引用传递给函数的时候,函数自动复制一份引用,这个函数里的引用和外边的引用没有半毛关系了.所以第一个例子里函数把引用指向了一个不可变对象,当函数返回的时候,外面的引用没半毛感觉.而第二个例子就不一样了,函数内的引用指向的是可变对象,对它的操作就和定位了指针地址一样,在内存里进行修改.

如果还不明白的话,这里有更好的解释: http://stackoverflow.com/questions/986006/how-do-i-pass-a-variable-by-reference

## 2 Python中的元类(metaclass)

这个非常的不常用,但是像ORM这种复杂的结构还是会需要的,详情请看:http://stackoverflow.com/questions/100003/what-is-a-metaclass-in-python

## 3 @staticmethod和@classmethod

Python其实有3个方法,即静态方法(staticmethod),类方法(classmethod)和实例方法,如下:

```python
def foo(x):
    print "executing foo(%s)"%(x)

class A(object):
    def foo(self,x):
        print "executing foo(%s,%s)"%(self,x)

    @classmethod
    def class_foo(cls,x):
        print "executing class_foo(%s,%s)"%(cls,x)

    @staticmethod
    def static_foo(x):
        print "executing static_foo(%s)"%x

a=A()

```

这里先理解下函数参数里面的self和cls.这个self和cls是对类或者实例的绑定,对于一般的函数来说我们可以这么调用`foo(x)`,这个函数就是最常用的,它的工作跟任何东西(类,实例)无关.对于实例方法,我们知道在类里每次定义方法的时候都需要绑定这个实例,就是`foo(self, x)`,为什么要这么做呢?因为实例方法的调用离不开实例,我们需要把实例自己传给函数,调用的时候是这样的`a.foo(x)`(其实是`foo(a, x)`).类方法一样,只不过它传递的是类而不是实例,`A.class_foo(x)`.注意这里的self和cls可以替换别的参数,但是python的约定是这俩,还是不要改的好.

对于静态方法其实和普通的方法一样,不需要对谁进行绑定,唯一的区别是调用的时候需要使用`a.static_foo(x)`或者`A.static_foo(x)`来调用.

|\\|实例方法|类方法|静态方法|
|:--|:--|:--|:--|
|a = A()|a.foo(x)|a.class_foo(x)|a.static_foo(x)|
|A|不可用|A.class_foo(x)|A.static_foo(x)|

更多关于这个问题:http://stackoverflow.com/questions/136097/what-is-the-difference-between-staticmethod-and-classmethod-in-python

## 4 类变量和实例变量

```python
class Person:
    name="aaa"

p1=Person()
p2=Person()
p1.name="bbb"
print p1.name  # bbb
print p2.name  # aaa
print Person.name  # aaa
```

类变量就是供类使用的变量,实例变量就是供实例使用的.

这里`p1.name="bbb"`是实例调用了类变量,这其实和上面第一个问题一样,就是函数传参的问题,`p1.name`一开始是指向的类变量`name="aaa"`,但是在实例的作用域里把类变量的引用改变了,就变成了一个实例变量,self.name不再引用Person的类变量name了.

可以看看下面的例子:

```python
class Person:
    name=[]

p1=Person()
p2=Person()
p1.name.append(1)
print p1.name  # [1]
print p2.name  # [1]
print Person.name  # [1]
```

参考:http://stackoverflow.com/questions/6470428/catch-multiple-exceptions-in-one-line-except-block

## 5 Python自省

这个也是python彪悍的特性.

自省就是面向对象的语言所写的程序在运行时,所能知道对象的类型.简单一句就是运行时能够获得对象的类型.比如type(),dir(),getattr(),hasattr(),isinstance().

## 6 字典推导式

可能你见过列表推导时,却没有见过字典推导式,在2.7中才加入的:

```python
d = {key: value for (key, value) in iterable}
```

## 7 Python中单下划线和双下划线

```python
>>> class MyClass():
...     def __init__(self):
...             self.__superprivate = "Hello"
...             self._semiprivate = ", world!"
...
>>> mc = MyClass()
>>> print mc.__superprivate
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: myClass instance has no attribute '__superprivate'
>>> print mc._semiprivate
, world!
>>> print mc.__dict__
{'_MyClass__superprivate': 'Hello', '_semiprivate': ', world!'}
```

`__foo__`:一种约定,Python内部的名字,用来区别其他用户自定义的命名,以防冲突.

`_foo`:一种约定,用来指定变量私有.程序员用来指定私有变量的一种方式.

`__foo`:这个有真正的意义:解析器用`_classname__foo`来代替这个名字,以区别和其他类相同的命名.

详情见:http://stackoverflow.com/questions/1301346/the-meaning-of-a-single-and-a-double-underscore-before-an-object-name-in-python

或者: http://www.zhihu.com/question/19754941

## 8 字符串格式化:%和.format

.format在许多方面看起来更便利.对于`%`最烦人的是它无法同时传递一个变量和元组.你可能会想下面的代码不会有什么问题:

```
"hi there %s" % name
```

但是,如果name恰好是(1,2,3),它将会抛出一个TypeError异常.为了保证它总是正确的,你必须这样做:

```
"hi there %s" % (name,)   # 提供一个单元素的数组而不是一个参数
```

但是有点丑..format就没有这些问题.你给的第二个问题也是这样,.format好看多了.

你为什么不用它?

* 不知道它(在读这个之前)
* 为了和Python2.5兼容(譬如logging库建议使用`%`([issue #4](https://github.com/taizilongxu/interview_python/issues/4)))

http://stackoverflow.com/questions/5082452/python-string-formatting-vs-format

## 9 迭代器和生成器

这个是stackoverflow里python排名第一的问题,值得一看: http://stackoverflow.com/questions/231767/what-does-the-yield-keyword-do-in-python

这是中文版: http://taizilongxu.gitbooks.io/stackoverflow-about-python/content/1/README.html

## 10 `*args` and `**kwargs`

用`*args`和`**kwargs`只是为了方便并没有强制使用它们.

当你不确定你的函数里将要传递多少参数时你可以用`*args`.例如,它可以传递任意数量的参数:

```python
>>> def print_everything(*args):
        for count, thing in enumerate(args):
...         print '{0}. {1}'.format(count, thing)
...
>>> print_everything('apple', 'banana', 'cabbage')
0. apple
1. banana
2. cabbage
```

相似的,`**kwargs`允许你使用没有事先定义的参数名:

```python
>>> def table_things(**kwargs):
...     for name, value in kwargs.items():
...         print '{0} = {1}'.format(name, value)
...
>>> table_things(apple = 'fruit', cabbage = 'vegetable')
cabbage = vegetable
apple = fruit
```

你也可以混着用.命名参数首先获得参数值然后所有的其他参数都传递给`*args`和`**kwargs`.命名参数在列表的最前端.例如:

```
def table_things(titlestring, **kwargs)
```

`*args`和`**kwargs`可以同时在函数的定义中,但是`*args`必须在`**kwargs`前面.

当调用函数时你也可以用`*`和`**`语法.例如:

```python
>>> def print_three_things(a, b, c):
...     print 'a = {0}, b = {1}, c = {2}'.format(a,b,c)
...
>>> mylist = ['aardvark', 'baboon', 'cat']
>>> print_three_things(*mylist)

a = aardvark, b = baboon, c = cat
```

就像你看到的一样,它可以传递列表(或者元组)的每一项并把它们解包.注意必须与它们在函数里的参数相吻合.当然,你也可以在函数定义或者函数调用时用*.

http://stackoverflow.com/questions/3394835/args-and-kwargs


