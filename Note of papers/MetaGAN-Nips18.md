
# MetaGAN: An Adversarial Approach to Few-Shot Learning

## Overview
- MetaGAN is a conceptually simple and general framework for few-shot learning problems.
It’s a conditional generative model to generate samples which are not distinguishable from true data sampled from a specific task. 
- They increase the dimension of the classifier output from N to N + 1, to model the probability that input data is fake. 
- They train the discriminator (classifier) and generator in an adversarial setup.

## Method

### GANs
First, briefly introduce [GANs](https://arxiv.org/pdf/1406.2661.pdf).

Generative adversarial networks (GANs) are deep neural net architectures comprised of two nets, pitting one against the other (thus the “adversarial”).

- Generator : generates new data instances.
- Discriminator : evaluates them for authenticity
i.e. the discriminator decides whether each instance of data it reviews belongs to the actual training dataset or not.

Here are the steps a GAN takes:
- The generator takes in random numbers and returns an image.
- This generated image is fed into the discriminator alongside a stream of images taken from the actual dataset.
- The discriminator takes in both real and fake images and returns probabilities, a number between 0 and 1, with 1 representing a prediction of authenticity and 0 representing fake.

### MetaGAN

#### Discriminator
They adopt two popular choices of few-shot classification models as the discriminator.
- MAML [Finn et al., 2017](https://arxiv.org/pdf/1703.03400.pdf)
    - MAML trains a transferable initialization that is able to quickly adapt to any specific task with one step gradient descent.
- Relation Networks [Sung et al., 2018](https://arxiv.org/pdf/1711.06025.pdf)
    - The Relation Network (RN) is a few-shot learning model aiming to do classification via learning a deep distance metric between images. 

```
Detail
```

#### Generator
They use a conditional generative model to generate fake data that is close to the real data manifold in one specific task T.
- First compress the information in the task’s support dataset with a dataset encoder E into vector hT, which contains sufficient statistics for the data distribution of task T. 
- Then hT is concatenated with random noise input z to be provided as input to the generator network.

Encoder:
- Instance-Encoder Module : learns a feature representation for each individual data example in the dataset.
- Feature-Aggregation Module : takes each embedded feature vector as input and produce the representation vector hT for the whole task training set.
