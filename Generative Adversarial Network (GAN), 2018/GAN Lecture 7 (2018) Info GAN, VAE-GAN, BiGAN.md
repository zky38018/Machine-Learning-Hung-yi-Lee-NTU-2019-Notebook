# Feature Extraction #
## InfoGAN ##
通过修改GAN输入的code来生成不同的图片，衡量code对image的影响
![](https://i.imgur.com/zaR0jMT.png)
![](https://i.imgur.com/nFxbT8y.png)
![](https://i.imgur.com/3MKAUdA.png)
![](https://i.imgur.com/29rY8FV.png)
## VAE-GAN ##
把VAE和GAN相结合，一方面用autoencoder降低重建误差，一方面衡量用Discriminator，比原来的GAN增加了原图部分，使得code更稳定。
![](https://i.imgur.com/zbg4DWi.png)
![](https://i.imgur.com/nKQwDsd.png)
## BiGAN ##
分别训练一个encoder和decoder,把encoder的输入、输出和decoder的输入、输出分别输入到判别器D里，判断是来自encoder还是decoder？、
![](https://i.imgur.com/hPz77yS.png)
![](https://i.imgur.com/Bt7USXg.png)
![](https://i.imgur.com/Jgs1xRs.png)
![](https://i.imgur.com/7cHXOfP.png)
## Triple GAN ##
![](https://i.imgur.com/UWrddP8.png)
## Domain-adversarial training ##
对不同域的图片抽取特征，判断它来自哪个域，并且判断他的类别
![](https://i.imgur.com/Lax8sQn.png)
![](https://i.imgur.com/eAhnkhj.png)
## Seq2seq Auto-encoder feature disentangle ##
相比于传统的antoencoder，把语音和语义分开。
![](https://i.imgur.com/ZwOoJdQ.png)
![](https://i.imgur.com/wsEHcoB.png)
![](https://i.imgur.com/bj27qAL.png)
![](https://i.imgur.com/gWsgtzd.png)
