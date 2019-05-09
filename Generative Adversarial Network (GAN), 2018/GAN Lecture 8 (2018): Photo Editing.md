# Intelligent photo editing #
## Modifying input code ##
输入的code决定了生成器G的输出。

理解每个dimension对输出的控制。
![](https://i.imgur.com/YfZkh58.png)
## GAN+Autoencoder ##
预先训练好一个GAN，把生成器G当作autoencoder的decoder，固定不动，把判别器D当作encoder的初始值，对encoder进行训练。
![](https://i.imgur.com/PbHXfAd.png)
## Attribute Representation ##
计算源对象和目标对象code的平均距离差，用源对象的code加上这个距离差code，再对新生成的code进行生成，就是目标对象。
![](https://i.imgur.com/ZOPkXe8.png)
## 找出目标对象对应code的三种方法 ##
![](https://i.imgur.com/Je0xQyV.png)
## 图像编辑的公式 ##
![](https://i.imgur.com/oHpLGAF.png)
