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

