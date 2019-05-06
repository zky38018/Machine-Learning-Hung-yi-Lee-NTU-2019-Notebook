# 1. GAN的目的是要生成一个跟真实样本空间相同的分布 #
## 最大似然估计=最小化KL发散 ##
![](https://i.imgur.com/5CEm02e.png)

![](https://i.imgur.com/fHgJXba.png)

# 2.生成器G是要最小化生成样本和真实样本的差异 #

![](https://i.imgur.com/WtRjeLl.png)
# 3.判别器D是要最大化生成样本和真实样本的差异 #
![](https://i.imgur.com/qB8ZaGh.png)
## 判别器的最大化差异相当于JS divergence ##
![](https://i.imgur.com/Ng8Oobp.png)

![](https://i.imgur.com/N6cAvhi.png)

![](https://i.imgur.com/r1ei0DJ.png)

![](https://i.imgur.com/MRDaOfH.png)

## 生成器G和判别器D之间的关系 ##
![](https://i.imgur.com/YBli817.png)

## 判别器D的目标函数相当于一个二分类器 ##
![](https://i.imgur.com/JyC5cZr.png)
# 4.GAN的训练流程 #
## 在一个循环里判别器D多训练几次，生成器G少训练1次 ##
![](https://i.imgur.com/eSViYiw.png)
## GAN的目标函数 ##
![](https://i.imgur.com/eM5dHHv.png)
