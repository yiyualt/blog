---
title: "Justifying Recommendations using Distantly-Labeled Reviews and Fine-Grained Aspects"
date: 2022-04-06T00:19:43+09:00
draft: true
---

## Questions: How do you think the previous reviews can explain the future decision? This work gives you the answer [[1]](https://aclanthology.org/D19-1018.pdf).

This work constructs an explanation/justification review dataset for the history ratings. The data construction is
(1) to develop a classification model (e.g.,BERT) to extract important reviews that explain why it is good or not (2) extract 
features from ground justifications.


### beam-search vs. top-k sampling
![your image](/images/31.png)
We see that using beam-search decoding is much better than top-k sampling. 

### Att2Seq vs. proposed
![your image](/images/32.png)
We see that the proposed ACMLM does not outperform compared with Attr2seq or Ref2seq.


### Not good points
- too many examples without further analysis

[1] Justifying Recommendations using Distantly-Labeled Reviews and Fine-Grained Aspects. Jianmo Li et al. EMNLP'19.
