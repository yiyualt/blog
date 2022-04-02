---
title: "Attention is All You Need"
date: 2022-04-02T00:59:43+09:00
draft: false
---

This [[1]](https://arxiv.org/pdf/1706.03762.pdf) is a very successful paper that has 38872 citations (at current time point). The paper
has far-reaching impacts to not only NLP community but also CV fields. You may be curious about this paper. 

This paper invented a purely attention based model, called Transformer, which replaces the recurrent operation of capturing sequential information with 
attention operations. The attention operation is performed by three independent linear transformation matrix, i.e., Q, V, and K. The matrix Q transforms 
the information of target/current token to be computed, while K matrix transforms the information of memory that the query is going to match, and V matrix 
transforms the information of original all tokens. In this way, the generated token/representation, fuses the information of itself, itself with others, 
and the others. 

Why attention-based model is superior to RNN-based sequential model? From the following figure, 
we can see that the model complexity is much smaller than eight recurrent operation or convolutional operation.
![This is an image](/images/10.png)

### Main Result
![This is an image](/images/11.png)

### More in the paper
- positional encoding 

Apart from the ccaled dot-product attention and multi-head attention, this paper invented also a novel positional
encoding.

- regularization tricks

For better training, the authors apply residual dropout and label smoothing. The dropout rate is 0.1 and the label soothing rate is
0.1 as well. 

- many variants

The authors have also provided many Transformer variants (20 models!). Those trials must have
taken much and much of time. 

- English Constituency Parsing

To valid the effectiveness of Transformer's superiority to RNN models, the authors do not only experiment on
machine translation task, but also test their performance on the English Constituency Parsing task. The results turns out that, 
desipte the lack of task-specific tuning, Transformer still performs quite well. 

We can see that, the experiments are very comprehensive ang make a lot of sense, 
thus this is pretty good paper. 

[1] Attention is All You Need, Ashish Vaswani, et al. NIPS 2017.