---
permalink: /starsend2end/
title: "An End-to-end Software Pipeline to Simulate Exploding Stars"
author_profile: false
---

![Predicted vs True Eexp](/files/vr_dens_iter.gif)
Volume rendering of an exploding star. Color and opacity show the gas density around the stellar core from high (red/opaque) to low (blue/transparent).

[//]: # (Context, role, goal)

### Context

When massive stars approach the end of their lives, they explode violently as supernovae.
These cosmic explosions are the results of many inter-dependent physical processes: nuclear burning and neutrino transport at the stellar cores, convective and supersonic gas flows, all in the presence of strong gravity and turbulence.

In order to realize these explosions in simulations, scientists rely on a handful of physics solvers, each responsible for a subset of physics most relevant to a given stage.
However, there is no existing end-to-end pipeline for the process. Scientists have to manually traverse the software stack; each layer of the stack often requires days to learn, and a PhD to master. 


### Objective

Combine experience with other researchers, to assemble an end-to-end simulation pipeline to follow stellar explosions across different scales.


### Approach 
[//]: # (Work, methods, describe plan and rationale, concisely)

logarithmic scale radial widths
GPU offloading of eos
adaptively remove blocks from memory



[//]: # (Results, achievement, deliverables, outcomes with merits. Insights, recommendations and opportunities.)
**What we found:**

[//]: # (Reflection, what next time, what you learn, mistakes and how to avoid.)
**What's next?** 
