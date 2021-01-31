**练习题**：

1. 怎么表示只包含⼀个数字1的元组。
2. 创建一个空集合，增加 {‘x’,‘y’,‘z’} 三个元素。
3. 列表['A', 'B', 'A', 'B']去重。
4. 求两个集合{6, 7, 8}，{7, 8, 9}中不重复的元素（差集指的是两个集合交集外的部分）。
5. 求{'A', 'B', 'C'}中元素在 {'B', 'C', 'D'}中出现的次数

```
tu = (1,)
print(tu)
se = set()
se.add('x')
se.add('y')
se.add('z')
print(se)
lst = ['A', 'B', 'A', 'B']
st = set(lst)
lst1 = list(st)
print(lst1)
a = {6, 7, 8}
b = {7, 8, 9}
c = (a - b) | (b - a)
print(c)
A = {'A', 'B', 'C'}
B = {'B', 'C', 'D'}
C = A & B
n = len(C)
print(n)
```

![image-20210131180520283](C:\Users\12813\AppData\Roaming\Typora\typora-user-images\image-20210131180520283.png)

