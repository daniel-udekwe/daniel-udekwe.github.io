---
layout: post
title: I was awarded the Unitary Fund microgrant to build QHDOPT
date: 2023-06-27 13:00:00-0400
inline: false
related_posts: false
---

I am excited to receive the [Unitary Fund microgrant](https://unitary.fund/grants/) (co-PI: Yuxiang Peng) to build an open-source software package **QHDOPT** for nonlinear optimization.

[Quantum Hamiltonian Descent (QHD)](https://arxiv.org/abs/2303.01471) is a quantum algorithm for continuous optimization. QHD can be implemented on spin-glass simulators (e.g., D-Wave) and demonstrates a significant advantage for solving non-convex problems. QHD can also be readily integrated into a branch-and-bound framework and leads to powerful commercial solvers. Despite the significant interest from the operations research community, implementing QHD on quantum hardware remains challenging for researchers without systematic training in quantum computing. We propose to develop QHDOPT, an end-to-end QHD-based nonlinear programming OPTimizer that eliminates the technical barrier of using QHD for the broader scientific computing community. In the ecosystem, only a few projects (e.g., ToQUBO.jl) target nonlinear optimization by directly reducing continuous problems to discrete ones regardless of the continuity structure. To our best knowledge, QHDOPT will be the first of this kind in the field.
