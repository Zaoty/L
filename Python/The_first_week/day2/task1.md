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
l=20
t=5
s=2
L1=v1
L2=v2
n = 0
seconds = range(1, l//v2 +1 )
for second in seconds:
    L1 = v1 * (second - n)
    L2 = v2 * second
    if (L1 - L2) >= t:
        n += 1
    continue
if L1 == L2 :
        print("D")
elif L1 > L2 :
        print("R")
elif L1 < L2 :
        print("T")
print(second)
