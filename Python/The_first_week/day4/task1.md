练习题：

1、列表操作练习

列表lst 内容如下

lst = [2, 5, 6, 7, 8, 9, 2, 9, 9]

请写程序完成下列操作：

在列表的末尾增加元素15
在列表的中间位置插入元素20
将列表[2, 5, 6]合并到lst中
移除列表中索引为3的元素
翻转列表里的所有元素
对列表里的元素进行排序，从小到大一次，从大到小一次

```
lst = [2,5,6,7,8,9,2,9,9]
lst.append(15)
print('1.',lst)
x = len(lst)
lst.insert(x//2 , 20 )
print('2.',lst)
lst1 = [2,5,6]
lst = lst + lst1
print('3.',lst)
del lst [3]
print('4.',lst)
lst.reverse()
print('5.',lst)
lst.sort()
print('6.',lst)
lst.sort(reverse=True)
print('6.',lst)
```

2、修改列表

问题描述：

lst = [1, [4, 6], True]

请将列表里所有数字修改成原来的两倍

```
lst = [1,[4,6],True]
lst[0] *= 2
lst[1][0] *= 2
lst[1][1] *= 2
print(lst)
```

3.符合下列属性的数组 arr 称为 山脉数组 ：
arr.length >= 3
存在 i（0 < i < arr.length - 1）使得：
arr[0] < arr[1] < ... arr[i-1] < arr[i]
arr[i] > arr[i+1] > ... > arr[arr.length - 1]
给你由整数组成的山脉数组 arr ，返回任何满足 arr[0] < arr[1] < ... arr[i - 1] < arr[i] > arr[i + 1] > ... > arr[arr.length - 1] 的下标 i 。

 

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/peak-index-in-a-mountain-array
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
class Solution(object):
    def peakIndexInMountainArray(self, A):
        for i in xrange(len(A)):
            if A[i] > A[i+1]:
                return i
```
