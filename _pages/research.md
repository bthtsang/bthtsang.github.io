---
permalink: /research/
title: "Research"
author_profile: true
---

## Please find my full publication list at [NASA ADS](https://ui.adsabs.harvard.edu/user/libraries/tbxiKajfTsSjDC7Ir7sZxA) and [Google Scholar](https://scholar.google.com/citations?user=nGVc2BAAAAAJ&hl=en).

## Research Interests 
My research includes a broad range of topics in stellar astrophysics. They can be roughly grouped into three subjects:
- Modeling the effects of radiation-matter coupling in super-Eddington systems;
- Predicting the observational signatures using radiation transfer techniques;
- Developing and applying deep learning models to analyze astronomical data. 
Using analytical and numerical methods, I focus primarily on the study of how radiation impacts the lives and deaths of massive stars. I strive to understand the physical mechanisms governing the dynamics of radiation-dominated stellar systems and to provide insights on how to interpret their observations. My research projects also necessitate continuous improvements of the numerical methods in radiation transport and hydrodynamics, which I also devote a portion of my time on.
In the following, I will briefly summarize a few past and ongoing projects. 


## Lives of Massive Stars

### Simulating Massive Star Cluster Formation
![R136 Star Cluster in the LMC](/files/R136.jpg) 
*This is my favorite image taken by the Hubble Space Telescope, showing the massive star cluster R136 in the Large Magellanic Cloud. (Source: NASA/ESA)*

**Why they matter:**
Massive star clusters hold the keys to many intriguing open questions in astronomy. Their birthplaces are believed to be the most active star formation regions in the history of the universe. Massive clusters that formed at high redshifts may survive to be the globular clusters we see today. The intense stellar radiation fields and supernova explosions from the massive stars can impact galaxy evolution. The close proximity of stars in the cluster cores is conducive to forming compact object mergers that could give rise to gravitational wave signals.  

### Simulating Mass Loss from Massive Star Envelopes

### Simulating Strong Radiation-Matter Coupling
![FLASH Levitation Test](/files/FLASH-Levitation.png)
*A simulation of radiation pressure-driven wind showing the intricate coupling of radiation and gas (Tsang & Milosavljevic 2015)*

**Why it matters:**
During the formation and the explosive deaths of massive stars, the strong coupling between radiation and gas can significantly affect the dynamics and the observable signatures of the systems. Most of these interactions cannot be directly observed. Therefore, accurately modeling them can help us to develop an understanding of the key physics that controls the systems.

## Radiation transport in transient systems
### Simulating Core-Collapse Supernova Light Curves


## Machine Learning Applications in Astronomy
### Variable Star Light Curve Classification
![RNN-GMM Network Schematics](/files/RNN-GMM-schematics.png)
*Schematic diagram of the neural network architecture for variable star light curve classification and novelty detection (Tsang & Schultz 2019).*

In face of the rapidly growing volume of time-domain astronomical data (think [Rubin Observatory](https://www.lsst.org/) and [Zwicky Transient Facility (ZTF)](https://www.ztf.caltech.edu/)), I am actively exploring the applications of artificial neural networks in automating our analysis pipelines. 

**Why it matters**
With the advent of the next-generation surveys such as the Rubin Observatory, automatic pipelines capable of processing an unprecedented amount of time-domain astronomical data are required. To put it in perspective, these surveys will generate light curves from billion of stars; manual processing of such vast amount of data is simply impractical. In recent years we have also witnessed the rapid development of artificial neural networks in science and engineering. Being able to leverage the active development will position us to fulfill the inevitable analysis demands.  

### Improving Performance with Data Augmentation

### 

<!--https://github.com/bthtsang/DeepClassifierNoveltyDetection -->

### Software Instruments
Here's a list of software instruments I use in my research. 
- [FLASH](http://flash.uchicago.edu/site/): multi-physics, magneto-hydrodynamics code
- [Sedona](https://ui.adsabs.harvard.edu/abs/2006ApJ...651..366K/abstract): Monte Carlo radiation transport code for supernovae and other transients
- [Arepo](https://arepo-code.org/about-arepo): moving-mesh magneto-hydrodynamics code
- [STELLA](http://www.ascl.net/1108.013): a 1D multi-group radiation hydrodynamics code
- [Tensorflow](https://www.tensorflow.org/): a general purpose machine learning development platform
