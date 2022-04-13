---
title: "Neural Attentional Rating Regression with Review-level Explanations"
date: 2022-04-06T00:18:43+09:00
draft: true
---

## Questions: Do you know how to evaluate/utilize reviews usefulness to modeling recommendation task? How do you know which reviews are more important than others? This paper gives you the answers [[1]](https://dl.acm.org/doi/pdf/10.1145/3178876.3186070).  

### Main results
![your image](/images/28.png)

### Attention weights of reviews
![your image](/images/29.png)
We see that in Item 1, the review a is more useful than review b; in Item 2, review a is more useful than
review a. Higher attention score in NARRE indicates more useful reviews. The authors also did experiments to sho
the correctness and effectiveness of the attention score. 

### Select useful reviews as explanations
![your image](/images/30.png)
The authors also evaluate how precise their NARRE model computes the usefulness of reviews. We see that, 
Precision@1 means, at the percentage of 38.6, NARRE would select correctly the most useful reviews. 


### More in the paper
- good human evaluation with crowd-sourcing



[1] Neural Attentional Rating Regression with Review-level Explanations. Chong Chen, et al. WWW'18.