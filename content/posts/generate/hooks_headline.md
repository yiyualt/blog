---
title: "Hooks in the Headline: Learning to Generate Headlines with Controlled Styles"
date: 2022-04-05T02:15:14+09:00
draft: true
---
## Questions: Do you know how to transfer a source text to target style? Do you know how to generate a more fascinating headline to capture more people's attention? This paper gives you the answers [[1]](https://aclanthology.org/2020.acl-main.456.pdf).

### What to say and How to say

Recently popular sequence to sequence models, i.e., the standard Encoder-Decoder structure-based models, 
are trying to solve the essentially two problems that are "what to say" and "how to say". More specifically, 
the Encoder model compress the text segment (such as a sentence, or sentences) into a distributed
representations, which stands for "what to say". On the other hand, Decoder model solves "how to say". 
Most of the researches focus on "what to say" without much information loss and thus have ignored "how to say". 
In this work, the authors explores an interesting problem, that generate "headline-style" headline. 

The proposed model is also a standard Encoder-Decoder scheme, however, the training is a bit different, which makes 
the style transferring and text summarization connected. Specifically, the model is trained on two task independently, i.e., 
"article -> headline" and "style-text -> style-text". In the training time, the parameters are shared and thus 
performing a multitask learning problem, where the task weight is a hyperparameter.  (Thinking: sequential learning would be better or worse?)

### multitask vs.sequential learning

![your image](/images/18.png)

This result shows that the modification of a basic text summarization model, MASS. The modifications are 
multitask-learning of MASS and sequential learning of MASS on the source (headlines) and target (stylish text) dataset. We
see that the multi-task learning with all parameters are shared greatly outperforms the sequential learning manner. 

### proposed model performance
![your image](/images/19.png)

We see that the proposed model outperforms the baseline by 1%~3%. Though the improvement is not large, 
we think the proposed "Style-Dependent Layer Norm" block may contribute to the improvement.

[1] Hooks in the Headline: Learning to Generate Headlines with Controlled Styles. Di Jin, et al. ACL'20.