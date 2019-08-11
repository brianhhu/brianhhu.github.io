---
layout: post
published: true
title: Choosing a deep learning framework
date: '2019-08-10'
---

<p align="center">
  <img width="640" height="480" src="http://brianhhu.github.io/img/dl_frameworks.jpg"><br />
  <em>Source: <a href="https://www.slideshare.net/noumfone/deep-learning-state-of-the-art-2019-mit-by-lex-fridman">https://www.slideshare.net/noumfone/deep-learning-state-of-the-art-2019-mit-by-lex-fridman</a></em>
</p>

Given the recent explosion of interest in deep learning, how do you go about choosing a deep learning framework?

<!--break-->

I faced this same question nearly two years ago when I started my journey in deep learning.
At that time (and even so today), the two major competitors were [*Tensorflow*](https://www.tensorflow.org/) and [*Pytorch*](https://pytorch.org/) (which I'll focus on here).
However, it is important to note that the framework landscape is constantly changing- while researchers
have largely moved on from some frameworks (e.g. Torch and Theano), new frameworks are also gaining traction quickly (e.g. fast.ai).

Tensorflow is backed by Google, while Pytorch is backed by Facebook. One of the major differences between these two frameworks
is that Tensorflow uses static computational graphs, while Pytorch uses dynamic computational graphs (although this will change with eager execution being more prominently featured in [Tensorflow 2.0](https://medium.com/tensorflow/whats-coming-in-tensorflow-2-0-d3663832e9b8)).
I eventually ended up choosing Pytorch for a couple of reasons (many of which are mentioned in the graphic above):

* **Learning curve:** I found Pytorch relatively easy to learn, with good [documentation](https://pytorch.org/docs/stable/index.html) and many helpful [tutorials](https://pytorch.org/tutorials/) online. I also found working with dynamic graphs to
be much more intuitive- when I tried out Tensorflow, having to create sessions and placeholders before being able to use a graph always confused me.
* **Speed of development:** I found Pytorch to be much more pythonic, making it easier to debug. Errors in Tensorflow, on the other hand, can often be cryptic. I also feel that Pytorch strikes a good balance between its level of abstraction and flexibility, making it easy to test out new ideas.
For example, Pytorch DataLoaders have made working with all different types of data a breeze. 
* **Community:** The [Pytorch forums](https://discuss.pytorch.org/) are a good source of information and useful for getting answers to questions. The Pytorch community is also
growing rapidly, with more and more papers being cited (Pytorch even seems to have caught up with Tensorflow! [source](https://www.oreilly.com/ideas/one-simple-graphic-researchers-love-pytorch-and-tensorflow))

In conclusion, I have found that Pytorch suits my needs as a deep learning researcher, allowing for fast prototyping of new ideas and providing a relatively stable API. Given its growing popularity,
I believe Pytorch will stick around for a while.

P.S. If you are converting models between different frameworks, I have found the [MMdNN tool](https://github.com/microsoft/MMdnn) to be helpful. Many times, it may not work completely right out-of-the-box, but I have found that it can be made to work with some minor hacks.
