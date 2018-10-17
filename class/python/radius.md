* raw_input([prompt]) 函數從標準輸入讀取一個行，並返回一個字串（去掉結尾的分行符號）
* input([prompt]) 函數和 raw_input([prompt]) 函數基本類似，但是 input 可以接收一個Python運算式作為輸入，並將運算結果返回。

```python

#!/usr/bin/env python
#coding=utf-8

# radius = 25 
# Input(輸入):Prompt the user to enter a radius
radius = eval(input("Enter a number for radius: "))

# Processing(處理):Compute area
area = radius * radius * 3.1415962

# Output(輸出):Display results
print("The area for the circle of radius", radius, "is", area)
```
