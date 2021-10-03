---
permalink: /rsg-outburst/
title: "Simulating RSG Pre-supernova Outbursts"
author_profile: true
---
**Plans**
- Set up a general framework to study the radiation hydrodynamical response of stellar envelopes to sudden energy deposition.
- Focus on the regime where the heating timescale (< 1 year) is shorter than the dynamical time.
- Compare the amount of mass loss, the density structure of the ejected layer, and the resultant stellar structure for energy deposited in different spatial geometries. Studies on the multi-dimensional nature of the problem are lacking in the literature.
- Investigate the role of proper radiation transport in the outermost (more inhomogeneous) layer.

**Simulation Procedure**
1. 1D MESA density and temperature profiles of a RSG were taken from Jared Goldberg's massive star model suites. 
2. The MESA profiles outside the helium core were mapped onto FLASH's 3D spherical polar grid. Numerically, adaptive mesh refinement (AMR) was in use. The gravity of the helium core was replaced by a point mass; the self-gravity of the hydrogen envelopes was included using the spherically symmetric mass interior to a given radius. 
3. Helmholtz equation of state (EOS) was adopted in FLASH, essentially treating thermodynamics the same way as MESA. Helmholtz EOS includes radiation pressure in the diffusion limit, and it assumes nuclei are fully ionized. Radiation transport was not included yet.
4. After the MESA-to-FLASH mapping, the stellar model was allowed to adjust to a new quasi-steady state for a few dynamical times.
5. Thermal energy was then deposited onto the hydrogen envelope. We tested two deposition geometries: spherical symmetric shell and a spherical segment. 

**Preliminary Results:**

To make sure the FLASH model can capture a realistic RSG envelope, we let the model "rest" for a few dynamical times.
<iframe src="https://player.vimeo.com/video/621738870" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>


**What's next?** 
In astronomy, observation is fundamentally limited to a single view (the view from Earth). In practice, it will be valuable to reconstruct the 3D scenes around different astronomical objects using a single input view. Ongoing work focuses on optimizing NeRF architectures with one-shot/few-shot image encoding (e.g., [PixelNeRF](https://github.com/sxyu/pixel-nerf)).
