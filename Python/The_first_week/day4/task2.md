**练习题**：

1、元组概念

写出下面代码的执行结果和最终结果的类型

```
(1, 2)*2
(1, )*2
(1)*2
```

分析为什么会出现这样的结果.

![image-20210129170342852](https://github.com/Zaoty/L/blob/main/Python/The_first_week/day4/image-20210129170342852.png)

()中含有逗号，被视为元组

()中不含有逗号，被视为表达式

2、拆包过程是什么？

```
a, b = 1, 2
```

上述过程属于拆包吗？

可迭代对象拆包时，怎么赋值给占位符？

