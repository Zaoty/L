**练习题**：

1、字典基本操作

字典内容如下:

```
dic = {
    'python': 95,
    'java': 99,
    'c': 100
    }
```

用程序解答下面的题目

- 字典的长度是多少
- 请修改'java' 这个key对应的value值为98
- 删除 c 这个key
- 增加一个key-value对，key值为 php, value是90
- 获取所有的key值，存储在列表里
- 获取所有的value值，存储在列表里
- 判断 javascript 是否在字典中
- 获得字典里所有value 的和
- 获取字典里最大的value
- 获取字典里最小的value
- 字典 dic1 = {'php': 97}， 将dic1的数据更新到dic中

```
dic = {
    'python': 95,
    'java': 99,
    'c': 100
    }
print(len(dic))
dic['java']=98
print(dic)
del dic['c']
print(dic)
dic.setdefault('php',90)
dic.update(dic)
print(dic)
lst= list(dic.keys())
print(lst)
lst1= list(dic.values())
print(lst1)
if 'javascript' in dic:
    print('javascript 在字典中')
else:
    print('javascript 不在字典中')
lst2 = list(dic.values())
a = 0
for i in range(len(lst2)):
    a += lst2[i]
print(a)
lst2.sort(reverse = False)
mx = lst2[len(lst2)-1]
print(mx)
lst2.sort(reverse = True)
mn = lst2[len(lst2)-1]
print(mn)
dic1 = {'php':97}
dic.update(dic1)
print(dic)
```

![image-20210131142640769](https://github.com/Zaoty/L/blob/main/Python/The_first_week/day5/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-01-31%20142550.png)

2、字典中的value

有一个字典，保存的是学生各个编程语言的成绩，内容如下

```
data = {
        'python': {'上学期': '90', '下学期': '95'},
        'c++': ['95', '96', '97'],
        'java': [{'月考':'90', '期中考试': '94', '期末考试': '98'}]
        }
```

各门课程的考试成绩存储方式并不相同，有的用字典，有的用列表，但是分数都是字符串类型，请实现函数`transfer_score(score_dict)`，将分数修改成int类型

```
def transfer_score(data):
    # your code here
```
