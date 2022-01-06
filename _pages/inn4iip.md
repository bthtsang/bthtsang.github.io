---
permalink: /inn4iip/
title: "Supernova Progenitor Parameter Estimation with Invertible Neural Networks (INNs)"
author_profile: true
---
This is a small (but still interesting) side project I did with INNs. The code I wrote for this project can be found on [my GitHub page](https://github.com/bthtsang/FrEIA/blob/master/inn4iip.py)

**Why this matters:**
Type II supernovae are the violent explosive deaths of massive stars (stars with masses larger than about 8 times of the Sun).
Astronomers observe and study their light curves (brightness variation in time) in order to deduce the properties of the underlying exploding stars (so-called supernova progenitors). Knowing the demographics of massive stars can help us better understand how massive stars live and die, how they impact their host galaxies, and how best we should design our future observatories. 
As in many applications in science, the *forward problem* of determining measurements given sets of physical parameters is easy. In our case for supernovae, we can perform numerical simulations. 
However, the *inverse problem*, that is, inferring the physical parameters given observations is ambiguous. Many sets of parameters can give rise to very similar observables -- model degeneracy. For example, in supernova modeling, stars with very different masses and sizes can produce essentially the same light curves. 
To date, most supernova progenitor parameters are still determined based on visual comparison with incomplete sets of light curve library. 
To fully characterize the model degeneracy, the posterior parameter distribution conditioned on the observed light curve is required.
INN is a recent deep learning architecture designed for reliable posterior estimation. 
With the imminent deployment of new observatories (e.g. [the Vera Rubin Observatory](https://www.lsst.org/), [James Webb Space Telescope](https://www.jwst.nasa.gov/)), it is timely to explore its applications in real-world scientific settings.


**How I approached this:**
I built an INN for the supernova application using the [Framework for Easily Invertible Architecture (FrEIA)](https://github.com/VLL-HD/FrEIA), a pytorch-based library. 
The exact INN architecture was rather basic, with three affine coupling blocks of *GLOW* type interlaced with random permutation layers. The sub-networks in the affine coupling layers are simple fully-connected networks with 3 layers of width 64.
The supernova model dataset was taken from my [previous published work](https://arxiv.org/abs/2006.01832). Altogether, there are 421 parameters-light curve pairs. Given the relatively small size of the dataset, the size of the INN was also limited (only about 101,000 trainable parameters).
My goal is to examine whether such a basic INN is applicable to the supernova inference problem. A total of 337 samples were used in training, while 84 were held out for testing.


**What I found:**
Show parameter plots with diagonal lines
Show example parameter for some objects


<iframe src="https://player.vimeo.com/video/587604817?h=2db627bf89" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The video above shows the output view. High-density gas is represented by red, low-density gas is represented by blue; intermediate values of density are in yellow/green. The NeRF-generated view shows promising performance - **it accurately retains the complex filamentary structures of the turbulent gas while maintaining a realistic 3D sense of the simulation.**


**What's next?** 
In astronomy, observation is fundamentally limited to a single view (the view from Earth). In practice, it will be valuable to reconstruct the 3D scenes around different astronomical objects using a single input view. Ongoing work focuses on optimizing NeRF architectures with one-shot/few-shot image encoding (e.g., [PixelNeRF](https://github.com/sxyu/pixel-nerf)).
