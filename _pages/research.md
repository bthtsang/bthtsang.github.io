---
permalink: /research/
title: "Research"
author_profile: true
---

## Please find my full publication list at [NASA ADS](https://ui.adsabs.harvard.edu/user/libraries/tbxiKajfTsSjDC7Ir7sZxA), [Google Scholar](https://scholar.google.com/citations?user=nGVc2BAAAAAJ&hl=en), and [ORCID](http://orcid.org/0000-0002-6543-2993).

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

**Why this matters:**
Massive star clusters hold the keys to many intriguing open questions in astronomy. Their birthplaces are believed to be the most active star formation regions in the history of the universe. Massive clusters that formed at high redshifts may survive to be the globular clusters we see today. The intense stellar radiation fields and supernova (SN) explosions from the massive stars can impact galaxy evolution. The close proximity of stars in the cluster cores is conducive to forming compact object mergers that could give rise to gravitational wave signals.  

**How we modeled this:**
The formation of massive star clusters presents a battle between two strong forces: gravity wants to bring gas toward the center, into the abyss of the gravitational potential; stellar feedback, such as radiation pressure, exerts an outward pressure to oppose the pull of gravity. The outcome of this battle is far from trivial because of the turbulent distributions of gas. In [Tsang & Milosavljevic (2018)](https://ui.adsabs.harvard.edu/abs/2018MNRAS.478.4142T/abstract), we directly modeled the gravitational collapse of turbulent giant molecular clouds and the associated radiation pressure feedback from the newly formed stars in 3D. 

**What we found:**
Contrary to the conclusions from previous 1D studies that assumed spherical symmetry, radiation pressure is inefficient in halting the gas infall due to a density-radiative flux anti-correlation. Essentially, radiation tends to choose the paths of least resistance and leaks through low-density channels. Such inefficiency in radiative forcing allows gas accretion to proceed, leading to high star formation efficiency. 
![Volume Rendering of Turbulent Cluster-forming Clouds](/files/VR_SSC.png) 
*Volume rendering of the turbulent gas distributions around a forming massive star cluster core. The red-to-violet spectrum denotes high-to-low gas density. (First place in the [Visualizing Science contest in 2017](https://cns.utexas.edu/news/visualizing-science-2017))*

### Simulating Mass Loss from Massive Star Envelopes

![IIn Ibn Schematic](/files/Smith_CSM_IIn_Ibn.png)
*Schematic diagram of CSM interacting supernovae. The four numbered regions represent: (1) the pre-shock CSM, (2) the shocked CSM, (3) the shocked SN ejecta, and (4) the freely expanding SN ejecta. Understanding how the materials in region (1) got there is essential to the proper interpretations of many supernova signatures (Source: [Smith 2008](https://doi.org/10.1007/978-3-319-21846-5_38))*

**Why this matters:**
Super-Eddington energy generation and deposition in the envelopes of massive stars are common and can lead to significant mass loss. Strong stellar winds from massive stars are an important feedback mechanism that regulates star formation and circulates metals and dust grain back into the interstellar medium. In addition, substantial mass ejection from the massive star's envelope can set up a dense circumstellar medium (CSM) surrounding the star. Later on, when the massive star undergoes core collapse, the interaction between the SN shock and the slow-moving CSM can imprint the observed spectra with narrow emission lines, the so-called Type IIn SNe ('n' for 'narrow' line). Understanding how the CSM is created can help interpret a family of similar interaction-powered SN events.

The overall stability of massive star envelopes also has implications on how realistic very massive stars (VMSs) and super-massive stars (SMSs) are. VMSs and SMSs are unusually massive stars (VMSs: 100-1000 Msun; SMSs: 10000 - 100000 Msun) theorized to be the intermediate objects that give rise to supermassive black holes (SMBHs). By examining the stability of their stellar envelopes and the extent of mass loss, we can better constrain the viability of different SMBH formation channels.

**How we model this:**
(Ongoing work)
By performing radiation transport analyses on 3D massive star envelope models, we are working to examine the roles of radiative forcing due to spectral lines. 
We are also using radiation hydrodynamical simulations to explore how super-Eddington energy deposition near stellar surfaces can induce mass loss prior to SN explosions. 

<!--
episodic nuclear shell burning 
energy deposition by internal gravity waves
binary interaction
-->

### Simulating Strong, Radiation-Driven Winds
![FLASH Levitation Test](/files/FLASH-Levitation.png)
*A simulation of radiation pressure-driven wind showing the intricate coupling of radiation and gas in a super-Eddington environment ([Tsang & Milosavljevic 2015](https://ui.adsabs.harvard.edu/abs/2015MNRAS.453.1108T/abstract))*

**Why this matters:**
Radiation pressure from young massive stars can be an important force that drives turbulence and winds in active star-forming regions. The strength of the radiation force affects the star formation rates in the molecular clouds, which in turn could impact the evolution of the host galaxies via subsequent stellar feedback. 
However, it is unclear how efficiently radiation couples with gas in the turbulent star-forming environments where sharp transitions in optical depths are commonplace.
Most of these interactions are not directly observable. Therefore, accurately modeling them can help us develop an understanding of the key physics at play.

**How we modeled this:**
We developed a Monte Carlo radiation transport module in the hydrodynamics code FLASH, and applied it to a 2D setup where an intense radiation field was set to launch a super-Eddington wind against gravity. Due to its profound implications, this setup has become a standard test problem for radiation hydrodynamics methods.

**What we found:** 
We discovered qualitatively different gas dynamics from previous studies that were based on lower-accuracy radiation transport schemes (e.g., flux-limited diffusion (FLD), first-moment (M1) closure). 
With our Monte Carlo scheme with superior accuracy, the gas layer received significant forcing and was launched into strong winds; whereas in lower-order methods the gas layer settled into a quasi-steady state without significant radiative acceleration. This work highlights the importance of accurate numerical treatment for radiation in super-Eddington environments.



## Radiation transport modeling of transient systems
### Simulating Core-Collapse Supernova Light Curves
**Why this matters:**
Most massive stars with mass above 8 solar masses end their lives in energetic core-collapse supernova (CCSN) explosions. A key challenge for astronomers is to reconcile the large variety of observed SN events with the properties of the massive star progenitors and their explosions. In order to achieve physical understanding of the full SN population, it is crucial to be able to reliably constrain progenitor and explosion properties from observations. 


![II-P Light Curve Comparison](/files/IIP_LCs.png) 
*Comparisons of Type II-P supernova light curves generated by two fundamentally different radiation transport schemes. The close matches between the two attest to the fidelity of our radiation transport modeling approaches.*

**How we modeled this:**
We focused on the modeling of Type II-Plateau SNe and the most readily available data product - their light curves.
We modeled a suite of red supergiants and their explosions using the MESA stellar evolution code. We mapped the models at the moment of shock breakout to two very different radiation transport code: the moment-based code STELLA, and the Monte Carlo-based code Sedona. We compared the output light curves and the time-dependent ejecta structures.

**What we found:**
Recent studies have shown that there is a high degree of degeneracy between light curve features and progenitor properties (mass, radius, explosion energy, etc). We confirmed such degeneracy and found that the light curves produced from the two codes agreed to about 5 - 10%. This remarkable agreement offers confidence in our radiation transport modeling pipelines.  

## Machine Learning Applications in Astronomy
### Variable Star Light Curve Classification
![RNN-GMM Network Schematics](/files/RNN-GMM-schematics.png)
*Schematic diagram of the neural network architecture for variable star light curve classification and novelty detection (Tsang & Schultz 2019).*


**Why it matters**
In face of the rapidly growing volume of time-domain astronomical data (think [Rubin Observatory](https://www.lsst.org/) and [Zwicky Transient Facility (ZTF)](https://www.ztf.caltech.edu/)), automatic pipelines capable of processing an unprecedented amount of time-domain astronomical data are required. To put it in perspective, these surveys will generate light curves from billion of stars; manual processing of such vast amount of data is simply impractical. In recent years we have also witnessed the rapid development of artificial neural networks in science and engineering. I see a clear opportunity in leveraging the current active development to prepare for the inevitable analysis demands in astronomy.  

**How is our neural network set up:**
We combined a recurrent neural network auto-encoder for unsupervised feature extraction with an estimation network for supervised classification and novelty detection. We drew inspiration from two recent works on [unevenly-sampled light curve classification](https://ui.adsabs.harvard.edu/abs/2018NatAs...2..151N/abstract) and [anomaly detection in commercial laboratories](https://openreview.net/forum?id=BJJLHbb0-).
The novelty detection functionality was based on a Gaussian Mixture Model (GMM) implemented in the estimation network.

**What we found:**
Our network attained a classification accuracy of about 99%, which is on par with the conventional workhorse of random forest (RF) classifier. The network was also capable of detecting previously unseen types of variability with precision 0.89, recall 0.82, and an F1 score of 0.85. In addition, our network has 10 to 100 times fewer trainable parameters than the RF approach. We found that simultaneous training of the auto-encoder with the estimation network was mutually beneficial, resulting in faster learning of the auto-encoder and higher classification/novelty detection performance of the estimation network.

<!--
### Improving Performance with Data Augmentation

### Learning astro-statistics from turbulence simulations
-->
<!--https://github.com/bthtsang/DeepClassifierNoveltyDetection -->

## Software Instruments
Here's a list of software instruments I use in my research. 
- [FLASH](http://flash.uchicago.edu/site/): multi-physics, magneto-hydrodynamics code
- [Sedona](https://ui.adsabs.harvard.edu/abs/2006ApJ...651..366K/abstract): Monte Carlo radiation transport code for supernovae and other transients
- [Arepo](https://arepo-code.org/about-arepo): moving-mesh magneto-hydrodynamics code
- [STELLA](http://www.ascl.net/1108.013): a 1D multi-group radiation hydrodynamics code
- [Tensorflow](https://www.tensorflow.org/): a general purpose machine learning development platform
