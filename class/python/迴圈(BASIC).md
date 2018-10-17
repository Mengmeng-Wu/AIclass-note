## 迴圈選擇
> * 選擇:If |if-else| ..沒有switch
> * 迴圈::while | for loop |沒有do-while
> * range break continue
> * Nested loop有switch

### IF

```python
import time
date = time.localtime()		#取得目前的日期時間
year = date[0]
month = date[1]
day = date[2]
day_month = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31] #若是閏年28的地方要改為29
if year%400==0 or (year%4==0 and year%100!=0):	#判斷是否為閏年
    day_month[1] = 29
if month==1:
    print(day)
else:
    print(sum(day_month[:month-1])+day) 
    #列出目前今年已經過幾天了
```

### FOR LOOP

```python
score = [70, 90, 78, 85, 97, 94, 65, 80]
s = 0
for i in score:
	s += i
print(s / len(score))
```

<b>[output]</b>

![](https://i.imgur.com/i0r7LuP.png)

```python
words = ['cat', 'window', 'defenestrate']
for w in words:
   print (w), len(w)
```

<b>[output]</b>

![](https://i.imgur.com/njZaUrd.png)


```python
#!/usr/bin/python
# -*- coding: UTF-8 -*-
 
for i in range(1,5):  #range總共跑4次
    for j in range(1,5):
        for k in range(1,5):
            if( i != k ) and (i != j) and (j != k):
                print (i,j,k)
```

<b>[output]</b>
![](https://i.imgur.com/rvQT4LM.png)


```python
def main(n): #定義main
    for i in range(n): #range為6
        print((' * '*i).center(n*3))
    for i in range(n, 0, -1):
        print((' * '*i).center(n*3))

main(6)
```

<b>[output]</b>

![](https://i.imgur.com/8m7oWD2.png)
