---
title: "A Zero Attentive Relevance Matching Network for Review Modeling in Recommendation System"
date: 2022-04-06T00:21:42+09:00
draft: true
---

### Model 



### Static Embedding vs. Dynamic Embedding

![your image](/images/15.png)
We see that the static representations of user and item outperform the dynamic representations. The result shown in 
this figure agrees with the comparison of other static and dynamic methods. 

### Static Embedding vs. Mixed Embedding

![your image](/images/16.png)
From this figure, we can see that the fuse of static and dynamic embeddings of user 
and items achieves the best performance. The reason may be that: static embeddings captures 
the user and item intrinsic properties (such as taste of a user and the price of an item), whereas
the dynamic representations learns the interaction knowledge between user and item. 
Therefore, the intrinsic properties incorporated with interactive knowledge better
models the recommendation scheme. 

### More in the paper

- siamese models outperforms interaction-based models

The plausible reason can be that the interaction-based models force to extract information from user-item
reviews, whereas not very review is useful to the target. Thus, this fact leads to over-fitting while training. 

- auxiliary loss in the training objective contributes to positive gain

The auxiliary loss is based on the computation of relevance matching function. Though the paper shows that the 
auxiliary loss contributes a lot in improving the final prediction results, I, personally think that
it would be better to train/design a model in an end-to-end training manner. 

- interaction-based representations on item side may not as profitable as they are on the user side

This may be due to the difference between the number of reviews per item with the numer of reviews per user? (not verified)

[1] A Zero Attentive Relevance Matching Network for Review Modeling in Recommendation System. Hansi Zeng, et al. ECIR 21.