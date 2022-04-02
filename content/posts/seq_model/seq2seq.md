---
title: "Sequence to Sequence Learning with Neural Networks"
date: 2022-03-31T00:59:43+09:00
draft: false
---

## Question: Since you have known that neural networks (e.g.RNN, LSTM) can be used for machine translation task, is it possible to generalize it to general sequence to sequence task?  This paper gives you the answer [[1]](https://arxiv.org/pdf/1409.3215.pdf).

This work present a general end to end sequence learning framework based on LSTM (long short-term memory). The model first maps an input sentence into a fix continuous representation via multi-layer LSTM, then a decoder model comprising also multi-layered LSTM maps the conditioning representation back. 
The model is very powerful and easy to train. The experiments on WMT’14 dataset of English to French translation task show that, 
the proposed model achieves a BLEU score of 34.8, whereas a phrase-based SMT achieves a BLEU score of 33.3. 

Though the model description part is short, the authors show very good and informative implementation details. 

### More in the paper

- The deep LSTM can decode long sequence very well in the semantic space. The following are 2-dimensional PCA projection of the LSTM hidden states.
![This is an image](/images/6.png)

![This is an image](/images/7.png)

[1] Sequence to Sequence Learning with Neural Networks, Ilya Sutskever, NIPS 2014. 