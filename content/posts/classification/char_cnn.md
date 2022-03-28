---
title: "Character-level Convolutional Networks for Text Classification"
date: 2022-03-28T00:59:43+09:00
draft: false
---

## Questions: Do you know how to employ a character-level CNN models for text classification task? This paper gives you all the answers [[2]](https://arxiv.org/pdf/1509.01626.pdf).
This paper introduces how to employ a character-level convolutional neural network for text classification task. 
Using character-level models has several advantages: (1) it is more suitable for user generated texts since the model can learn missing letter or misspelling patterns from the data. (2) it does not require external knowledge on the text, such as language, tokenization and so on. The structure of the model is shown in the figure. 


### Compared with important baselines
![This is an image](/images/4.png)

From this figure we see that, char-CNN models are competitive with the sophisticated models (e.g., word-LSTM and word-CNN). Note that the vocabulary for char-CNN is merely 70 characters, thus the parameters need to learn for embedding layer is very small, compared to generally hundreds of thousands of vocabulary size for word-based models. 



### Upper/lower-case or not
![This is an image](/images/5.png)

This result suggest that to distinguish between the upper-lower case would be better choice than not. 

### More in the paper

- char-CNNs work better in larger datasets

They work generally well in large datasets, such as Amazon Review data that contains several millions of training data.

- char-CNNs work better for user-generated data

User-generated data usually has missing letters or misspelling words. word-CNNs cannot deal with such words because the low-frequency words would be filtered out when building a word vocabulary.

- many constructed datasets

This paper has constructed a lot of datasets for text classification, including sentiment polarity classification datasets, topic classification datasets. 

### Research Thinking


[2] Character-level Convolutional Networks for Text Classification. Xiang Zhang, Junbo Zhao, and Yann LeCun. NIPS 2015.