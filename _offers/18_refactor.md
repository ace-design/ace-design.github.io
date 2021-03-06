---
title: Composing Code refactoring

people:
  - seb
  - ben

level:
  - MSc
  - PhD

available: false

layout: offer
last-updated: 2018-10-31
---

### Summary

Software code is often subject to code refactoring. This is the essence tof test-driven development: _(i)_ test, _(ii)_ code, _(iii)_ make test green, _(iv)_ refactor. Refactoring is often performed manually, or with a support from the IDE. But the information that a given refactoring happened is lost, leading to the infamous "I told you so" versioning anti-pattern where 2 alternative design are constantly added and removed in the given system. We propose in this project to formalise the classical code refactoring and to remember their application, supporting developers at both level: _(i)_ making easy to apply a refactoring to a given piece of code and _(ii)_ reasoning on the sequence of refactoring made in a given project.

### Project Description

We consider here the refactoring defined by Fowler in his seminal book. In the project, students will provide a framework where an expert can implement a refactoring rule. Then, according to the available catalogue, a developer will be able to select the rule to apply, configure it and automatically apply it to her source code. Then, The system will version this application in a way that the whole story will be available to support reasoning.

For example, a developer _d_ asks the system to refactor a class `C` into `C'` (applying a renaming rule). The system will automatically apply the modification to the source code. The system will also warns the user that this class wal already named `C'` two month ago. The idea is to reason on the sequence of refactoring to provide a better support for end-user. In addition, it can also help conflict resolution when performing code merge (by computing the canonical sequence of refactoring to apply when refactoring were performed in ≠ branches).

### Expected Skills

  - good knowledge of the Java programming language
  - affinity with code generation, reflexivity and metaprograming
  - logical reasoning

### Requirements

The refactoring rules will be implemented in Java (e.g., using Spoon), and the project will cover well defined rules extracted from Fowler's book. The user will interact with the rules using a CLI as a minimal and viable product, and a possible integration into a classical IDE such as IntelliJ or Eclipse. The project will use Git as versioning control system to support refactoring versioning.

### Expected results

  - a framework to express refactoring rules
  - experiments showing how the rules can be applied to Java code
  - Reasoning on sequences of refactoring rules to warn users or support better merge.

### References

  - [https://martinfowler.com/books/refactoring.html](https://martinfowler.com/books/refactoring.html)
