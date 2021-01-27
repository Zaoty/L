# 条件语句

### 1.if语句

+ if 语句的 expr_true_suite 代码块只有当条件 expression 结果为真时才执行，否则执行紧跟在该代码块后面的语句
+ 单个if语句中的expression条件表达式可以通过布尔操作符and,or和not实现多重条件判断

### 2.if - else语句

+ Python提供与if搭配使用的else,如果if语句的条件表达式结果为假，则执行else语句后的代码
+ if语句支持嵌套，即在一个if语句中嵌入另一个if语句。Python使用缩进而非大括号标记代码块边界，因此要注意else的悬挂问题。

### 3.if-elif-else语句

+ elif语句即为else if ，用于检查多个表达式是否为真，并在为真时执行特定代码块中的代码。

### 4.assert关键词

+ assert这个关键词我们称之为“断言”，当这个关键词后边的条件为False时，程序自动崩溃并抛出AssertionError的异常
+ 进行单元测试时，可以用来在程序中置入检查点，条件为True时才能让程序正常工作。
