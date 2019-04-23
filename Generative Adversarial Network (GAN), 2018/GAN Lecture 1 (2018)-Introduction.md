
## 有用的英文表达 ##
	since sliced bread 有史以来（形容一项技术非常好）

----------

# Basic idea of GAN #
##   Generation ##
图像生成：输入一个向量，输出一张图片。
## Discriminator ##
输入一张图片，给出一个scalar（分数）。

scalar越大，代表图像越真实；越小，代表越假。
## Generator VS Discriminator ##
写作敌人，念做朋友
### 算法 ###
- 初始化generator(G)和discriminator(D)
- 在每个训练周期中：
	1. 固定G,更新D（D学习给真实的对象高的分数，给生成的对象低的分数）
	2. 固定D，更新G（G学习去骗过D）
## 详细的算法 ## 
![](https://i.imgur.com/MlptPEC.png)

----------

# GAN as structured learning #
## structured learning ##

![](https://i.imgur.com/NQBZqyu.png)
## 为什么结构化学习这么具有挑战性？ ##
- **One-shot/Zero-shot Learning**:
	- 在分类中，每种类别都有很多样本实例
	- 在结构化学习中
		- 如果你把每个可能的输出都看作一个“类别”。。。
		- 由于输出的空间是很大的，很多“类别”是没有训练数据的
		- 机器学习需要在测试时产生新东西
		- 需要更多的智能
		
- Machine has to learn to do planning(全局观)
## 结构化学习的方法——局部+全局 ##
![](https://i.imgur.com/bpti37t.png)


----------
	
# Can Generator learn by itself? #

1. G是输入一个向量，输出一张图片，那输入的向量（code）哪里来？
2. Encoder in auto-encoder provides the code
3. Auto-encoder的后半部分——Decoder就是一个G（Generator）
![](https://i.imgur.com/V3ssTN1.png)
4. Auto-encoder的改进版本：Variational Auto-encoder(VAE)
5. what do we miss?
	- Each neural in output layer corresponds to a pixel.
	- The relation between the components are critical.
	- Although highly correlated, they cannot influence each other.
	- Need deep structure to catch the relation between components.


----------

# Can Discriminator generate? #

1. Discriminator的输入是一个对象，比如一张图象，输出是一个scalar，代表对象的好坏
2. 自上而下地评价组分之间的关系是很容易的.
![](https://i.imgur.com/TA4LW7K.png)
3. 假设我们已经有D，可以生成所有可能的对象，然后选择中间得分最高的作为最终结果
4. 怎么训练D？我们只有真实图像，如何产生假图？
5. 通常的算法：给一系列真实样本，随机生成假的样本

----------

# G和D的比较 #

G是从局部考虑，D是全局考虑。
![](https://i.imgur.com/CZvVYxe.png)

----------

# Benefit of GAN #
![](https://i.imgur.com/qauXObq.png)