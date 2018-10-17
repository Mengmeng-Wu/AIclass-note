# Python_pillow

說明手冊  [Poin Me](https://pillow.readthedocs.io/en/5.3.x/)

----

* 單純移動roation 45度角

```python
from PIL import Image
im = Image.open("../images.jpg")
im.rotate(45).show()
```

<b>[output]</b>


![](https://i.imgur.com/caSJ8LU.png)


-----

* Filter Blur

```python
from PIL import Image, ImageFilter

# 打開一個jpg影像檔，注意是在當前路徑:
im = Image.open('../images.jpg')

# 應用模糊濾鏡filter():
im2 = im.filter(ImageFilter.BLUR)

# 將模糊濾鏡後的圖片存檔:
im2.save('images_blur.jpg')
```

<b>[output]</b>

![](https://i.imgur.com/WnbqYaE.png)

-----


* 縮放IMAGES

```python
#!/usr/bin/env python

#coding=utf-8

from PIL import Image
# 打開一個jpg影像檔，注意是當前路徑:

im = Image.open('../images.jpg')
# 獲得圖像尺寸:
w, h = im.size
print('Original image size: %sx%s' % (w, h))

# 縮放到50%:
im.thumbnail((w//2, h//2))
print('Resize image to: %sx%s' % (w//2, h//2))

# 把縮放後的圖像用jpeg格式保存:
im.save('view_thumb.jpg')
```

<b>[output]</b>

![](https://i.imgur.com/VIXdA0D.png)

![](https://i.imgur.com/hSDQH9h.png)
