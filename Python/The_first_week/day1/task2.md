**练习题**：

leetcode 习题 136. 只出现一次的数字

给定一个**非空**整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。

尝试使用位运算解决此题。

题目说明:

```
"""
Input file
example1: [2,2,1]
example2: [4,1,2,1,2]

Output file
result1: 1
result2: 4
"""



class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        
     # your code here
```

不太懂怎么用python表示这个程序

。。。先大概说一下逻辑吧。。

i遍历每个整数，先用a & (1<<i)检测 i 是否属于该集合

若结果为0， 则令i + 1，

若不为0，则用a & ~(1<<i) 将 i 从该集合删除 ，之后再用a & (1<<i)检测 i 是否属于该集合

若结果为0，则 i 即为该元素。若结果不为0，则令i + 1
