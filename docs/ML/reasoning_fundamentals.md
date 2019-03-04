Title: Reasoning about nature of reasoning
description: My ideas on building blocks on intelligence.
hero: 
author: Abhishek Aggarwal
date: 2019-03-04

# Reasoning about nature of Reasoning
This is messy idea soup, and not meant for public consumption

## Knowledge Representation
Comparison to word embeddings which do not account for context. The idea is that words are just symbols and the context determines which entities they are mapped to. 

This is also the reason that current neural architectures are not interpretable because we do not form embeddings of relations but instead of symbols.

In this new paradigm, we must form embeddings for relations and embeddings

## Reasoning
## Intelligent system
## Learning Intelligent system

- Knowledge is embedded in analogies or relations.

Based on above premise, with enough text data, one shall be able to extract a pretty good (and intelligent) description of world and reason about it.


# All intelligent arguments can be inferred from basic building block relations and set of primitive entities.
Knowledge is then a set of primitive entities and corresponding relations. This need not be a fully connected graph.

A complete knowlege system is one, where one can reason about any two entities in the entity space.

Reasoning is then defined as
1. input -> entity_1
2. relation(entity_2) -> entity_2


# Properties of relations
They are very much like in maths

R(A, B) -> {true| false}
R(A) -> B
R^(B) -> A

Also, given A, B -> one should be able to find the relation (important for interpretability)

Note: this does not mean that R^ must exist as a primitive relation.

A reasoning system must be able to construct all entities from the primitive entities using convex combination.

Imagine a spiders web. If primitive entities are represented at the outer edges of the web, then all the space of new (non-primitive) entities can be created as a linear combination of primitive entities.

# Implementation ideas
|E| -> |R| 

number of possible arguments can then be |R|^(number of steps of reasoning). ( Connection with group theory?? )

One can argue that given the amount of relations and entities, any argument can be made with reason.

Reasoning is then an optimization process to find the **shortest** relation between two (new or primitive) entities. 

This idea can also be used to determine when to stop reasoning.

## Role of context (temporal information, and symbols)
- context is then used solely to map the symbols (or any input modality) into corresponding entities.


## Attributes of Learning system
- learning system must be able to learn primitive entities and relations.
- learn the mapping function
- learning system must be able to contruct new relations (to reduce the amount of computation)

Once set of primitive relations and primitive entities are acquired, along with the mapping (symbol, context) -> entity mapping function, a learning system should be very sample efficient in acquiring new concepts.


## Learning a task
- is tantamount to forming more dense relations amount context/task dependent entities. 


A > B, B > C => A > C

Entities in this respect are just variables. 

It is the job of mapping function to map symbols to these variables.


## Learning 
- relations that most used can follow hebbian learning rule, and thus are not the first one to be overwritten. 
- adding new relations (must take some computation), that is an analogy must be made.
- a new relation (think more) is a composition of premitive relations??? 
- thus a same inference can be obtained by either more computation by applying consequtive compositional relations on entities. 
- Or a shortcut may be formed or repeated application (hebbian learning again?)


## optimization
- use forward prop to form new relations? 
- can forward prop be a one step optimization process to find the analogies?

## Role of memory? 
- Can some emtities or relation be more active due to priming effect of forward processing? Fast Weights? 
- Perhaps priming can activate all the entities and relations connected by few steps to the last used entities and relations.

## demo
- Theorem proving?
- Sample Efficiency
- Interpretabilty?

## also consider adding optimization techniques like
- relative position for text (transformer-xl)


