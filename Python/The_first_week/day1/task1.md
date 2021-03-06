# 思考题

## 1.Python是怎么诞生的，Python之父是谁

自从20世纪90年代初Python语言诞生至今，它已被逐渐广泛应用于系统管理任务的处理和[Web](https://baike.baidu.com/item/Web/150564)编程。

Python的创始人为荷兰人吉多·范罗苏姆（Guido van Rossum）。1989年圣诞节期间，在[阿姆斯特丹](https://baike.baidu.com/item/阿姆斯特丹/2259975)，Guido为了打发[圣诞节](https://baike.baidu.com/item/圣诞节/127881)的无趣，决心开发一个新的脚本解释程序，作为ABC语言的一种继承。之所以选中Python（大蟒蛇的意思）作为该编程语言的名字，是取自英国20世纪70年代首播的电视喜剧《蒙提·派森的飞行马戏团》（Monty Python's Flying Circus）。

ABC是由Guido参加设计的一种[教学](https://baike.baidu.com/item/教学)语言。就Guido本人看来，ABC这种语言非常优美和强大，是专门为非专业程序员设计的。但是ABC语言并没有成功，究其原因，Guido认为是其非开放造成的。Guido决心在Python中避免这一错误。同时，他还想实现在ABC中闪现过但未曾实现的东西。

就这样，Python在Guido手中诞生了。可以说，Python是从ABC发展起来，主要受到了[Modula-3](https://baike.baidu.com/item/Modula-3/17009923)（另一种相当优美且强大的语言，为小型团体所设计的）的影响。并且结合了[Unix shell](https://baike.baidu.com/item/Unix shell)和[C](https://baike.baidu.com/item/C/7252092)的习惯。

Python已经成为最受欢迎的[程序设计语言](https://baike.baidu.com/item/程序设计语言/2317999)之一。自从2004年以后，python的使用率呈线性增长。Python 2于2000年10月16日发布，稳定版本是Python 2.7。Python 3于2008年12月3日发布，不完全兼容Python 2。 2011年1月，它被[TIOBE](https://baike.baidu.com/item/TIOBE)编程语言[排行榜](https://baike.baidu.com/item/排行榜/4895)评为2010年度语言。

~~以上CTRL\+ C及CTRL\+ V自百度百科~~

## 2.Python和C++（C）的区别在哪，为什么要学习Python而非C++

1.Python是用C写的，运行速度自然比C（C++）慢

2.Python用缩进区分语句关系，C用各种括号引号

*1、语言类型*

*Python是一种基于解释器的语言，du解释器会zhi逐行读取代码；首先将daoPython编译为字zhuan节码，然后由大型shuC程序解释。*

*C是一种编译语言，完整的源代码将直接编译为机器代码，由CPU直接执行。*

*2、内存管理*

*Python使用自动垃圾收集器进行内存管理。*

*在C语言中，程序员必须自己进行内存管理。*

*3、应用*

*Python是一种通用编程语言，一个多范式。它主要支持面向对象编程，程序编程，函数编程。*

*C是结构化编程语言。允许使用函数，选择（if / else等），迭代（循环）。它主要用于硬件相关的应用程序。*

*4、速度*

*Python编程语言因为历史原因，有一个GIL锁，导致其对多线程支持不够好，运行速度较慢；而C语言很快，C语言是比较底层的语言，运行效率上要优于Python。*

*5、复杂些不一样*

*在Python中，不需要声明变量类型。而在C中，必须声明变量类型。*

*Python程序更易于学习，编写和阅读。而C程序语法比Python更难。*

*Python中的测试和调试更容易；而在C中测试和调试更难。*

~~以上斜体来自百度知道~~

## 3.相较于Python2，Python3做了哪些大的改进？

作者：王猫猫
链接：https://www.zhihu.com/question/19698598/answer/12704353
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。



\>  1. print不再是语句，而是函数，比如原来是 print 'abc' 现在是 print('abc')
但是 python2.6+ 可以使用 from __future__ import print_function 来实现相同功能
\>  2. 在Python 3中，没有旧式类，只有新式类，也就是说不用再像这样 class Foobar(object): pass 显式地子类化object
但是最好还是加上. 主要区别在于 old-style 是 classtype 类型而 new-style 是 type类型
\>  3. 原来1/2（两个整数相除）结果是0，现在是0.5了
python 2.2+ 以上都可以使用 from __future__ import division 实现改特性, 同时注意 // 取代了之前的 / 运算
\>  4. 新的字符串格式化方法format取代%
错误, 从 python2.6+ 开始已经在str和unicode中有该方法, 同时 python3依然支持 % 算符
\>  6. xrange重命名为range
同时更改的还有一系列内置函数及方法, 都返回迭代器对象, 而不是列表或者 元组, 比如 filter, map, dict.items 等
\>  7. !=取代  <   >  
python2 也很少有人用  <  >  所以不算什么修改
\>  8. long重命名为int
不完全对, python3 彻底废弃了 long+int 双整数实现的方法, 统一为 int , 支持高精度整数运算.
\>  9. except Exception, e变成except (Exception) as e
只有 python2.5 及以下版本不支持该语法. python2.6 是支持的. 不算新东西
\>  10. exec变成函数
类似 print() 的变化, 之前是语句.

~~以上来自知乎王猫猫的回答~~

# 练习题

### 1.怎样对python中的代码进行注释？

用#注释整行，用'''   '''  和  """   """注释中间内容

## 2.python有哪些运算符，这些运算符的优先级是怎样的？

| 运算符                   | 描述                                                   |
| :----------------------- | :----------------------------------------------------- |
| **                       | 指数 (最高优先级)                                      |
| ~ + -                    | 按位翻转, 一元加号和减号 (最后两个的方法名为 +@ 和 -@) |
| * / % //                 | 乘，除，取模和取整除                                   |
| + -                      | 加法减法                                               |
| >> <<                    | 右移，左移运算符                                       |
| &                        | 位 'AND'                                               |
| ^ \|                     | 位运算符                                               |
| <= < > >=                | 比较运算符                                             |
| <> == !=                 | 等于运算符                                             |
| = %= /= //= -= += *= **= | 赋值运算符                                             |
| is is not                | 身份运算符                                             |
| in not in                | 成员运算符                                             |
| not and or               | 逻辑运算符                                             |

## 3.python 中 `is`, `is not` 与 `==`, `!=` 的区别是什么？

is,is not 比较的是两个变量的内存地址

= ， ！= 比较的是两个变量的值

## 4.python 中包含哪些数据类型？这些数据类型之间如何转换？

整型，浮点型，布尔型

- 转换为整型 int(x, base=10)
- 转换为字符串 str(object=' ')
- 转换为浮点型 float(x)
