# About

This part includes some personal findings/implementations in deep learning.

### Table of Contents
**[1. What is the difference between pooling and pooling-over-time?](#)**<br>
**[2. What is difference between max-pooling, min-pooling and average-pooling?](#)**<br>
**[3. What is co-adaption in deep learning?](#)**<br>
**[4. What is perplexity in NLP?](#)**<br>

## 1. What is the difference between pooling and pooling-over-time?

The max-over-time pooling is usually applied in NLP (unlike ordinary max-pool, which is common in CNNs for computer vision tasks), so the setup is a little it different.

See [here](https://stackoverflow.com/questions/48549670/pooling-vs-pooling-over-time)

## 2. What is difference between max-pooling, min-pooling and average-pooling?

See [here](https://medium.com/@bdhuma/which-pooling-method-is-better-maxpooling-vs-minpooling-vs-average-pooling-95fb03f45a9) for a good explanation.

A good example in this artical is the MNIST dataset: since the digit is white and backgroud is black, we should use `max-pooling` .

## 3. What is co-adaption in deep learning?

When you build a neural network with certain number of neurons in its hidden layers, you ideally want each neuron to operate as an independent feature detector. Of two or more neurons begin to detect the same feature repeatedly (co-adaption), the network isn't utilizing its full capacity efficiently. It's wasting computational resources computing the activation for redundant neurons that are all doing the same thing.

See [here](https://www.quora.com/What-does-co-adaptation-of-neurons-in-a-Neural-network-mean) and the [paper](https://arxiv.org/pdf/1207.0580.pdf).

## 4. What is perplexity in NLP?

Overall, the perplexity is just the exponential of the entropy.

For a more detailed explanation, see [this artical](https://towardsdatascience.com/perplexity-intuition-and-derivation-105dd481c8f3).

