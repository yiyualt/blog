---
title: "Factorization Machines"
date: 2022-04-10T15:55:32+09:00
draft: true
---
## Questions: You must have heard of the well-known model, Factorization Machine. So, what do you think it is? Is it a machine? Is it a timer machine? Is it a model? Is it an algorithm? This paper gives you the answers [[1]](https://www.csie.ntu.edu.tw/~b97053/paper/Rendle2010FM.pdf). 

Factorization machine is a generic classifier that can deal with large, sparsity data. 
This work starts from support vector machine (SVM) and incorporate with factorization models to achieve
a new model class.

The advantages of Factorization Machine is as follows: 

- It is a general classifier that can deal with huge, sparsity data

- It can work on any type of feature vectors. For example, by combining the features of user and items as well as their
interactions, factorization machine can achieve comparable results with the state-of-the-art factorization models in recommendation
scenarios.


### FM vs SVM

![your image](/images/26.png)
We see that, with the increase of feature dimensions, the loss of FM keeps decreasing where the traditional
SVM model fails.

### More details in the paper
- why can it deal with sparsity problem?

- which order of FM would be the best?


### Comment 
The really amazing thing about factorization machine is that, it can capture the interactions of 
features in a very efficient way. 

[1] Factorization Machines. Steffen Rendle. ICDM'10.