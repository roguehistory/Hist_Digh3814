---
title: "Neural Networks & Computer Vision"
description: "The Automated Archaeologist"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -4
author: "Shawn Graham"
---
## Introduction

![neural network gif](https://media.giphy.com/media/LXRhyTjXJEUmQG1NrT/giphy.gif)

Gif by Alex Mordvintsev showing how neural networks 'see'; a higher resolution version is available [here](https://twitter.com/zzznah/status/1118917356430995456).

When our eyes see an image, various receptors in the retina respond by firing. Some fire in response to various colours. Some fire in response to light and shadow. Imagine that these cells are arranged in layers. If those simple cells in the first layer fire, they pass a signal to the next layer up. The cells in _that_ layer might only fire if they get enough 'activations' from the previous layer. Each layer in turn receives the input of more and more complicated patterns of connections from the previous layer. Eventually, the brain receives the signal.

A biologist might read that paragraph, and shudder. Neural networks have long been around in the field of artificial intelligence, and they've been modelled after that simple analogy. Since about 2012 or so, the field of neural networks has exploded with the raw computing power of commercial grade GPUs. The key to the recent explosion has been this combination of raw computing power, large million image datasets, and the idea of allowing inputs to back propogated along the network: basically, if you put enough images of a dog in front of the neural network, the average pattern of connection and firing could be labelled 'dog'; then if a picture of, say, a cat was put in front of the network, the _distance_ or _similarity_ of the firing could be compared to that we know for 'dog' and a score computed. Put enough pictures of cats in front of the neural network, and the network learns what 'cats' look like.

I simplify enormously, of course, but that's the gist. The neat thing is, once you've got a network trained on thousands of different kinds of things - which takes enormous computing power and resources - you can _retrain_ just the **last** layer of the network with new data, to teach it what something looks like that it wasn't trained on. Retrain the network on pictures of Roman pottery, and it will learn what different kinds of Roman pottery look like (but you can't use it for dogs any more). The network lights up in a particular way when it encounters pictures of _verenice nera_, and we can say: this pattern = verenice nera, with a given probability.

(For a discussion on the use of neural networks in archaeology, see [Baxter 2014](https://www.academia.edu/8434624/Neural_networks_in_archaeology)).

Indeed, you don't even need to have labelled categories of things for a pretrained neural network to be useful. The Yale DH Lab uses a neural network without that final layer to find image similarity: it shows images to the network, and computes the distance between how the network lights up for one image versus a different image. This distance can then be expressed in two-dimensional space, and you end up with a visualization of visual similarity! See [their repository here](https://github.com/YaleDHLab/pix-plot).

![pixplot](https://raw.githubusercontent.com/YaleDHLab/pix-plot/master/pixplot/web/assets/images/preview.png)

## Exercise

In this exercise, you're going to re-train a neural network on a small dataset of Roman pottery images.

1. In our [course repository](https://github.com/shawngraham/hist3000/blob/master/static/data/archaeological_image_classifier.ipynb) I have created a notebook containing all of the code necessary to build a simple image classifier that you will train on some Roman pottery wares.  Hit the blue 'open in colab' button. The notebook assumes you have a Google drive account. You will need to upload the [image data zipped folder](https://github.com/shawngraham/hist3000/blob/master/static/data/data.zip?raw=true) (clicking the link should start a download to your machine).

2. Read the notebook carefully, and make sure to run each cell in sequence, letting a cell complete before you run the next one. Also, you need to make sure that the notebook settings for hardware acceleration are set to 'gpu' (see the getting started block in the notebook).
