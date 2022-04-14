---
title: "Explainable Recommendation through Attentive Multi-View Learning"
date: 2022-04-06T00:19:43+09:00
draft: true
---
## Qustions: How do you model aspects from different level (hierarchical structure) for explainable recommender system? This paper gives you the answer [[1]](https://dl.acm.org/doi/pdf/10.1609/aaai.v33i01.33013622).

This work proposes a neural model that modeling aspects/features from **hierachical stratucture**, to predict the future rating score of a item to a given user. 

### Explanation
The explanation is constructed by: pre-defined template + [feature] which is identified as higher attention scores to the final prediction. 

### Not good points
- relily highly on external knowledge (e.g., Microsoft Concept Graph)

[1] Explainable Recommendation through Attentive Multi-View Learning. Jingyue Gao, et al. AAAI'19. 