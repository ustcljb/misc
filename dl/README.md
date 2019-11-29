# About

This part includes some personal findings/implementations in deep learning.

### Table of Contents
**[1. What is the difference between pooling and pooling-over-time?](#)**<br>
**[2. What is co-adaption in deep learning?](#)**<br>

## 1. What is the difference between pooling and pooling-over-time?

The max-over-time pooling is usually applied in NLP (unlike ordinary max-pool, which is common in CNNs for computer vision tasks), so the setup is a little it different.

See [here](https://stackoverflow.com/questions/48549670/pooling-vs-pooling-over-time)

## 2. What is co-adaption in deep learning?

When you build a neural network with certain number of neurons in its hidden layers, you ideally want each neuron to operate as an independent feature detector. Of two or more neurons begin to detect the same feature repeatedly (co-adaption), the network isn't utilizing its full capacity efficiently. It's wasting computational resources computing the activation for redundant neurons that are all doing the same thing.

See [here](https://www.quora.com/What-does-co-adaptation-of-neurons-in-a-Neural-network-mean) and the [paper] (https://arxiv.org/pdf/1207.0580.pdf)

