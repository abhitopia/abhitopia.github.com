Title: Reconciling deep learning with symbolic artificial intelligence
description: Paper Summary
hero: Paper Summary (WIP)
authors:
    - Abhishek Aggarwal
date: 2019-03-06

[Link to article][MartaGarnelo12MurrayShanahan_18]

I must admit that I discovered this article trying to build my **original** ideas, and I was pleasantly surprised on how it overlapped 80%-90% on what I had come to conclude even before reading this. It is reassuring that to know that people who are far more qualified, and who have spent way more time than I have on this topic have come to similar conclusion (albeit with more references). Self adulation aside, lets get to business.

### Deep Learning
#### Shortcoming in Deep Learning
They categorize (with examples) which are fairly common and intuitive with current Deep Learning method.

1. **Data Inefficiency**: Need no less than a simulator for Deep RL and millions of samples in old-fashioned DL.
2. **Poor Generalization**: In ability to _transfer_ or _reuse_ learning to a (even slightly) different domain.
3. **Lack of Interpretability**: Black box phenomenon.

#### Strengths of DL

1. **Data driven automatic representation (and compute) learning**: Throw in huge amount of data, and a suitable optimizer and wait.

### Symbolic AI
Most predominant until 1980s, in symbolic AI, representations are typically _propositional_ in character, and assert that certain relations hold between certain objects, while each reasoning step computes a further set of relations that follow from those already established, according to a formally specified set of inference rules. As reminder (and mathematically speaking), a proposition is a statement that evaluates to either True or False. Predicate is a _function_ or mapping that takes variables produce propositional output. A relation is a predicate of two variables.

#### Shortcoming of Symbolic AI
1. **Hand crafted representation**: It is not clear how the representations can be learned from data and have traditionally been hand crafted to be used. This is known as [_symbol grounding problem_][SymbolGroundingProblem]. The contrast with DL is obvious.

#### Strengths of Symbolic AI
Strengths typically align with shortcomings of DL.

1. **Data efficiency**: thanks to their declarative nature, symbolic representations lend themselves to re-use in multiple tasks, which promotes data efficiency. There is mostly no training needed, as the rules are often handcrafted.
2. **Cross-domain generalization**: Symbolic representations tend to be high-level and abstract, which facilitates generalisation. As long as symbols are mapped to correct variables, and problem is correctly formulation in Symbolic AI language.
3. **Interpretable**: Because of their language-like, propositional character, symbolic representations are amenable to human understanding. The predetermined rules of inference can be examined by humans.

WIP, more to follow.
#### Compositionality 
**Show that this can be done using Tensors**

#### Relational Representation
**Can be done using Tensors**

It is easy to show that each layer of feed-forward network is than one function.

[MartaGarnelo12MurrayShanahan_18]: https://www.sciencedirect.com/science/article/pii/S2352154618301943#bib0255
[SymbolGroundingProblem]: https://www.sciencedirect.com/science/article/pii/0167278990900876