## Project Overview

In this project we'll be building a GAN to generate images of a variety of vehicles and animals, based on the stl10 dataset, which contains images of birds, airplanes, ships, cats, trucks, ships, airplanes, cars, deers, and horses.

To achieve this we will create a Generator that outputs images, using a number of CNN layers, upsampling layers, and an output layer, and conversely, a Discriminator, which will be trained to discriminate between real images and generated images.

### STL-10 Database (Source: https://www.tensorflow.org/datasets/catalog/stl10)
The STL-10 dataset is an image recognition dataset for developing unsupervised feature learning, deep learning, self-taught learning algorithms. It is inspired by the CIFAR-10 dataset but with some modifications. In particular, each class has fewer labeled training examples than in CIFAR-10, but a very large set of unlabeled examples is provided to learn image models prior to supervised training. All images were acquired from labeled examples on ImageNet.

Note: For our purposes, the labels will actually not be necessary, since our goal is not to generate images of a specific type, but simply to create images that pass as real.

### Update:

As you'll see below, our model struggled to fit with such high resolution images, so you'll also see references to actually importing and trying different models with cifar10 (source: https://www.tensorflow.org/datasets/catalog/cifar10)