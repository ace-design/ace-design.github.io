---
title: Identifying Optimization Conflicts in LLVM

people:
  - seb
  - laure
  - matthieu

level: graduate  

layout: offer
last-updated: 2018-10-31
---

This internship proposal is a joint collaboration between _Université du Québec à Montréal_ (UQAM) and the _Laboratoire d'Informatique du Paralélisme_ (LIP) located in Lyon.  It targets MSc students interested in software engineering (CA) and compilation (FR).


## Context

The [LLVM](https://llvm.org/) project is a compiler infrastructure, defining modular and reusable compiler artefacts. In this context, we will particularly focus on the optimisation passes defined in the LLVM implementation.

An optimisation pass can be modelled as a function _p_ that takes as input an LLVM intermediate representation (_IR_) of the program and produces as output an optimised one: _p: IR -> IR_. Thus, chaining passes means to rely on classical function composition: _p○p'(ir) = p(p'(ir))_.

## Objective

This internship addresses the identification of conflicts between passes. Proving in an absolute way the absence of overlapping among passes is a difficult problem, that will not scale the number of passes available in LLVM. Related work focus on reducing the search space to compute an _Optimized Sequence of Optimization_ (OSO), considering non-functional metrics such as execution time [[1]](https://ieeexplore.ieee.org/document/8326605).


However, similarly to our recent work on rewriting rules interactions [[2]](https://hal.archives-ouvertes.fr/hal-01722040), we would like to provide an empirical analysis of the different passes, from a functional point of view, _i.e._, measuring the functional impact of permuting two passes. Considering that it is too difficult to prove that the optimization passes _o_ and _o'_ commutes (respectively interacts) in the general case, we want to measure if they commute when applied to a specific program _p_.

By applying this approach to a reference corpus of programs, we will gather evidences to then refine the initial results and target specific optimisation passes, _i.e._, the one that have the most impact.

## Expected work

The first task is to understand the LLVM toolchain, and how the optimiser works with the different passes, which can be analysis or rewriting ones. Then, a _distance_ metrics will have to be defined to measure the difference between two intermediate representations.

Let _o1_ and _o2_ two optimisation passes, and _p_ a given program.

  - Let _p12 = o1(o2(p))_, and _p21 = o2(o1(p))_
  - if _distance(p12, p21) = 0_, then _o1_ and _o2_ are said to _commute_ on _p_.
  - If there is a distance between _p12_ and _p21_, then the passes are said to _interact_ on _p_.

The second task is to setup an empirical benchmark that will apply different optimization sequences on a reference corpus, and carefully gather the commutativity / conflict results with respect to the programs under study and the executed passes.

Then, based on these experimental results, we will measure the impact of an interaction. According to the state of the art, this impact can be measured using non functional metrics, _e.g._, execution time. However, considering that the source of the passes is available in LLVM, we want to consider a given pass as a white box and instrument its code to gather metrics about its usage, at a fine grained level. For example, an analysis pass will enrich the intermediate representation with meta-data that are reused by a rewriting one. Measuring the number of time a rewriting phase access to theses metadata will help to finely measure the impact of a given pass to the other one.

## References

1. "A Study of Conflicting Pairs of Compiler Optimizations", Yosi Ben Asher, Gadi Haber, Esti Stein. 11th International Symposium on Embedded Multicore/Many-core Systems-on-Chip (MCSoc), 2017. [Link](https://ieeexplore.ieee.org/document/8326605)
2. "A Delta-oriented Approach to Support the Safe Reuse of Black-box Code Rewriters". Benjamin Benni, Sébastien Mosser, Naouel Moha, Michel Riveill. International Conference on software Reuse (ICSR), 2018. [Link](https://hal.archives-ouvertes.fr/hal-01722040)
3. "LLVM: A Compilation Framework for Lifelong Program Analysis & Transformation". Chris Lattner and Vikram Adve. In Proceedings of the international symposium on Code generation and optimization: feedback-directed and runtime optimization (CGO), 2004. [Link](https://dl.acm.org/citation.cfm?id=977673)
