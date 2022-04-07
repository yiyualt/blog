---
title: "Incorporating Copying Mechanism in Sequence-to-Sequence Learning"
date: 2022-04-03T02:15:30+09:00
draft: true
---

## Questions: Attention mechanism is good, right? Though, is it perfect for all sequence to sequence task? This paper [[1]](https://arxiv.org/pdf/1603.06393.pdf) gives you the answers.  

Attention allows model to focus on different/important parts of source sequence when generating a target token in the target sequence. However, in natural language, we, human beings, do 
no always totally rewrite the sentence. For example, when doing reading comprehension or writing a summary of an article, we may directly copy-and-paste 
several keywords or phrases of the original.  This paper proposes such phenomenon and refers to as copying.  
Therefore, the authors explores the copy mechanism in seq2seq task, and further propose a model called "COPYNET".
The experiments on three dataset/tasks, i.e., synthetic datasets, summarization datasets, and dialogue datasets, show
the superiority of COPYNET to RNNsearch model (attention). 

The COPYNET follows a standard Encoder-Decoder structure. The Encoder is not changed, whereas the Decoder fuses the information of Copy-Mode with Generate-Mode, which stands 
for the probabilities of the current embedding to be kept, and be used for next generation, respectively. 


### Synthetic Dataset
![your image](/images/12.png)

### Summarization Dataset
![your image](/images/13.png)

### Dialogue Dataset
![your image](/images/14.png)

### COMMENT

COPYNET's advantages compared with Attention:

- Achieves better results in some tasks, such as summarization, single-turn dialogue.

COPYNET's disadvantages:

- Cannot generalize well to many other NLP tasks/datasets, where the copy mechanism does not fit.

- Cannot generalize well to many network structures (such as Transformer) other than RNN -based models. 

[1] Incorporating Copying Mechanism in Sequence-to-Sequence Learning. Jiatao Gu, et al. ACL 2016. 