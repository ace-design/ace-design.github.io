---
title: Abstract Syntax Tree Merging in Git

people:
  - seb

level: MSc  
available: true

layout: offer
last-updated: 2019-05-04
---

### Context

In classical version control systems (e.g., Git), software development can be separated using different _branches_. However, at some point, the source code developed inside a given branch needs to be reconciliated with the one pushed by the other software developers. In a perfect world, this intergreation is easy, as the system will automatically merge together the source code seamlessly.

Unfortunately, the world is far from being perfect, and software developers  fear the so-called _merge conflict_. The fact that Git works at the text level is one of the root cause of the total mess such a conflict can create in a project: the tool has no idea of the structrure of the pieces of software to be merged! For example, imagine two developers, _Bob_ and _Alice_. If Alice change the contents if a method `m` in her branch, and Bob move the method `m` to another part of the program, this is considered as a conflict in Git. But it should not be, as considering the semantics of their respective intention, we can automatically reconciliate their editions, and yield an automated merged version of the source code!

In this project, we propose to leverage the Git merge algorithm to provide a tool able to merge source code at the abstract tree level. The key point is to identify how to reconciliate classical conflicts (using real world examples extracted from large scale Java projects) in a better way than the text-based algorithm.

Join the team, _make git-merge great again_!


### Skills and Background

  - loving to craft software;
  - knowing how to use Git, and the meaning of the _MVP_ acronym;
  - fluency in object-oriented programming (e.g., Java);
  - good knowledge in object-oriented software design;
  - knowing software development good practices (i.e, _Clean Code_ by Uncle Bob is on your night table).


### Required role of the student

  - contribution to a research project;
  - contribution to the development of prototypes;
  - discovering state-of-the-art literature;
  - communicating about the work done in the lab (technical report, article).

### References

  - _[Fine-grained and accurate source code differencing](https://hal.archives-ouvertes.fr/hal-01054552/document)_. Jean-Rémy Falleri, Floréal Morandat, Xavier Blanc, Matias Martinez and Martin Monperrus. ASE 2014.
  - _[On the Nature of Merge Conflicts: a Study of 2,731 Open Source Java Projects Hosted by GitHub](https://ieeexplore.ieee.org/document/8468085)_. Gleiph Ghiotto, Leonardo Murta, Marcio Barros and Andre van der Hoek. TSE 2018, ICSE 2019 (Journal-First)
