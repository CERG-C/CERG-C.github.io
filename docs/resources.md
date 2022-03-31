# Awesome Volcano Resources 🌋

<p align="center">
    <em>A curated list of resources for volcanology.</em>
</p>
<p align="center">
<a href="https://github.com/sindresorhus/awesome" target="_blank">
    <img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" alt="Awesome">
</a>
</p>

--- 

This list curates a collection of useful resources in volcanology.

---

## Computer codes 

### Hazard assessment

#### Tephra dispersal and fallout

- [Tephra2](https://github.com/geoscience-community-codes/tephra2): 2D model for ground tephra accumulation written in C with some [additional functions](https://github.com/e5k/Tephra2Utils) in Matlab ([reference](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2003JB002896)).
- [TephraProb](https://github.com/e5k/TephraProb): Probabilistic hazard assessment for tephra fallout written in Matlab ([reference](https://appliedvolc.biomedcentral.com/articles/10.1186/s13617-016-0050-5)).
- [Fall3d](https://gitlab.com/fall3d-distribution): 3D atmospheric tephra dispersal ([reference](https://gmd.copernicus.org/articles/13/1431/2020/)).
- [LagTrack](https://github.com/e5k/LagTrack): Particle tracking tool written in Matlab ([reference](https://www.sciencedirect.com/science/article/abs/pii/S0012821X21002399)).
- [GBF](https://github.com/unigeSPC/gbf): Probabilistic hazard assessment for ballistic impacts written in Matlab ([post processing](https://github.com/e5k/GBF-Post-Processing)) ([reference](https://www.sciencedirect.com/science/article/pii/S0377027316301317)).

#### Lava flow inundation 

- [Molasses](https://github.com/geoscience-community-codes/MOLASSES): Lava flow inundation model written in C ([reference](https://link.springer.com/article/10.1186/2191-5040-1-3)).
- [Q-LavHA](https://we.vub.ac.be/en/q-lavha): Probabilistic hazard assessment for lava inundation in QGis ([reference](https://www.sciencedirect.com/science/article/pii/S0098300416303715)).
- [MrLavaLoba](https://github.com/demichie/MrLavaLoba): Stochastic model for stochastic for pahōehoe lava flow inundation written in Python ([reference](https://www.sciencedirect.com/science/article/abs/pii/S0377027317303876)).
- [PyFlowGo](https://github.com/pyflowgo/pyflowgo): Python version of FLOWGO for lava flow inundation ([reference](https://www.sciencedirect.com/science/article/pii/S0098300417306738)).
  
#### Lahars & PDCs inundation

- [ECMapProb](https://github.com/AlvaroAravena/ECMapProb): Probability maps of PDC inundation using a modified energy cone model approach ([reference](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2019JB019271)).
- [LaharFlow](https://www.laharflow.bristol.ac.uk): Model of lahar dynamics on evolving topography. Only as a web interface.
- [LaharZ](https://pubs.usgs.gov/of/2014/1073/): Statistical model to estimate lahar inundation. Requires ArcGIS ([reference](https://pubs.usgs.gov/of/2014/1073/pdf/ofr2014-1073.pdf))

### Eruption history & analogues

- [PyVOLCANS](https://github.com/BritishGeologicalSurvey/pyvolcans) Python library to explore similarity between volcanic systems ([reference](https://link.springer.com/article/10.1007/s00445-019-1336-3)).

### Exposure & impact assessment 

- [VolcGIS](https://github.com/vharg/VolcGIS): Python framework for exposure analyses (reference).

### Deposit characterisation

- [Tephra2 inversion](https://github.com/geoscience-community-codes/tephra2-inversion): Tephra2 inversion method written in C with some [post-processing tools](https://github.com/e5k/Tephra2Utils) in Matlab ([reference](https://pubs.geoscienceworld.org/gsl/books/book/1732/chapter/107601115/Inversion-is-the-key-to-dispersionunderstanding)).
- [CareySparks86_Matlab](https://github.com/e5k/CareySparks86_Matlab) Matlab implementation of the Carey and Sparks (1986) model to estimate plume height from isopleth data ([reference](https://link.springer.com/article/10.1007/BF01046546)).
- [TephraFits](https://github.com/e5k/TephraFits): Matlab function to estimate the volume of and characterise tephra deposits from field-based methods ([reference](https://link.springer.com/article/10.1186/s13617-018-0081-1)).
- [TOTGS](https://github.com/e5k/TOTGS): Calculation of the total grain-size distribution of tephra deposits using the VORONOI method in Matlab ([reference](https://link.springer.com/article/10.1007/s00445-004-0386-2)).
- [AshCalc](https://github.com/MatthewDaggitt/AshCalc): Calculation of the volume of tephra deposits in Python ([reference](https://appliedvolc.biomedcentral.com/articles/10.1186/2191-5040-3-7)).


### Miscellaneous tools

- [CDSAPItools](https://github.com/e5k/CDSAPItools): Python functions to download wind and atmospheric data from ERA5 formatted to work with different models (e.g., [TephraProb](https://github.com/e5k/TephraProb), [Fall3d](https://gitlab.com/fall3d-distribution))
- [TopoToolbox](https://github.com/wschwanghart/topotoolbox): Matlab library for terrain analyses ([reference](https://esurf.copernicus.org/articles/2/1/2014/)).

## Databases