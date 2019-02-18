# GAN-comparisions

This repo contains my implementations of different GANs. <br><br>
Checklist :
- [x] Vanilla GAN
- [x] DC GAN
- [ ] Conditional GANs
- [ ] InfoGANs
- [ ] Wasserstein GANs

* __Dataset__ : The Cifar-10 dataset was used for training. The data was normalized between [-1,1).

* __Training__ : 

  * Vanilla GAN : The architecture consisted of a six layer neural net with leaky-ReLU activations on all but the last layers. The model was trained with noisy labelled data to improve performance. Adam and SGD optimizers were used for training. The model was trained for 650 epochs with a learning rate of 0.0002.
  
  * DC GAN : The architecture consisted of a five convolutional layers and a linear layer, again with with leaky-ReLU activations on all convolutional layers. This model was also trained with noisy labelled data and for 50 epochs with a learning rate of 0.0002. Adam and SGD optimizers were used for the discriminator and generator respectively. The model is still undertrained, and may perform better on further training. 

* __Loading__ : The dataset can be loaded by moving the .pth and .txt files to the root folder and running the appropriate cells. The default files corrosponds to the DC Gan, trained for 50 iterations.

For Vanilla GAN:
![](https://github.com/adiah80/SAiDL-Winter-Assignment-2018/blob/master/Assignment_3/Van_cost_vs_iterations.png)
![](https://github.com/adiah80/SAiDL-Winter-Assignment-2018/blob/master/Assignment_3/Van_final.png)

For DC GAN:
![](https://github.com/adiah80/SAiDL-Winter-Assignment-2018/blob/master/Assignment_3/DC_cost_vs_iterations.png)
![](https://github.com/adiah80/SAiDL-Winter-Assignment-2018/blob/master/Assignment_3/DC_final.png)
