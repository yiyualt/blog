---
title: "Joint Deep Modeling of Users and Items Using Reviews for Recommendation"
date: 2022-04-06T00:17:43+09:00
draft: true
---

## Questions: Previous work used content such as review texts as additional features, but do you know how to directly modeling users and items based on reviews? This paper gives you the answer [[1]](https://arxiv.org/pdf/1701.04783.pdf).

This is the one of the first work to model reviews jointly with the ratings. Previous work either to discover the latent
factors by using LDA (Latent Dirichlet allocation) technique, or using the review as an regularization term. The authors
claim that those approaches would limit the representation learning ability for user and items. In addition, note that 
previous work uses only the history interaction (e.g., a pair of **(userID, itemID, review)**) as training data, by contrast, the 
authors instead use the history of reviews written by a user as training data. 

### Main results
![your image](/images/27.png)

### More in the paper
Personally, I believe this is a great paper due to the good performance and simplicity of the proposed model, as well as the clear writing style. 

- the authors show the impact of different initialization strategies, such as tf-idf, random word embedding etc. 

- the more reviews in training, the better results, as shown in Figure 3 in origin paper. 

[1] Joint Deep Modeling of Users and Items Using Reviews for Recommendation. Lei Zheng, et al. WSDM'17. 