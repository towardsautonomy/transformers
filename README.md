# Transformers for Vision

## Understanding Transformers through implementation and visualization of attention weights by dissecting the model intermediate layers

Transformers have been shown to be a great neural network architecture and works well in various domains, particularly proving itself in the field of NLP and Vision. This is an encoder-decoder architecture, with encoder block generating keys, and values for the decoder block through multi-headed self-attention, and the decoder block generating queries through a masked multi-headed self-attention block. The key-value pair from encoder and query from decoder is then passed through another multi-headed self-attention (effectively cross-attention) to generate output probability vectors.

![](media/transformer.png)

Original transformers introduced by Vaswani et al. in the paper "Attention Is All You Need", contains an encoder-decoder architecture. Several workstreams however explores an encoder-only or a decoder-only architecture which performs better on specific tasks while costs less memory and time for training. An example of encoder-only architecture is BERT where certain tokens are masked in the input and the network is tasked to predict those missing tokens. Similarly, GPT-n is an example of decoder-only architecture, where, given past n tokens, the network is trained to predict (n+1)th token. For a simple image classification example in consideration here, an encoder-only architecture will work pretty well, however, here I build an encoder-decoder architecture, as well as add support for encoder-only architecture for complete understanding of how to build and train such a system. I train both networks in this notebook and visualize attention layers.

### Launch the [notebook](transformers.ipynb) to give it a spin and get a better understanding of how to build and train such a system.