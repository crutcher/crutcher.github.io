---
title: The Hot Dense Grid
layout: default
permalink: /roadmaps/hot_dense_grid/
---

# The Hot Dense Grid

A roadmap to easy-to-develop, high-performance,
fully GPU/network saturated, datacenter-scale, sharded
space/time finite grid simulations.

## Background

### Dense Finite Grid Simulations

A large number of valuable problems can be represented elegantly
and succinctly as relatively short sets of tensor field expressions
and operations which describe a simulated
space/time; where local state is described by local variables,
and state evolution is governed by local field equations.
Translated into SQL operations, we would say that state evolution
is governed by window functions, with narrow windows in n-dimensions.

Let's call this set "Dense Finite Grid Simulations".

This set includes a number of extremely high-value problems:
* atomic and molecular dynamics,
* physics field flows:
  * fluid,
  * heat,
  * electromagnetics,
  * optics,
  * weather,
  * ocean and river currents,
* protein-protein interactions,
* and nano-tech simulation

Each of these are trillion dollar problems, and they all
share a common underlying computational algebra.

We should expect that incremental investment in the tooling to
facilitate these simulations will have a tremendous leverage effect
on these problems; yielding far-outsized payoffs to many industries.

### GPU/TPU Tensor Libraries Opportunities

Modern GPU/TPU n-dimensional tensor libraries, though largely
designed for AI modeling, provide many of the core operations
needed to support these problems. As a result,
we are seeing increasing research into implementing solutions
to these problems using these libraries.


