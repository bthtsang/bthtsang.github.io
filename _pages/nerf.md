---
permalink: /nerf/
title: "Exploring Neural Radiance Fields (NeRFs)"
author_profile: false
---

## Context

Given a number of images of an object with known camera positions and angles, the goal of novel view synthesis is to render the scene from unobserved viewpoints. Realistic and efficient rendering of 3D scenes is essential for real-time and interactive data visualization and exploration.
[Neural Radiance Field (NeRF)](https://arxiv.org/abs/2003.08934) is a new class of deep learning framework for novel view synthesis that has demonstrated faithful rendering of complex scene with economical network sizes. In astrophysics, detailed 3D simulations are often too cumbersome for real-time data visualization. However, interactive visualization is often necessary to derive physical understanding. With the rapid development in NeRF architectures, it seems timely to explore their applications in scientific visualization.


## Approach 

We trained the baseline NeRF network ([official implementation](https://www.matthewtancik.com/nerf)) using volume rendering images of a 3D simulation of turbulent interstellar gas (backdrop to form stars). Our goal was to examine whether NeRF is applicable to render scientific simulations. We used 100 input images/camera poses for training, and for testing we render the "learned simulation" with a camera fly-around.

## Results

<iframe src="https://player.vimeo.com/video/587604817?h=2db627bf89" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The video above shows the output view. High-density gas is represented by red, low-density gas is represented by blue; intermediate values of density are in yellow/green. The NeRF-generated view shows promising performance - it accurately retains the **complex filamentary structures of the turbulent gas** while maintaining a realistic 3D sense of the simulation.


## What's next?

In astronomy, observation is fundamentally limited to a single view (the view from Earth). In practice, it will be valuable to reconstruct the 3D scenes around different astronomical objects using a single input view.
The baseline NeRF is known to be rather slow to train. Since its introduction in 2020, there has been a explosion of NeRF-inspired network architectures.
Neural representation of volumetric data is a particularly promising direction to explore for improving the analysis and visualization workflows in science.
