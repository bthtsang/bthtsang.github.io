---
permalink: /starsend2end/
title: "An End-to-end Software Pipeline to Simulate Exploding Stars"
author_profile: false
---

![Predicted vs True Eexp](/files/vr_dens_iter.gif)
Volume rendering of the gas density around an exploding star. Color and opacity show the density from high (red/opaque) to low (blue/transparent).

[//]: # (Context, role, goal)

## Context

When massive stars approach the end of their lives, they explode violently as supernovae.
These cosmic explosions are the results of many inter-dependent physical processes: nuclear fusion and neutrino transport at the cores of the stars, convective and supersonic gas flows, all in the presence of strong gravity and turbulence.

In order to realize these explosions in simulations, scientists rely on a handful of physics solvers each responsible for a subset of physics relevant to a certain stage of explosion.
However, there is no existing end-to-end pipeline for the process -- scientists have to manually traverse the software stack; each layer of the stack often requires days to learn and a PhD to master. 

### Objective

Joining forces with a few researchers who are masters of various layers of the software stack,
we set out to construct an end-to-end simulation pipeline capable of evolving stars from their births all the way to their explosive ends. 
The pipeline should evolve the simulations with minimal human inputs, while providing useful analysis/diagnostic metrics and visualization products.


[//]: # (Work, methods, describe plan and rationale, concisely)
### Approach 

We employ a few tricks to follow the evolution of stars across large spatial and temporal scales.

logarithmic scale radial widths
GPU offloading of eos
adaptively remove blocks from memory



[//]: # (Results, achievement, deliverables, outcomes with merits. Insights, recommendations and opportunities.)
**What we found:**

[//]: # (Reflection, what next time, what you learn, mistakes and how to avoid.)
**What's next?** 
