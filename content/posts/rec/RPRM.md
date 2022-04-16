---
title: "Leveraging Review Properties for Effective Recommendation"
date: 2022-04-07T02:21:43+09:00
draft: true
---
## Questions: Do you know how to use properties in reviews? This paper gives you the answer [[1]](https://arxiv.org/pdf/2102.03089.pdf).

Previous work uses attention mechanism to score each review for representing user/item [2]. In contrast, this work proposes to use reviews instrics (such as rencency, length, helpful votes, prob-helpful, rating, polarity) to compute the usefulness of reviews. The proposed model is RPRM, namely Review Properteis-based Recommendation Model. 

### Main Results
![your image](/images/35.png)
We see that RPRM outperforms the best baseline (NARRE) significantly. 

### Analysis
Different users may focus on different properties. For example, for capturing user A's preference,  the P_vote and review length will contribute more. In contrast, for user C, the reviews' recency, i.e., age, will accounts more. 

![your image](/images/36.png)

![your image](/images/37.png)

### Not good points 
- introduction is too long, which has a lot of overlaps with related work part. 

### References

[1] Leveraging Review Properties for Effective Recommendation, Xi Wang, et al. WWW'21.

[2] Neural Attentional Rating Regression with Review-level Explanations. Chong Chen, et al. WWW'18.