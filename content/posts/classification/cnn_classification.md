---
title: "Convolutional Neural Networks for Sentence Classificaion"
date: 2022-03-27T00:59:43+09:00
draft: false
---

## Questions: Do you know how to use a Convolutiona Neural Network do text classification task? Do you know how better it is to use pre-trained word embeddings (e.g., word2vec) compared with random representations? Do you know when it is better to further fine-tuning on the embeddings? This paper gives you all the answers [[1]](https://aclanthology.org/D14-1181.pdf).

Initializing word vectors with those obtained from
an unsupervised neural language model (e.g., word2vec) offers great gains in performance. Even a simple convolutional neural network (CNN) on top of the embeddings achieves surprising results, compared with the more sophisticated deep models.
This work explores various CNN-based models for text classification task, and shows the importance of either using static pre-treined embeddings or further fine-tuning the embeddings. 

The proposed model is shown in the figure. 

### Embeddings: Random vs Pre-trained (Word2Vec)
![your image](/images/1v.png)

We see that word2vec initialization works quite well. The results are not surprising because word2vec embeddings are trained on a huge amount of unlabeled text data (hundreds of billions of words), which is task independent and thus has obtained universal knowledge about the real world.

### Pre-trained Embeddings: Fixed vs Fine-tuned
![This is an image](/images/2.png)

The results show that fixed embedding is competitive with further fine-tuning the embedding since the gain obtained by training on the specific data is not very large. We also notice that for CR and MPQA dataset the fixed embedding even wins.
The plausible reason may be that training on a small dataset results in over-fitting. 

### Pre-trained Embeddings: Single vs Mixed
![This is an image](/images/3v.png)

The mixed model is actually the proposed model by this work. It has two independent channels that are static and non-static representations. During training, the static word representations keep fixed while the non-static embeddings updates via gradient descent. We see that the mixed 
model does not always perform well compared to fine-tuned model. These results suggest that the pre-trained vectors are quite good across datasets and tasks.

### More in the paper

- comparison with many baselines 

Those baselines include both traditional machine learning methods and deep neural models. The authors show that the proposed simple model perform quite well against the other models.

- comprehensive benchmark comparisons

The datasets (i.e., MR, SST-1, SST-2, Subj, TREC, CR, and MPQA) cover a range of different tasks, such as sentiment classification, question type classification, and opinion polarity detection task.


### Research Thinking

You may try similar things following this paper, such as exploring various RNN models on various word embeddings for various tasks. 
The following listed could be the possible examples:

- Vanilla RNN + word2vec + text classification
- Vanilla RNN + GloVe + text classification
- Vanilla RNN + BERT + text classificaition
- GRU + word2vec + text classification 
- GRU + Glove + text classification
- GRU + BERT + text classification
- LSTM + word2vec + text classification
- LSTM + GloVe + text classification
- LSTM + BERT + text classification


[1]: Convolutional Neural Networks for Sentence Classification. Yoon Kim. EMNLP ' 14, Pages 1746–1751. 