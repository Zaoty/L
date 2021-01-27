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
while L1 < l and L2 < l:
    L1 = v1 * second1
    L2 = v2 * second2
    if (L1 - L2) >= t:
        second2 += s
        L2 = v2 * ( second2 )
        second1 = second2 - s
        L1 = v1 * second1
    else :
        second2 += 1
        L2 = v2 * ( second2 )
        L1 = v1 * second1
if L1 == L2 :
        print("D")
elif L1 > L2 :
        print("R")
elif L1 < L2 :
        print("T")
print(second2)

