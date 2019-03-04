Title: Misc topics and papers
description: 
hero: Topics and papers I find interesting in Machine Learning
author: Abhishek Aggarwal
date: 2019-03-03

### NLP benchmark
- [NLP Progress website](http://nlpprogress.com/english/language_modeling.html)

### Tranformer XL
- [Code and pretrained model](https://github.com/kimiyoung/transformer-xl/tree/master/pytorch)
- [Paper](https://arxiv.org/pdf/1901.02860.pdf)

### AWD-LSTMS
This is a great blog on the underlying concept and should help implement the same in trudle. It would be also 
good to see how awd-lstm compare with attentive awd-lstms. 

- [Blog](https://yashuseth.blog/2018/09/12/awd-lstm-explanation-understanding-language-model/)

### RNN training methods and corresponding computational complexity
- [Paper](https://web.stanford.edu/class/psych209a/ReadingsByDate/02_25/Williams%20Zipser95RecNets.pdf)

### Short term memory for RNNs
This paper propose by Jimmy Ba and Hinton, proposes an old idea of using Hebbian like learning rule on 2nd order TPR representations to augment traditional RNN to incoorporate temporary, short-term memory.
 
 - [Paper](https://arxiv.org/abs/1610.06258)
 - [Fast weight memories](https://pdfs.semanticscholar.org/f862/0fb17d7e0e41c44c1e87fe3693daad0d30bd.pdf)
 - [Video](https://www.youtube.com/watch?v=Hd20zGKAdoI) by Jimmy
 - [Video](https://www.youtube.com/watch?v=GLmptInTNSw) by Hinton

#### My two cents
- Can this be combined with Neural Ordinary Differential equation to determine automatically determine the length of inner loop?
- Can decay parameter be learning, than have constant exponentail rate decay?
- It will be interesting to see how large scape Ulmfit like language model trained using truncated BPTT will do. If it works, it should be faster (and real time) during inference compared to attentional variants including Transformer XL.

### Symbolic Neural Reasoning using TPR
This follows on Paul Smolensky work on symbolic reasoning using TPR and gives an end-to-end learning framework using Fast-Weights update of third order TPRs. Very interesting paper, which scope to build upon further.

- [Paper](https://papers.nips.cc/paper/8203-learning-to-reason-with-third-order-tensor-products.pdf)

#### My two cents
- Authors haven't been able to integrate it to a full fledged LSTM (or unable to make it work). The idea is novel and needs further investigation.


### Graph Neural Networks
- [Paper](https://arxiv.org/pdf/1806.01261.pdf)
- [Paper](https://arxiv.org/pdf/1810.00826v1.pdf)
- [Blog](https://medium.com/intuitionmachine/intuitive-relational-reasoning-for-deep-learning-3ae164f9f5cd)

### Neural and Symbolic Reasoning
- [Workshop](http://neural-symbolic.org/)
- [Course](http://tiarkrompf.github.io/cs590/2018/)
- [FOL Theorem Proving Dataset](https://archive.ics.uci.edu/ml/datasets/First-order+theorem+proving)
- [HolStep Dataset](https://arxiv.org/abs/1703.00426)
- [DeepMath - Deep Sequence Models for Premise Selection](https://arxiv.org/pdf/1606.04442)

#### My two cents
- Theorem proving and theorem validation is epitomy of symbolic reasoning. It would be interesting to see how the Fast-weights and TPR variants above do on these tasks.
