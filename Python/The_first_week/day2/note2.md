# 循环语句

### 1.while循环

while语句最基本的形式包括一个位于顶部的布尔表达式和一个或多个属于while代码块的缩进语句

while循环的代码块会一直循环执行，直到布尔表达式的值为假

布尔表达式可以不带有运算符，仅给出数值。可以写入str、list或任何序列，长度非零视为真值。

### 2.while-else循环

当while循环执行完，执行else。若while循环中跳出了循环，如break，则不执行else

### 3.for循环

for循环是迭代循环，在Python中相当于一个通用的序列迭代器，可以遍历任何有序序列，如str、list、tuple等，也可以遍历任何可迭代对象，如dict

for 迭代变量 in 可迭代对象

​		代码块

每次循环，迭代变量被设置为可迭代对象当前的元素，提供给代码块使用

### 4.for-else循环

for循环执行完时，执行else输出。若for循环中跳出循环，则不执行else代码块

### 5.range()函数

range([start,] stop[, step=1 ])

+ 这个BIF(Built-in functions) 有三个参数，用中括号括起的参数是可选的
+ step=1表示第三个参数的默认值是1
+ range这个BIF的作用为生成一个从start参数的值开始到stop参数的值结束的数字序列，该序列包含start的值但不包含stop的值

### 6.enumerate()函数

enumerate(sequence, [start= 0])

+ sequence——一个序列、迭代器或其他支持迭代对象
+ start——下标起始位置
+ 返回enumerate（枚举）对象

enumerate(A)不仅返回了A中的元素，还顺便给该元素一个索引值（从0开始）。此外，用enumerate(A,j)还可以确定索引起始值为j

### 7.break语句

break可以跳出当前所在层的循环

### 8.continue语句

continue终止本轮循环并开始下一轮循环

### 9.pass语句

pass语句的意思是“不做任何事”，如在需有语句的地方不写任何语句，则解释器会报错，pass语句用于解决此问题

### 10.推导式

##### 列表推导式

*[* **expr** *for* **value** *in* **collection** **[if condition]** *]*

```
x = [-4, -2, 0, 2, 4]
y = [a * 2 for a in x]
print(y)
# [-8, -4, 0, 4, 8]
```

##### 元组推导式

*(* **expr** *for* **value** *in* **collection [if condition]** *)*

```
a = (x for x in range(10))
print(a)

# <generator object <genexpr> at 0x0000025BE511CC48>

print(tuple(a))

# (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
```

##### 字典推导式

*{* **key_expr** *:* **value_expr** *for* **value** *in* **collection [if condition]** *}*

```
b = {i: i % 2 == 0 for i in range(10) if i % 3 == 0}
print(b)
# {0: True, 3: False, 6: True, 9: False}
```

##### 集合推导式

*{* **expr** *for* **value** *in* **collection [if condition]** *}*

```
c = {i for i in [1, 2, 3, 4, 5, 5, 6, 4, 3, 2, 1]}
print(c)
# {1, 2, 3, 4, 5, 6}
```

##### 其他

```
d = 'i for i in "I Love Lsgogroup"'
print(d)
# i for i in "I Love Lsgogroup"

e = (i for i in range(10))
print(e)
# <generator object <genexpr> at 0x0000007A0B8D01B0>

print(next(e))  # 0
print(next(e))  # 1

for each in e:
    print(each, end=' ')

# 2 3 4 5 6 7 8 9

s = sum([i for i in range(101)])
print(s)  # 5050
s = sum((i for i in range(101)))
print(s)  # 5050
```

### 11.综合例子

```
passwdList = ['123', '345', '890']
valid = False
count = 3
while count > 0:
    password = input('enter password:')
    for item in passwdList:
        if password == item:
            valid = True
            break
            
    if not valid:
        print('invalid input')
        count -= 1
        continue
    else:
        break
```
