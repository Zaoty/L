**练习题**：

1. 怎么找出序列中的最⼤、⼩值？
2. sort() 和 sorted() 区别
3. 怎么快速求 1 到 100 所有整数相加之和？
4. 求列表 [2,3,4,5] 中每个元素的立方根。
5. 将[‘x’,‘y’,‘z’] 和 [1,2,3] 转成 [(‘x’,1),(‘y’,2),(‘z’,3)] 的形式。

1.max()          min()

2.`list.sort(key=None, reverse=False)` 对原列表进行排序。

- `key` -- 主要是用来进行比较的元素，只有一个参数，具体的函数的参数就是取自于可迭代对象中，指定可迭代对象中的一个元素来进行排序。
- `reverse` -- 排序规则，`reverse = True` 降序， `reverse = False` 升序（默认）。
- 该方法没有返回值，但是会对列表的对象进行排序。

```
sorted(iterable, key=None, reverse=False) 
```

对所有可迭代的对象进行排序操作。

- `iterable` -- 可迭代对象。
- `key` -- 主要是用来进行比较的元素，只有一个参数，具体的函数的参数就是取自于可迭代对象中，指定可迭代对象中的一个元素来进行排序。
- `reverse` -- 排序规则，`reverse = True` 降序 ， `reverse = False` 升序（默认）。
- 返回重新排序的列表。

3.

`sum(iterable[, start=0])` 返回序列`iterable`与可选参数`start`的总和。

```
lst = range(101)
a = sum(lst)
print(a)
```

![image-20210131235529323](C:\Users\12813\AppData\Roaming\Typora\typora-user-images\image-20210131235529323.png)

4.

```
a = [2,3,4,5]
for i in a:
    b = i ** (1/3)
    print(b)
```

![image-20210131235411567](C:\Users\12813\AppData\Roaming\Typora\typora-user-images\image-20210131235411567.png)

5.

```
a = ['x','y','z']
b =  [1,2,3]
c = zip(a,b)
print(list(c))
```

![image-20210131235454635](C:\Users\12813\AppData\Roaming\Typora\typora-user-images\image-20210131235454635.png)

