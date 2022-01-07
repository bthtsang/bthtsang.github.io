---
permalink: /rsg-outbursts/
title: "Simulating RSG Pre-supernova Outbursts"
author_profile: false
---

## Plans
- Set up a general framework to study the radiation hydrodynamical response of stellar envelopes to sudden energy deposition.
- Focus on the regime where the heating timescale (< 1 year) is shorter than the dynamical time.
- Compare the amount of mass loss, the density structure of the ejected layer, and the resultant stellar structure for energy deposited in different spatial geometries. Studies on the multi-dimensional nature of the problem are lacking in the literature.
- Investigate the role of proper radiation transport in the outermost (more inhomogeneous) layer.

## Simulation Procedure
1. 1D MESA density and temperature profiles of a 15 Msun RSG were taken from Jared Goldberg's massive star model suites. 
2. The MESA profiles outside the helium core were mapped onto FLASH's 3D spherical polar grid. Numerically, adaptive mesh refinement (AMR) was in use. The gravity of the helium core was replaced by a point mass; the self-gravity of the hydrogen envelopes was included using the spherically symmetric mass interior to a given radius. 
3. Helmholtz equation of state (EOS) was adopted in FLASH, essentially treating thermodynamics the same way as MESA. Helmholtz EOS includes radiation pressure in the diffusion limit, and it assumes nuclei are fully ionized. Radiation transport was not included yet.
4. After the MESA-to-FLASH mapping, the stellar model was allowed to adjust to a new quasi-steady state for a few dynamical times.
5. Thermal energy was then deposited onto the hydrogen envelope. We tested two deposition geometries: in a spherical symmetric shell and a spherical segment. 

## Preliminary Results:

To make sure the FLASH model can capture a realistic RSG envelope, we let the model "rest" for a few dynamical times. Below I am showing the density slice (along a constant phi) of the 3D simulation. In the setup \theta spans \pi/4 to 3\pi/4, while \phi is from 0 to \pi.

<iframe src="https://player.vimeo.com/video/621738870" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

After about 1.7 years, convection started to develop (seeded numerically) and the envelope settled into a rather dynamically stable state. This model was just for sanity check, to make sure the MESA-to-FLASH mapping was OK.

Next, expecting substantial mass loss, we mapped the same model onto a domain 2x in radial extent (note that radius now extends to 2000 Rsun). Again we allowed the model to settle into a quasi-steady state before depositing 2.5 \times 10^{47} erg over 116 days (10^7 s) at 430 +/- 10 Rsun. The amount of energy was chosen to be around the binding energy of the layer above the deposition radius. The deposition radius of 430 Rsun and the shell thickness were inspired by the 15 Msun RSG model in [Leung & Fuller (2020)](https://ui.adsabs.harvard.edu/abs/2020ApJ...900...99L/abstract). 

<iframe src="https://player.vimeo.com/video/621739937" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The behaviors of the model up to 6.3 years were basically the same as above. At year 6.3, thermal energy was deposited uniformly over a spherically symmetric shell at 430 Rsun. The top layer was launched upward, Rayleigh-Taylor instabilities were observed shortly after, and the majority of the layer was ejected.

To examine what a non-spherically symmetric mode of energy deposition would do, we deposited the **same amount of energy at the same radius**, but this time restricted only to a spherical segment of theta/phi = 90 +/- 15 deg. 

<iframe src="https://player.vimeo.com/video/621740268" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The first 6.3 years were identical to the spherical symmetric case. However, the subsequent behaviors after energy deposition were quite different. The top layer expanded outward with some degree of RT instability development. The sideways expansion of the "bubble" induced shocks in the remaining stellar materials, and the amount of mass loss was only about 1/3 of the spherical shell case. It seems to suggest that dimensionality matters to the outcome. 

## What's next? 
- Examine and quantify the relation between different modes/strengths of energy deposition and mass loss.
- Analyze the density distributions of the outer/ejected layers, infer potential observational consequences.
- Contrast with models in 1D or 2D.
- Include proper radiation transport.
