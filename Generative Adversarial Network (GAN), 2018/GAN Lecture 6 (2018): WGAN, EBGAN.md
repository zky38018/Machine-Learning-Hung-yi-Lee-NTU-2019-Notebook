# Tips for Improving GAN #
## JS divergence is not suitable ##
只要两个分布没有重叠，JS divergence 都是 log2 

Intuition: If two distributions do not overlap, binary classifier achieves 100% accuracy.
![](https://i.imgur.com/QHuWfVQ.png)
![](https://i.imgur.com/j4algzF.png)


## Least Square GAN(LSGAN) ##
把原始GAN里面的sigmoid换成linear(把分类问题变为回归问题)

![](https://i.imgur.com/lyjTwZL.png)
## Wasserstein GAN(WGAN) ##

### Earch Mover's Distance ###
把两个分布之间的移动考虑成用推土机推土，有很多的移动方案，选取平均移动距离最小的方案来定义。
![](https://i.imgur.com/qJJW1r3.png)
![](https://i.imgur.com/dQzz4dO.png)
![](https://i.imgur.com/7O8D74p.png)
![](https://i.imgur.com/7oF5Bl8.png)
![](https://i.imgur.com/R0J1EaG.png)
![](https://i.imgur.com/oK9RRCF.png)
### 1-Lipschitz ###
Do not change fast.
保证斜率很小。
![](https://i.imgur.com/FvNlvgD.png)
### weight cipping ###
把所有的参数W限制在c和-c之间，当w>c时，w=c;当w<-c时，w=-c。

## Improved WGAN(WGAN-GP) ##
D属于1-Lipschitz本来的限制是对所有的x,现在把限制区域定义在Pdata和PG的中间。
![](https://i.imgur.com/AsZz9L1.png)
![](https://i.imgur.com/6riJOjM.png)
![](https://i.imgur.com/DtyG8jh.png)
## Spectrum Norm ##
让所有地方的梯度都小于1
![](https://i.imgur.com/pLxMwHe.png)
## WGAN的算法流程 ##
![](https://i.imgur.com/dmZjZro.png)
## Energy-based GAN(EBGAN) ##
把经典GAN的判别器D换成autoencoder
![](https://i.imgur.com/sa4HFha.png)
![](https://i.imgur.com/EjHbJdL.png)
## Loss-sensitive GAN(LSGAN) ##
引入margin的概念
![](https://i.imgur.com/cyQxeJr.png)
