# Text-to-Image #
### 传统的有监督学习方法 ###
会计算所有真实图片的平均值和生成图片的距离，导致生成的图片模糊。
### **Conditional GAN** ###
相比于GAN，G和D都增加了condition部分
![](https://i.imgur.com/5ELlgDx.png)
### Conditional GAN中两种Discriminator ###
![](https://i.imgur.com/V4Z3iC0.jpg)
### **stack GAN** ###
先生成小图，再生成大图。
![](https://i.imgur.com/pxhzSbN.png)

----------
# Image-to-image #
### 传统的有监督学习方法 ###
会计算所有真实图片的平均值和生成图片的距离，导致生成的图片模糊。(与Text-to-Image一样)

### **Patch GAN** ###
判决器D再判决时不是看整张图片，而是看一小块。
![](https://i.imgur.com/chqvIlX.png)

----------
# Speech Enhancement #

----------
# Video Generation #