# Q-LavHA

With the knowledge gained on [topographic controls](Hazard_lava_steepest-descent.md) and [modeling](Hazard_lava_modeling.md) gained from the previous exercise, we will now look at `Q-LavHA`[^1] as an alternative approach for probabilistic hazard assessments for lava flow inundation. This part of the exercise assumes that you have already [installed](Hazard_lava_config.md) both `QGIS` and `Q-LavHA`. The [Q-LavHA user manual](../files/Usersguide_Q-LavHA_V3_2020.pdf) contains some important information about how to configure the model and the data, so we encourage you to have a look at it at some point. 

## Theory behind Q-LavHA 

The starting philosophy behind `Q-LavHA` is similar to the analysis performed for the [path of steepest descent](Hazard_lava_steepest-descent.md#flow-accumulation) approach: the DEM, the model will try to estimate *where* the flow will go next based on the maximum $\Delta h$ of the surrounding pixels. However, `Q-LavHA` uses a probabilistic approach to estimate this flow direction. 

Firstly, as we saw, a lava flow is a viscous fluid with yield strength, which means that it can *escape* the steepest path and propagate laterally, fill depressions and overcome topographical obstacles. To account for that, `Q-LavHA` introduces 2 corrective factors:

- $H_c$, representing the flow thickness.
- $H_p$, representing the ability of a flow to *inflate*. 

Together, these two parameters will avoid the modelled flow getting stuck in topographic low and will allow it to spread laterally, as we saw the 2021 flow of La Palma was able to do. 

Secondly, the initial estimation of path of steepest descent is performed *stochastically*

1. `Q-LavHA` flow doe

Corrective factors are included enabling the lava to overcome small topographical obstacles or pits (Fig. 2). The factor Hc (m) is always added to the elevation of the central pixel before calculating h ∆ i (Eqs. 2 and 3). This enables to represent the lava thickness (Felpeto et al., 2001). As it is observed that real lava flows are capable of flooding preexisting depressions (Sigurdsson et al., 2015) whereas lava flow lines would be trapped numerically into the topographic depression, we propose the introduction of a higher corrective factor, Hp (m), which can be applied if the source pixel is surrounded by eight pixels at a higher elevation pixels which Hc cannot overcome (Fig. 2).



## References

[^1]: Mossoux, S., Saey, M., Bartolini, S., Poppe, S., Canters, F., Kervyn, M., 2016. Q-LAVHA: A flexible GIS plugin to simulate lava flows. Computers & Geosciences 97, 98–109. https://doi.org/10.1016/j.cageo.2016.09.003