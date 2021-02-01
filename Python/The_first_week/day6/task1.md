**练习题**：

1. 怎么给函数编写⽂档？
2. 怎么给函数参数和返回值注解？
3. 闭包中，怎么对数字、字符串、元组等不可变元素更新。
4. 分别根据每一行的首元素和尾元素大小对二维列表 a = [[6, 5], [3, 7], [2, 8]] 排序。(利用lambda表达式)
5. 利用python解决汉诺塔问题？

> 有a、b、c三根柱子，在a柱子上从下往上按照大小顺序摞着64片圆盘，把圆盘从下面开始按大小顺序重新摆放在c柱子上，尝试用函数来模拟解决的过程。（提示：将问题简化为已经成功地将a柱上面的63个盘子移到了b柱）

[![img](https://camo.githubusercontent.com/13b5107716e76b74486af654c4fb80d96697f3d6ee2365ee71aa090bcc43c21c/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f32303230303731343233323533353831332e706e67)](https://camo.githubusercontent.com/13b5107716e76b74486af654c4fb80d96697f3d6ee2365ee71aa090bcc43c21c/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f32303230303731343233323533353831332e706e67)

1.2.

```
def functionname(parameters):
    "函数_文档字符串"
    function_suite
    return [expression]
```

3.

 如果要修改闭包作用域中的变量则需要 `nonlocal` 关键字

4.

```
a = [[6, 5], [3, 7], [2, 8]]
a.sort(key=lambda a: a[0],reverse=True)
print(a)
a = [[6, 5], [3, 7], [2, 8]]
a.sort(key=lambda a: a[1],reverse=True)
print(a)
```

![image-20210202014738688](https://github.com/Zaoty/L/blob/main/Python/The_first_week/day6/2.1%201.png)

5.

```
i = 0
def hanota(num,a,b,c) :
    global i
    if (num == 1) :
        i += 1
        print('移动第{0}次{1}-->{2}'.format(i,a,c))
        return
    hanota(num-1,a,c,b)
    hanota(1,a,b,c)
    hanota(num-1,b,a,c)

hanota(3,'a','b','c')


```

![image-20210202015111452](https://github.com/Zaoty/L/blob/main/Python/The_first_week/day6/2.1%202.png)
