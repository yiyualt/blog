---
title: "BPR: Bayesian Personalized Ranking from Implicit Feedback"
date: 2022-04-10T15:54:32+09:00
draft: true
---


## Questions: in implicit recommendation scenario, how do you differentiate the "dislike" and "unseen"? This paper gives you the answer [[1]](https://arxiv.org/pdf/1205.2618.pdf). 

**Problems** in common practice for modeling implicit recommendation. In implicit recommendation scenario, the goal of a recommender system is 
to rank the unseen products and display to users from top to down. However, as only the implicit data are available such as purchase and view, it is difficult to differentiate the unpurchased or
unseen data is "Disliked" or "Neutral" by the users. 

The common practice of previous recommender systems, including **matrix factorization** or **knn-based** approaches 
simply model the observed data as positive class and unobserved data as negative class. Then, they construct
a **binary classifier** training on the observed data and use the model to predict probability distributions 
for unobserved data. Finally, the products are ranked in terms of the predicted values.
However, such models cannot distinguish the neutral data and disliked data as they are both modeled as negative class while 
training. 

This work solves this problem by proposing a novel ranking based metric and further proposed model, called BPR, 
Bayesian Personalized Ranking. The proposed model cannot only achieve the best performance compared to MF or KNN-models, 
but also it can be easily integrated on those models. 


### Main ideas
The main idea of BPR is that, instead of labeling observed as 1 and unobserved as 0,
this work constructed a **pair of observed and unobserved**, i.e., (observed, unobserved) while the observed > unobserved. 
In this way, in inference time, the predicted rank is actually the final rank. Therefore, 
BPR models **relative ranking**, rather than absolute ranking. But how to solve the ranking contradiction cases, 
where a>b, b>c, but a<c?


### BPR models
What the BPR models does is to design a novel training metrics, (or, loss function) based on AUC. The 
authors provide many maths here to induce that BPR-Opt is totally differentiable. One may easily use 
backward and many gradient descent algorithms such as SGD, to train to get the optimal parameters.

### Main results
![your image](/images/25.png)

We see that, in ranking task, BPR+MF performs best than the other baselines, including 
both MF and KNN -based models.

### More in the paper

- how to construct the training data

- why it works

### Not good in this paper
- the experiment parts could be extended to include more analysis and results, rather than solely providing main results.

we may learn from this paper how to construct the training data. 

### References
[1] BPR: Bayesian Personalized Ranking from Implicit Feedback. Steffen Rendle et al. UAI'09.

