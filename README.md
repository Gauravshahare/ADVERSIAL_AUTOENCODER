# ADVERSIAL_AUTOENCODER

Implementation of paper (https://arxiv.org/abs/1511.05644) for my own research in Python 3 using Pytorch Library

![Paper](https://user-images.githubusercontent.com/51395380/58937435-0e82bc00-8790-11e9-80dd-44025701c9a2.png)

### Data
MNIST data set   ( dimensions of each image 28 * 28 * 1)

### Model Description

Adversial Autoencoder has 3 types of network  A ) Encoder B) Decoder  C) Discriminator

Encoder Network compresses the image in into bottleneck layer (Assuming the input to network are coorelated),it learns Latent Features.

Decoder Network takes input from encoder network, it reconstructs the image from bootleneck layer.

Discriminator Network distinguses between fake data and real data.

We are using Bivarient Normal distribution as our Prior distribution.


### Network Architecture
ENCODER      784 ==> 400 ==> 100 ==> 2

DECODER       2 ==> 100 ==> 400 ==> 784

DISCRIMINATOR  2 ==> 10 ==> 10 ==> 2

If you look at the way the network has trainied you will find encoder and discriminator are competing with each other which  forces the output from bottle neck layer to follow prior distribution 

### Result

![result](https://user-images.githubusercontent.com/51395380/58938463-818d3200-8792-11e9-85e3-a2874ae0dfc0.PNG)
