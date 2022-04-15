---
title: "Dual Learning for Explainable Recommendation: Towards
Unifying User Preference Prediction and Review Generation"
date: 2022-04-06T02:20:44+09:00
draft: true
---

## Questions: To first recommend, or first explainable, that is a question. Fortunally, this paper gives you the answer [[1]](https://dl.acm.org/doi/pdf/10.1145/3366423.3380164).

Previous work adopt a weighted sum of prediction task and explanation task in a multi-task learning manner. In contrast, this work connects the two tasks via a duality loss function as a regularization term. Then, the training is in sequential learning manner. The experimental results show that the performance of the proposed DualPC well outperforms the multi-task manner, i.e.d, NRT model. 

Moreover, the authors also design a novel computing mechanism that guide the model to inference in test time without the given review. 


### Prediction task
![your image](/images/33.png)
We see that, DualPC > NARRE > DeepCoNN > NCF while performing the prediction task. 

### Explanation task
![your image](/images/34.png)
We see that in explanation generation task, the DualPC still outperforms the baselines. 


### Not good points
- need more experimental analysis, other than the main results. For example, I have expected more analysis on the duality function. Although I see some preliminary results on this, e.g., Figure 5. However, perhaps we need more insights?

- the way of how marginal probability of C and R are computed, is not optimal, though. They're fixed value but have little guidance or idea why. 


### Reference
[1] Dual Learning for Explainable Recommendation: Towards Unifying User Preference Prediction and Review Generation. Peijie Sun, et al. WWW'20.