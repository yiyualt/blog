---
title: "Recurrent Continuous Translation Models"
date: 2022-03-30T00:59:43+09:00
draft: false
---

Questions: How can we employ continuous language modeling for modeling machine translation task? This paper gives you the answer [[1]](http://localhost:1313/posts/seq_model/cnn_rnn/).

In contrast to previous statistical machine translation task which uses neural methods for only re-scoring the best-n translations, this paper introduces a method called Recurrent Continuous Translation
Model (RCTM), that is purely based on continuous representation of both source and target sequence. 

The condition of source sentence is modeled with CNN, while the generation of target sentence is modeled with a Recurrent Neural Network Language Model (RNNLM).
The authors have implemented four experiments to verify the effectiveness of their proposed models.



[1] Recurrent Continuous Translation Models. Nal Kalchbrenner, EMNLP 2013.