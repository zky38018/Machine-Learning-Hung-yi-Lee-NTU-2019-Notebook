# Unsupervised Conditional Generation #
Transform an object from one domain to another **without paired data**.
## Two approach ##
![](https://i.imgur.com/KYFS2KC.png)

----------

### 第一种方法 ###
1. 忽略输出图片跟输入图片的相似性，直接上
![](https://i.imgur.com/bQJW7QL.png)
2. 弄两个encoder网络来使输入输出的特征向量保持一致
![](https://i.imgur.com/IGgLUWO.png)
3. 弄两个Generator,使输入输出在保持pixel-wise的相似性。
![](https://i.imgur.com/I1Z9iqy.png)
4. 在3的基础上再弄一套从domain Y到domain X的网络
![](https://i.imgur.com/b9oiWl4.png)
#### Issue of Cycle Consistency ####
![](https://i.imgur.com/QwgT7wG.png)
#### StarGAN ####
借鉴编码的思想，对特征域编码
![](https://i.imgur.com/U1pTSmB.png)
![](https://i.imgur.com/BgvbtJ1.png)
![](https://i.imgur.com/Xk9PfhX.png)

----------

### 第二种方法 ###


-  按照autoencoder的方法训练，但如何保证两个autoencoder产生的特征向量有相似性？
![](https://i.imgur.com/xKsrWfS.png)
	
	- 共享两个autoencoder的参数
	![](https://i.imgur.com/qCctkE6.png)
	- 增加一个domain discriminator
	![](https://i.imgur.com/l7ylDTP.png)
	- cycle consistency
	![](https://i.imgur.com/D0sZQcL.png)
	- semantic consistency
	![](https://i.imgur.com/vDIOJtI.png)