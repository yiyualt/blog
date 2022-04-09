---
title: "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding"
date: 2022-04-03T00:21:35+09:00
draft: true
---

## Questions: You must have heard of BERT, don't you? What is BERT? Why is it so famous? This paper gives you the answers [[1]](https://arxiv.org/pdf/1810.04805.pdf). 

### Transferring Knowledge in NLP
Previous research has demonstrated that employing transferring learning benefits a lot to both CV and NLP fields. 
More specifically, one can pre-train global word representations (i.e., embeddings) based on language modeling task via 
various model architecutres; thus the pre-trained embeddings gives a good initialization for downstream tasks, such 
as Natural Language Understanding, Natural Language Generation, Text Classification; one can then just add 
an additional layer on the top of embedding layers, to achieve the state-of-the-art results.

This work generalizes further the pre-training of word embeddings by bi-directional language modeling tasks and as a result it 
achieves the SOTA word representations in **11** NLP tasks. 

### BERT Details

Please check the [video](https://www.bilibili.com/video/BV1PL411M7eQ?spm_id_from=333.999.0.0).


### Results on GLUE
![your image](/images/24.png)

More about GLUE: 

- MNLI

Multi-genre Natural Language Inference task. Given a pair of two sentences, the goal 
is to predict the second sentence is: (a) entailment, (b) contradiction, or (c) neutral.
(multi-class classification)

- QQP

Quora Question Pairs. Given a pair of two questions, the goal is to predict whether the two
questions are semantically equivalent. (binary classification)

- QNLI

Questions Natural Language Inference. Given a pair of question and answer, the goal is to predict 
whether the answer texts match the question. (binary classification)

- SST-2

Stanford Sentiment Treebank. Given a sentence, the goal is to predict if it's sentiment 
polarity. (binary classification)

- CoLA

Corpus of Linguistic Acceptability. Given a sentence, the goal is to predict whether an English 
sentence is linguistically "acceptable". (binary classification)

- STS-B

Semantic Textual Similarity. Given a pair of sentences, the goal is to predict the semantic 
similarity between the two sentences from 1 to 5. (multi-class classification)

- MRPC

Microsoft Research Paraphrase Corpus. Given a pair of sentences, the goal is to predict if 
the sentences are semantically equivalent. (binary classification)

- RTE

Recognizing Textual Entailment. Given a pair of sentences, the goal is to predict if 
the second sentence is entailment of the first sentence. (binary classification)


### More in the paper

- experiments on SQuAD 1, SQuAD 2, and SWAG

Different to GloVe paper which only evaluates the word embedding based on precision score of analogy task proposed 
in word2vec paper, this work evaluate the word embedding performance on many downstream tasks, instead. 
As the experiments are comprehensive and the performance of proposed model is thus more intuitive
and feelable, the success of BERT paper is predictable.

- difference to GloVe, word2vec

The main goal of either GloVe paper or word2vec is to obtain a good representation of words/sentences. Therefore, 
one may need to redesign the models except for embedding layer, for downstream tasks at hand. 
These processes are tedious, which is BERT paper tries to solve as well. In contrast, 
this work does not only present a good word embeddings, but also the designed model are generally 
fitable to most of NLP tasks, such as text classification tasks. The reported results show that BERT
performs quite good both in fine-tuning style or feature-based style. This is also why there is no need
to compare with GloVe or word2vec papers.

- masking strategies

This paper introduces masked language models (MLM), together with many tricks for training while masking
(a) token(s). For more details, you may check the paper in [1]. 

### Not good points

- the reported results should be test on TEST, not DEV


[1] BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. Jacob Devlin et al. (Google AI Language). NAACL'19.  