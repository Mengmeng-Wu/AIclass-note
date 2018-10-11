# 安裝tensorflow(Ubuntu 18.04)

## 順序: 
1. python 2. Anaconda 3. Tensorflow

<b>指令</b>

先安裝python 可查看python觀看版本到多少了d
```linux
$ sudo apt-get install python3
```

安裝pip
pip2
```linux
$ sudo apt install python-pip
```
pip3
```linux
$ sudo apt install python-pip3
```
check Version
```linux
$ pip --version
```

```linux
$ cd /tmp
```
curl 要進去且去選擇該要的版本並且下載
```linux
$ curl -O https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh
```
<p>sha256sum <b style="color:gray">Anacnodal version</b></p>

```linux
$ sha256sum Anaconda3-5.2.0-Linux-x86_64.sh
```
<b style="color:gray">output</b>

![](https://i.imgur.com/qXTQXMg.png)

run the srcript
```linux
1.$ bash Anaconda3-5.2.0-Linux-x86_64.sh
2.點選ENTER同意且輸入yes
```

<b style="color:gray">output</b>

anaconda3 預設位置點選 **[Enter]** 要等一下 才開始安裝相關套件
![](https://i.imgur.com/6NYzvR7.png)

![](https://i.imgur.com/EaQnfDI.png)

![](https://i.imgur.com/uy1F3V1.png)

```linux
$ source ~/.bashrc
```
確認Anaconda是否安裝成功
```linux
$ conda list
```
<p><b style="color:red">[success]</b><b style="color:gray">output</b></p>

![](https://i.imgur.com/y1D48mu.png)




<b style="color:red">[ERROR]</b>重新安裝並檢查是否有漏掉的步驟
![](https://i.imgur.com/aG3uiEy.png)

<b style="color:red">[ERROR]</b>python未完全安裝好
![](https://i.imgur.com/HB0PutR.png)

* 若要安裝Tensorflow [Point Me](https://www.tensorflow.org/install/pip)

測試tensorflow是否成功
-> 測試 VERSION1
```python
import tensorflow as tf
A = tf.constant('Hello World!')
with tf.Session() as sess:
    B = sess.run(A)
    print(B)
```
> 出現的錯誤訊息:Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA[color=#004d80]
```
import os 
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '2' 
```
-> 測試 VERSION2
```python
# -*- coding: utf-8 -*-

import tensorflow as tf
import os 
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '2'
# 宣告變數    
B = tf.Variable(0, dtype=tf.int64)
with tf.Session() as sess:
    # 變數需要初始化
    sess.run( tf.global_variables_initializer() )

    # 使用 assign 更改變數值
    for i in range(5):
        print( sess.run(B.assign(i)) )
```

<b style="color:red">[NOTICE]</b>
* spyder寫入有問題，不知道是否是因為執行為python3