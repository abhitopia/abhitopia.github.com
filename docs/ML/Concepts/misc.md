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


### Logic Tensor Network
The paper doesn't as good of a justice to the theory they develop in the tutorial. They lay the foundation of first order (fuzzy) logic in tensors. The tutorial is also a good introduction to fuzzy logic.

- [Tutorial, Code, Notebooks](https://sites.google.com/fbk.eu/ltn/tutorial-ijcai-2018)



### Model confidence recalibration
I stumbled upon [this blog](http://alondaks.com/2017/12/31/the-importance-of-calibrating-your-deep-model/) post when I noticed that after training my model for longer (and consequently obtaining higher accuracy), the confidence thresholding didn't work as well. This also hijacked the highly confident beams during beam search. 
The post is baed on a nicely written article, link below.

- [Paper](https://arxiv.org/abs/1706.04599)
- [Pytorch Code](https://github.com/gpleiss/temperature_scaling)

#### My two cents
- This has not been tried in NLP settings. I am in process of implementing it now as part of my work at True AI. I shall post the results after.


## Symbolic Reasoning, Inductive Logic Programming, Link Predict, Program Synthesis

### From Machine Learning to Machine Reasoning
Old classic and discusses some plausible requirements and neurological evidence for the basis of intelligence.
- [Paper](https://arxiv.org/pdf/1102.1808.pdf)

### Differentiable Inductive Logic Programming
- [Paper](https://arxiv.org/pdf/1711.04574.pdf)

### Logical Rule Induction and Theory Learning Using Neural Theorem Proving
- [Paper](https://arxiv.org/pdf/1809.02193v1.pdf)

### Lifted Rule Injection for Relation Embeddings
- [Paper](https://arxiv.org/abs/1606.08359)
- [Video](https://vimeo.com/239247564)

### End-to-end differential proving
- [Video](https://www.artificial-intelligence.video/end-to-end-differentiable-proving-tim-rocktaschel-university-of-oxford)
-[Paper](https://arxiv.org/pdf/1705.11040.pdf)

### Programming with a Differentiable Forth Interpreter
- [Paper](https://arxiv.org/abs/1605.06640)
- [Code](https://github.com/uclmr/d4)
- [Video](https://vimeo.com/238227890)

### Differentiable Programs with Neural Libraries (Terpret)

- [Paper](https://arxiv.org/abs/1611.02109)
- [Paper 2](https://arxiv.org/pdf/1608.04428.pdf)
- [Video](https://vimeo.com/238227833)
- [Code](https://github.com/51alg/terpret)

### Differentiable Functional Programming (scala)
- [Video](https://www.youtube.com/watch?v=igRLKYgpHy0)


### Differentiable Functional Program Interpreters
- [Paper](https://people.csail.mit.edu/feser/2016nfp.pdf)


### A curate list on code induction and synthesis
- [link](https://github.com/src-d/awesome-machine-learning-on-source-code)

### Adventures in Neuro Symbolic Machine Learning
- [Slides](https://homepages.inf.ed.ac.uk/csutton/talks/adventures-neurosymbolic-2018/adventures-neurosymbolic.pdf)


### Tensor Product Programming Language
- [Paper](https://scholar.colorado.edu/cgi/viewcontent.cgi?article=1574&context=csci_techreports)
- [Introduction to Tensor Decompositions and their Applications in Machine Learning](https://arxiv.org/pdf/1711.10781.pdf)
- [Tensor Decomposition](https://ebiquity.umbc.edu/_file_directory_/papers/833.pdf)


### Weight Decay, BatchNorm and connection with learning rate
- [Blog](https://blog.janestreet.com/l2-regularization-and-batch-norm/)

