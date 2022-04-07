---
title: "Efficient Estimation of Word Representations in Vector Space"
date: 2022-04-02T12:48:05+09:00
draft: true
---
## Question: Do you know the power of word vectors? What are they and what are in them?  These papers [[1]](https://arxiv.org/pdf/1301.3781.pdf) [[2]](https://proceedings.neurips.cc/paper/2013/file/9aa42b31882ec039965f3c4923ce901b-Paper.pdf) give you the answer. 

Continuous word vectors are computed by different language models, including Neural Network Language
Model (NNLM) and Recurrent Neural Network Language Model (RNNLM). In those methods, the main task is 
language modeling while the yield word vectors are side effects. Therefore, the yield word vectors have two
problems: 1. quality is not high (we will talk later on the measurement of word vectors' quality) 2. the compuataion speed
is too slow due to the model structure and training strategies. 

In contrast, this work focuses on computing high-quality word embeddings. Specifically, 
the authors proposed two interesting models, called Skip-gram and Continuous Bag of Words (CBOW) 
for capturing good word embeddings. The experiment on Google News corpus shows that the proposed models 
perform very well that they can capture syntactic and semantic regularities, which is surprising phenomenon.

### Compared with traditional language model 
![your image](/images/20.png)
We see that, the proposed skip-gram and CBOW models greatly outperform other NNLM models based on semantics
and syntactics, trained on Google News corpus. 

### negative sampling vs. hierarchical softmax
![your image](/images/21.png)
We see that the negative sampling strategy greatly outperforms hierarchical softmax approach. 

### More in the paper

- hierarchical softmax

Hierarchical softmax function employs a tree-based structure, such reducing the N complexity to log(N) complexity.


- negative sampling strategy

The author modifies the noise contrastive estimation (NCE) strategy to language modeling, thus proposing also a novel sampling approach, 
Negative sampling (NEG),  which can significantly speed up the training and results in better vector representations. The negative sampling
is an alternative to hierarchical softmax. 

- sub-sampling startegy

Rare words are more important than frequent words. The sub-sampling adopts an empirical formula that 
**discard words** while training. The experiment shows that it accelerates learning and even
significantly improves the quality of learned representations of the rare words. 


### Not good points

The quality of learned word vectors are most evaluated qualitatively, which is not 
strongly convincing. We argue that examples combined with automatic evaluation measures 
would be more convincing. 

### References

[1] Efficient Estimation of Word Representations in Vector Space. Tomas Mikolov et al. ICLR'13 Workshop.

[2] Distributed Representations of Words and Phrases and their Compositionality. Tomas Mikolov et al. NIPS'13.