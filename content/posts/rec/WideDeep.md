---
title: "Wide & Deep Learning for Recommender Systems"
date: 2022-04-10T15:56:32+09:00
draft: true
---

## Questions: What is a modern deep learning based recommendation system? This paper from Google gives you the answers [[1]](https://arxiv.org/pdf/1606.07792.pdf).

Traditional recommender systems use collaborative filtering (CF) or content-based, or matrix factorization methods, or hybrid models. 
The generalization and memorization problems generally exist on those systems. As we introduce in [this](http://localhost:1313/posts/rec/fm/) blog, factorization
matrix well captures the interactions between all hidden vectors (i.e., embeddings) via dot product, which motivates this work. 
In contrast, this work employs multi-layer perceptron to capture the non-linear interaction between all the embeddings. 
Therefore, what is where the name "wide & deep" comes from, which is further the generalization of factorization machine.

### the development of embedding based recommender system. 

- stage-1: people initialize the embedding layer for both users and items, i.e., latent factor; 
then, they use the **dot-product** as the predicted values; then the errors on the training data can be back-propagated to update 
the user and item representations (embeddings, latent factors). This is the type of matrix factorization approaches. 
The only difference between various models lies in the **regularization term**, for example, SVD imposes the restriction of singular vectors, while
NMF imposes the restriction of non-negativeness, and so on. The reasons for doing so is to try to 
solve/eliminate problems including over-fitting, sparsity, etc. 

- stage-2: the problem of the above models is that, the interaction between features are not captured. For this, the work [2]
proposes **factorization machine** to also computes the interaction between the features in high-order at the cost of linear time. 
The design of the computation is very sensible and thus becomes a very successful work.

- stage-3: the problem of the factorization machine is that, they compute the interaction by dot-product, which 
can only capture the linearity of features (it is not strictly correct, because the 2-nd order computation is not linear). 
Therefore, the team from Google company employ the **deep neural network** to eliminate the aforementioned problems.

### Main idea
The main idea is simple, which is: some features are suitable for wide network while others are more suitable for deep network. 
The combination output of wide & deep parts are then weighted for the final prediction, where the weights are learned via training.

### More in the paper
- what does it mean "joint training"? 

- good implementation of the whole engineering work.

### Not good points
- no baseline comparison

[1] Wide & Deep Learning for Recommender Systems. Heng-Tze Cheng et al. Google. 2016 Workshop of Deep Learning for Recommender System. 

[2] Factorization Machines. Steffen Rendle. ICDM'10.