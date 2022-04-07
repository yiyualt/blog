---
title: "Retrieve, Rerank and Rewrite: Soft Template Based Neural Summarization"
date: 2022-04-04T02:14:57+09:00
draft: true
---

## Questions: 

### Controllable Text Generation
You may know how to generate controllable texts from my post blogs. Specifically, 
Controllable text generation changes the way of "how to say", while keep the modeling
of "what to say". There are several ways to achieve that, for example, we can change
the way of training without changing anything of the internal models. the paper "hooks in headline" [2] 
is an example, which is related with the topic of "style transfer". Alternatively, we may 
embed copy mechanism [3] onto the decoder model to force copying text segment from sources
with probabilities.  






### References
[1] Retrieve, Rerank and Rewrite: Soft Template Based Neural Summarization, Ziqiang Cao, et al. ACL'18. 

[2] Hooks in the Headline: Learning to Generate Headlines with Controlled Styles. Di Jin, et al. ACL'20.

[3] Incorporating Copying Mechanism in Sequence-to-Sequence Learning. Jiatao Gu, et al. ACL'16. 