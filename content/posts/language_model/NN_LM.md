---
title: "A Neural Probabilistic Language Model"
date: 2022-03-29T00:59:43+09:00
draft: false
---

## Questions: How do you know if a sentence is more likely to appear than another sentence? Do you know how likely a certain word appearing to the end of a text chunk? Yeah, you may, and should know the answer. It is exactly the language modeling! 

In the past, people used statistical approaches (e.g., n-gram and its variants) to solve language modeling task. But the flaws are apparent: it knows nothing about the word (makes no use of word similarity); the generated text are low-quality and many repeated text chunks due to the fixed n-gram models; when the vocabulary size and sequence length is long, the probability computation suffers from a ["high-dimension curse"](https://en.wikipedia.org/wiki/Curse_of_dimensionality).

This work solved such issues by a totally different design: (1) first, one could represent words as k-dimensional discrete variables (the idea of word embedding, though it cannot be called embedding yet); then, the sequence of word representations are passed to a function (the function is learned by neural network) and mapped to a word distribution probability, which is a continuous value. By moving from the start of the sequence to the end, one may obtain the likelihood of the sentence. 
The metrics used for training is text [perplexity](https://en.wikipedia.org/wiki/Perplexity). After training, we cannot only obtain the probability of the sentence, but also obtain the word representations. 
By the word representations, similar/synonyms words can be used. For example, having seen the sentence _The
cat is walking in the bedroom_ in the training corpus should help us generalize to make the sentence _A dog was running in a room_ almost as likely, simply because "dog" and "cat", "walking"
and "running" have similar semantics and grammatical roles. 

### More in the paper
- introduces many tricks for training the model

In early days, it is very hard to train a deep neural network model, not only because the hardware capacity but also because there does not exist handy deep learning framework as these days (Tensorflow, PyTorch, Theano etc.)

- initialization does not matter too much

The authors compared the randomly initialized word representations with SVD (singular vector decomposition) initialization. The results show marginal improvement at rate of 0.3%.


[1] A Neural Probabilistic Language Model. Yoshua Bengio, Rejean Ducharme, and Pascal Vincent. NIPS 2000.