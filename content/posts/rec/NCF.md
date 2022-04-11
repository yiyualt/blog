---
title: "Neural Collaborative Filtering"
date: 2022-04-10T15:58:32+09:00
draft: true
---
## Questions: Neural Network? Collaborative Filtering? How about Neural Collaborative Filtering? [[1]](https://arxiv.org/pdf/1708.05031.pdf).

The authors propose **NCF** (Neural Collaborative Filtering) framework. Under the framework, the author proposes 
further Multi-Layer Perceptron model and Generalized Matrix Factorization Model that could be integrated into one model.
Although the authors claim they're ensembled, I think it is more similar to the framework of Wide & Deep joint learning 
model. 


### More in the paper
- the results show that MLP with 4 hidden layers perform best. 

- pretraining is better than randomly initialization 

- MLP performs than GMF at most of time

### Not good point
- The main results should be written in tables, instead of figure. 

- Table 3 and Table 4 could be integrated in a more concise table.

- related work part is loosen, and could be improved

[1] Neural Collaborative Filtering. Xiangnan He, et al. WWW'17. 