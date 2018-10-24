---
title: Scalable Software Composition

description: |
  Separating concerns without being able to recompose them in a scalable way does not make sense. There is a need to consider this class of issues as a first-class citizen with respect to current software development to accelerate it. 

people:
  - seb
  - ben
  - mireille
  - sebseb

layout: project
last-updated: 2018-08-24
---

The Separation of Concerns (SoC) paradigm relies on the idea that decomposing a problem into different smaller sub-concerns helps to tame its complexity, and that automatic composition will make it possible to rebuild a complete system. However, separating without being able to recompose in a scalable way does not make sense: ultra-large-scale systems require to compose concerns from different domains, where a choice in a given domain impacts another choice in another domain. Until now, a huge and coordinated effort is necessary to define, analyse, assess. and validate composition operators for a dedicated domain. This triggers a scalability challenge for the SoC paradigm itself. For example, in a dynamic context, an automated engine triggers composition to (de)activate features in the system. If the composition operators used are not commutative or idempotent then the composition order has consequences, making it difficult to develop the adaptation rules. An industrial example is the way a Docker image (the de facto standard for deployment) is composed with others to create turn-key software stacks: the elements added during the composition might interact with the ones that pre-exist in the base image (and it is part of Docker’s business model to verify such consistency for premium users)

We envision the definition of an _Abstract Composition Engine_ (ACE) that will factorize knowledge about software composition and support engineers when defining new ones for their very own domain. The requirements of the ACE were expressed thanks to externally funded projects (see CCV) with industrial partners and international experts. Instead of rewriting each part of the composition from scratch in their own universe, they will be able to reuse off-the-shelf elements and customize them for their needs. Automated reasoning approaches will analyze the given artifacts and the used operators to automatically infer properties – thanks to static analysis or reference benchmark usage –on the composed system and to support its assessment in a scalable way. Such properties can be functional (i.e., domain-specific) or non-functional (e.g., associativity, idempotency).  Based on these properties, it is possible to analyze the expressed composition directives and the resulting model. The idea is to apply approaches like query rewriting to optimize the composition directives in a scalable way. 

### Ongoing projects:

  - Composition d'Applications pour "Mobile Earthquake Recorder in Marine Areas by Independent Divers" (MERMAID), (2017-2020)
  - Modelling Software Composition (2016-2019)


