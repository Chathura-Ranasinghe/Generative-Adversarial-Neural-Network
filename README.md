# Generative adversarial networks (GANs)

A generative adversarial network (GAN) is a deep learning architecture that trains two neural networks to compete against each other to generate more authentic new data from a given training dataset. For instance, you can generate new images from an existing image database or original music from a database of songs.

## Key points of GANs

### 1. Use unsupervised Learning (supervised itself).
### 2. Have two submodels:
    - 2.1. Generator submodel
    - 2.2. Discriminator submodel

![GAN Architecture](image.png)

Reference: [TensorFlow Tutorial on DCGAN](https://www.tensorflow.org/tutorials/generative/dcgan)

#### How GANs Works

In GANs, the generator and discriminator play a game of cat and mouse:

- The generator creates fake data, like images, from random noise. Its goal is to make these fakes look as real as possible.
  
- Meanwhile, the discriminator's job is to tell real data from fake. It learns to distinguish between real images and the ones the generator creates.
  
- They keep improving through competition. As the generator gets better at making fakes, the discriminator gets better at spotting them, and vice versa. Eventually, the generator learns to make really convincing fakes, while the discriminator becomes adept at telling them apart.

### 3. Both Generator and Discriminator implement as CNN(Convolutional neural network).

Convolutional neural network is a regularized type of feed-forward neural network that learns feature engineering by itself via filters optimization. Vanishing gradients and exploding gradients, seen during backpropagation in earlier neural networks, are prevented by using regularized weights over fewer connections.

## Tenssorflow Dataset 

### Tensorflow_datasets ( tfds ) defines a collection of datasets ready-to-use with TensorFlow. Each dataset is defined as a tfds.core. In here we are going to use "fashion mnist" data set

Reference: [TensorFlow Dataset Catelog](https://www.tensorflow.org/datasets/catalog/overview)
