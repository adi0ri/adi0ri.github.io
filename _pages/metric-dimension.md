---
layout: page
title: Metric dimension of random geometric graphs
description: Graduate research on landmark selection and whole-graph collision repair.
permalink: /metric-dimension/
---

My graduate research at California State University, Chico studies how to approximate the smallest set of landmarks that uniquely identifies every vertex in a random geometric graph. Each vertex is identified by its vector of graph distances to the landmarks.

## My contribution

Two vertices can have identical distance signatures even when each local region is resolved on its own. I implemented a shared whole-graph repair that finds those pairs, adds landmarks to distinguish them, and verifies the result after pruning.

## Paired benchmark

| Method        | Valid before repair | Valid after repair |
| ------------- | ------------------: | -----------------: |
| Grid          |            36 of 48 |           48 of 48 |
| Zoomed Square |            47 of 48 |           48 of 48 |

These are validity results on the same 48 benchmark graphs. Validity means every vertex has a distinct distance signature. It does not establish that the resulting landmark set is minimum-sized.

[Read my merged pull request and the benchmark details](https://github.com/rctillquist20/random-geometric-graphs/pull/1) · [Research repository](https://github.com/rctillquist20/random-geometric-graphs)
