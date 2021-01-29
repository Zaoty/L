**练习题**：

1、字符串函数回顾

- 怎么批量替换字符串中的元素？

- 怎么把字符串按照空格进⾏拆分？

- 怎么去除字符串⾸位的空格

  

+ 1.可以用replace(old, new [, max])

  2.可以用maketrans(intab, outtab)创建字符映射的转换表

然后使用translate(table, deletechars="")

+ split(str="", num)
+ lstrip([chars]



2、实现isdigit函数

题目要求

实现函数isdigit， 判断字符串里是否只包含数字0~9

```
def isdigit(string):
    """
    判断字符串只包含数字
    :param string:
    :return:
    """
    # your code here
    pass
```

```
def isdigit(string):
    """
    判断字符串只包含数字
    :param string:
    :return:
    """
    print(isdigit.isnumeric())
    pass
```
