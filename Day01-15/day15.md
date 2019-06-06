[day15](https://github.com/jackfrued/Python-100-Days/blob/master/Day01-15/15.%E5%9B%BE%E5%83%8F%E5%92%8C%E5%8A%9E%E5%85%AC%E6%96%87%E6%A1%A3%E5%A4%84%E7%90%86.md)

## 学习笔记

## Pillow

[官方文档](https://pillow.readthedocs.org/)

**PIL**：Python Imaging Library，已经是Python平台事实上的图像处理标准库了。PIL功能非常强大，但API却非常简单易用。

由于PIL仅支持到Python 2.7，加上年久失修，于是一群志愿者在PIL的基础上创建了兼容的版本，名字叫Pillow，支持最新Python 3.x，又加入了许多新特性，因此，我们可以直接安装使用**Pillow**。



### Modle - Image 

基础示例:
旋转图片并打开文件
```python
from PIL import Image
im = Image.open("bride.jpg")
im.rotate(45).show()
```

本次实践接触了以下方法：

- **open** 加载某图片
- **show** 打开某图片
- **rotate** 旋转
- **thumbnail** 缩放
- **crop** 裁剪
- **paste** 复制另一张图片到当前图片中
- **putpixel** 修改某像素的颜色值
- **transpose** 提供翻转和旋转(每90度)的方法 

问题：如何获取图片的尺寸

```python
image = Image.open('test.png')
print(image.size)
# (width, height)
```

### Model - ImageFilter

示例：
使用滤镜(图像增强过滤器)
```python
image.filter(ImageFilter.CONTOUR)
```

其他还包括：
- BLUR
- CONTOUR
- DETAIL
- EDGE_ENHANCE
- EDGE_ENHANCE_MORE
- EMBOSS
- FIND_EDGES
- SHARPEN
- SMOOTH
- SMOOTH_MORE


## 练习

### 图片缩放+拼接

![52033d3768a0134ad9d690b8b1294d45.png](evernotecid://18A3C926-B76C-4495-83CC-83D4C0B01782/appyinxiangcom/5697895/ENResource/p2976)


### 滤镜

![8bce711ff92368dc8ff975fc8a7fb878.png](evernotecid://18A3C926-B76C-4495-83CC-83D4C0B01782/appyinxiangcom/5697895/ENResource/p2977)
