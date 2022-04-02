---
title: "Neural Machine Translation by Jointly Learning to Align and Translate"
date: 2022-04-01T00:59:43+09:00
draft: false
---

## This work [[1]](https://arxiv.org/pdf/1409.0473.pdf) is the cornerstone of future  the lots of "attention" mechanism based models. 

The common practice of previous work on Neural Machine Translation (NMT), is first to compress the source sentence to a continuous sentence representation via a RNN-like model, and then re-maps the vector 
back to a sequence of words via decoder-RNN method. Although such end-to-end training framework shows effectiveness, the compressed vector 
usually losses lots of information of Encoder, and results in difficulties for Decoder to decode the vector. This paper proposes a different
scheme that allows the decoder model to automatically search for parts of a source sentence that are relevant to predicting a target word.
The alignment function is achieved by a feedforward neural network which can be jointly trained as all the other parts in the model. 

## Main Results
![your image](/images/8.png)
We see that the improvement is very large (above 50%), which suggests that the alignment/attention mechanism is very powerful. 
The reason is that, alignment allows the target sentence to focus on different parts of source sentence. 

## Attention Visualization
This paper also provides a very good visualization method that helps us better inspect and analyze our models. The visualiation tool 
is also helpful for understanding what is being learned by the models trained. The following is an example from the paper: 
![your image](/images/9.png)

### More in the paper

- this paper has very good writing

We can learn a lot from this paper, not only in its proposed method, but also in its writing skills. For example, one could describe the detailed architecture of proposed model, training 
procedures (hyperparameter settings, training time), and examples in the APPENDIX.  



[1] Neural Machine Translation by Jointly Learning to Align and Translate, Dzmitry Bahdanau, et al. ICLR 2015.