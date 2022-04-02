---
title: "Improving Transformer Models by Reordering their Sublayers"
date: 2022-04-02T01:49:58+09:00
draft: true
---

This paper [[1]](https://aclanthology.org/2020.acl-main.270.pdf) explores the order of modules, i.e., FFN (feedforward network) and multi-head attention  in Transformer model. 
The results show that more attention layers on the bottom and more FFN layers on the top, would result in more robust
model and high-performance results (specific to tasks, and need to explore in the future).

Though the idea of this paper is very simple, it is worthwhile learning from the writing of this paper. 

[1] Improving Transformer Models by Reordering their Sublayers. Ofir Press, et al. ACL 2020. 