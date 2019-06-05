---
title: Safe Deployment of Micro-services Using Containers

people:
  - seb
  - naouel

level: MSc  
available: true
priority: 2

layout: offer
last-updated: 2019-05-05
---

### Context

Micro-services architectures relies on small and independent entities (the micro-service) that communicate with others to achieve business goals. These entities communicate together using messages exchanged on top of a broker, _e.g._, Kafkfa.

In this project, we are interested by the safe deployment of micro-services architecture. It aims to model a micro-service in terms of exchanged messages, and see how the different services define a choreography of messages. then, we will leverage this model to _(i)_ accelerate the deployment by generating software artifacts (_e.g._, docker compose file) that are consistent by nature (no dangling services), and _(ii)_ provide a support to _what-if_ scenarios in the architecture.  For example, what is the impact of a failure of a given service? Can we replace a given service by another one?

The technological ecosystem is build on top of state-of-the-art industrial tools, such as docker, nodeJS and Kafka. The project will deliver a model to represent a service, and a set of analysis to leverage this model and provide feedbacks to software architects.



### Skills and Background

  - loving to craft software;
  - knowing how to start a docker container
  - some knowledge in distributed systems (e.g., networking, message-based communication)
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

  - _[Building microservices: designing fine-grained systems](http://ce.sharif.edu/courses/96-97/1/ce924-1/resources/root/Books/building-microservices-designing-fine-grained-systems.pdf)_. S. Newman. 2015. O'Reilly.
  - _[Research on Architecting Microservices: Trends, Focus, and Potential for Industrial Adoption](https://ieeexplore.ieee.org/abstract/document/7930195)_. Paolo Di Francesco, Ivano Malavolta and Patricia Lago. 2017 IEEE International Conference on Software Architecture (ICSA)
