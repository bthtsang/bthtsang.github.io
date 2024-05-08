---
permalink: /rsg-outbursts/
title: "Simulating RSG Pre-supernova Outbursts"
author_profile: false
---

{% include video id="Y6OD6_Ck6T0" provider="youtube" %}
<iframe src="https://www.youtube.com/shorts/Y6OD6_Ck6T0" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

## Context

Months to years before massive stars explode as supernovae, most of them exhibit elevated levels of surface activities.
In other words, there are usually powerful mass and energy outbursts from the surface of the stars -- think solar flares, but more than a million times brighter.
The precise nature of these outbursts is still unknown. There are signs from observations that these outbursts are highly aspherical. 
However, most computer simulations of these outbursts were limited only to 1D, leaving the 3D structure of these pre-supernova stars essentially unexplored. 

## Objective

To systematically simulate these outbursts, we set up a generic hydrodynamical framework to examine the reactions of stars to a sudden deposition of energy. We focus on the regime where the energy deposition is explosive - large amount of energy deposited quickly. 
We would like to compare the amount of mass loss, the density structure of the ejected mass, and the resultant stellar structure. 
We would also like to release the simulation framework so that other researchers can perform their own experiments.


## Approach

The simulations were performed in two stages. 
First, the structure (e.g., density, temperature, etc) of a star was mapped onto a 3D spherical voxel grid. 
Adaptive mesh refinement (AMR) was used to allocate voxel grids to regions of the star where sharp changes in density were located. 
The star was allowed to *relax* into a quasi-equilibrium state. Convection of gas is prevalent in this stage, as can be seen in the video above (the time stamp depicts *time until energy injection*).

In the second stage, bursts of thermal energy were injected deep in the star. 
We then sat back and observed what happened to the star.


## Results:

<iframe src="https://www.youtube.com/shorts/Xn_Zpxs8oHY" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The reaction of the star following the energy injection can be seen in the video above.
The "thermal bomb" placed in the star launched the top layer of the star upward. 
Soon, turbulent features (known as Rayleigh-Taylor instabilities) developed in the injection zone,
which allowed the underlying hot gas to carve out channels of material outbursts.
An inflated, still turbulent, stellar surface remained.

As a control experiment, we repeated the energy injection simulation but replaced the star with one *without* convection. 
The model was then effectively "1D", mimicking the 1D setup most prior work were based on.

<iframe src="https://www.youtube.com/shorts/PY66jUi5Xiw" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

Similar to the above convective case, turbulent instabilities readily developed in the energy injection zone. 
However, without the convective motions seeding the formation of "outburst channels", 
the top of the star inflated and expanded as a whole, and eventually settled back down without much mass loss.  

The simulations above revealed a geometric effect that has never been observed nor studied before.
Overall, the amount of mass loss and the spatial structure of the ejected mass can be significantly impacted when the 3D effects of convection are considered. 

## What's next? 

There are many natural next steps for this projects. 
We can employ path tracing techniques to predict the brightness variations of the star before, during, and after energy deposition and compare them to observations. 
Using a suite of simulations, one can also systematically quantify the relations between different modes/strengths of energy deposition, the resultant mass loss, and the post-outburst stellar structures.
