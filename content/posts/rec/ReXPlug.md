---
title: "ReXPlug: Explainable Recommendation using Plug and Play Language Model"
date: 2022-04-08T00:21:46+09:00
draft: true
---
## Questions: Given a pre-trained model (e.g., BERT, GPT), how do you build an explainable recommender system? This paper [[1]](https://dl.acm.org/doi/pdf/10.1145/3404835.3462939?casa_token=tG-gjQvK5pUAAAAA:Js4NA7pNFAh6YjRI9ttroGKHq3UUw_6Mnvnb13UQ1OO4DWt_oN9YIko1aia5vN_v1Epv1hD_-AtpIQ) gives you the answer. 

This work builds a sentiment classifier (as rating prediction task) on the top of BERT/GPT models, to generate an explanation along with the rating. The results show that the propose ReXPlug performs great in both prediction task and explanation generation task. 

### Main results 
![your image](/images/38.png)
We see that, the proposed RexPlug is comparable to the state-of-the-art approache, CAML. 

### Not good points
- no ablation study, no further analysis. 

- too many abbreviations

[1] ReXPlug: Explainable Recommendation using Plug and Play Language Model. Deepesh V. Hada et al. SIGIR'21. 