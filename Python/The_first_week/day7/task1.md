**练习题**：

1、以下类定义中哪些是类属性，哪些是实例属性？

```
class C:
    num = 0
    def __init__(self):
        self.x = 4
        self.y = 5
        C.count = 6
```

num   .count是类属性，.x  .y是实例属性

2、怎么定义私有⽅法？

在 Python 中定义私有变量只需要在变量名或函数名前加上“__”两个下划线，那么这个函数或变量就会为私有的了。

3、尝试执行以下代码，并解释错误原因：

```
class C:
    def myFun():
        print('Hello!')
    c = C()
    c.myFun()
```

1.函数定义myFun时在后面的括号中应有self

2.缩进问题。原代码中c = C()及下一行代码缩进在class C语句中，因此找不到C类。应取消缩进，与class C语句同级。



4、按照以下要求定义一个游乐园门票的类，并尝试计算2个成人+1个小孩平日票价。

要求:

- 平日票价100元
- 周末票价为平日的120%
- 儿童票半价

```
class Ticket():
    # your code here
```

```
class Ticket():
    def __init__(self):
        day = True
        if day == True:
            adult = 100
        else:
            adult = 120
        kid = adult / 2
        print(adult * 2 + kid)
c = Ticket(
```

