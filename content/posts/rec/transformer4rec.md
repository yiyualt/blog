---
title: "Transformer4Rec: Bridging the Gap between NLP and Sequential / Session-based Recommendation"
date: 2022-04-02T01:50:58+09:00
draft: true
---
## Questions: You may be already familiar with Huggingface's Transformers lib, which allows the researchers and practitioners easily to train their own models based on Transformer-type architecture for specific NLP tasks. Is there any similar open source lib for people who are in recommendation community? This paper gives you answers [[1]](https://dl.acm.org/doi/pdf/10.1145/3460231.3474255). 

This work has many contributions:

- an open source library for researchers 

The designed project called Transformer4Rec, enables researchers quickly to implement and customize models with conjunction of the state-of-the-art transformer models in NLP filed. It may greatly foster
the communication between NLP and Recommendation communities. 

- a comprehensive experiment report 

The authors present a very comprehensive experiments on Transformer family models (BERT, Transformer-XL, GPT series, XLNet) modified for sequential and session-based recommendation task. 

- a clear description of the relationship between two tasks

This work gives a very clear description of the difference between sequential models in NLP with Sequential recommendation, as well as their relations. The authors also show the difficulties in 
adapting models to sequential/session-based recommendations.

- the proposal also achieves promising performance compared to the previous models 

[1] Transformer4Rec: Bridging the Gap between NLP and Sequential / Session-based Recommendation, Gabriel de Souza Pereira, et al. RecSys 21. 