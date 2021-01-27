# 练习题

1.

for num in range (1500 , 2700) :

​		if num % 7 == 0:

​				if num % 5 == 0:

​						print(num)

​				continue

2.

```
v1=10
v2=5
l=1000
t=5
s=1
second1 = second2 = 1
L1=v1
L2=v2
while L1 < l and L2 < l :
    L1 = v1 * second1
    L2 = v2 * second2
    second2 += 1
    if (L1 - L2) > t :
        L2 = v2 * (second2 + s)
        second1 = second2 - s
if L1 > l :
        print("R")
elif L2 > l :
        print("T")
else :
        print("D")
print(second2)
```

