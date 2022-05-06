# Modelling lava flows

As we saw from the previous exercise, lava flows are slightly more complex than water, and the hydrological modelling approach fails to describe some important hazard metrics required for both short- and long-term risk assessments. Assessing the **timing** of lava inundation is still an active topic of research, so we will restrict ourselves to estimating the **surface area** of flows. For this, we first need to review some of the **physical** concepts behind the fluid dynamics of lava flows.
   
<!-- - Option 1: Reaching a given distance 
  - Arbitrary
  - Calibrated
  - Probability distribution based on differences in elevation -->



## :material-format-list-checks:{ .icn } Objectives

- Understand basic rheological properties of lavas. 
- Review the main emplacement processes.
- Identify and appreciate the sources of uncertainties in lava flow modelling.

## :fontawesome-solid-gears:{ .icn } When and why do lavas flow?

!!! note "Credits"

    This section is largely inspired by the great rheology class of [Tom Shea](https://www.soest.hawaii.edu/gg/people/gg_profile_shea_t.html) at the University of Hawai'i.

### Some definitions

##### Shear stress 

The shear stress $\tau$ is the **load stress applied to a fluid** &rarr; i.e., the force per unit area acting in the direction and parallel to the flow surface:

$$
\tau = \rho g h \times sin(\alpha)\ [Pa = Nm^{-2}]
$$

##### Strain rate 

The strain rate $\epsilon$ is the **rate of deformation** when a shear stress is applied &rarr; i.e., velocity gradient:

$$
\epsilon = \frac{dV}{dZ}\ [s^{-1}]
$$

##### Yield strength

The yield strength $\tau _0$ is the **shear stress above which deformation begins**:

$$
\tau_0 = \rho g h_0 \times sin(\alpha)\ [Pa = Nm^{-2}]
$$

##### Viscosity

The viscosity $\eta$ is the **resistance of fluid** to flow when shear stress is applied:

$$
\eta = \frac{d\tau}{d\epsilon}\ [Pa\ s = Nm^{-2}s]
$$

### When does lava flow?

From Figure 1:

- &rarr; Flow occurs when **driving forces** (here = gravitational forces) > **resistive forces**
- &rarr; Response/behaviour of the fluid depends on its **rheology**

<figure markdown>
  ![rheology](img/lava/tom_rheology.png)
  <figcaption>Figure 1: Left: Summary of driving forces. Right: Types of fluids. Note that on the right plot, the slope of at each point of the curve represents the flow's viscosity. Credit: Tom Shae.</figcaption>
</figure>

### Flow rheology

#### Newtonian fluids

- Newtonian fluids will start to flow/deform when an infinitesimally low *shear stress* is applied
- The relationship between the applied force (&rarr;*shear stress*) and rate of deformation (&rarr;*strain rate*) is linear

#### Non-newtonian fluid 

A fluid is **non-newtonian** when one of these conditions is met:

1. The relationship between *shear stress* and *strain rate* is **non-linear**
2. A *yield strength* must be exceeded before flowing occurs, after which the *shear stress*/*strain rate* relationship can be linear or not

Amongst non-newtonian fluids:

- Fluids with variable *shear stress*/*strain rate* include **pseudoplastic** or **dilatant** fluids
    - Dilatant fluids: apparent *viscosity* increases with increasing *shear rate* &rarr; *shear thickening fluids*
    - Pseudoplastic fluids: apparent *viscosity* decreases with increasing *shear rate* &rarr; *shear thinning fluids*
- **Bingham** fluids are a special type of non-newtonian fluids characterized by a *yield strength* and a linear *shear stress*/*strain rate* relationship

!!! tip "Lava flows"

    Lava flows are typically **non-newtonian**, **pseudoplastic** fluids with a **yield strength**.

    Think of a slope. If you drop a newtonian fluid (i.e., no yield strength) on it, it will immediately start flowing, whereas non-newtonian fluids with a yield strength will require some help.

    Can you think of any fluids that would behave like these?

    ??? check "Solution"

        - **Water** is a newtonian fluid with no yield strength 
        - **Toothpaste** is a non-newtonian fluids with a yield strength

    What parameters can help lava flows to overcome yield strength?

    ??? check "Solution"

        - Effusion rate
        - Flow thickness
        - Slope

## :material-head-sync:{ .icn } Dynamics of lava flows

Let's try and put these physical concepts in the perspective of *actual* lava flows. Look at these videos, and describe them in terms of:

- Flow shape, geometry, morphology, texture
- Colour (as an indicator to which physical parameter?)
- Velocity and flow rate?


Flow type        | Video 1                                                 | Video 2
-----------------|---------------------------------------------------------|--------------------------------------------------------
**Lava channel** | [Video 1a](https://youtu.be/aJ66rTiHA4A?t=49;mute=1)    | [Video 1b](https://www.youtube.com/watch?v=BgjpSlzU9oU)
**Pāhoehoe**     | [Video 2a](https://www.youtube.com/watch?v=JoGFPabrdUI) | [Video 2b](https://www.youtube.com/watch?v=myxTc32foGs)
**'A'ā**         | [Video 3a](https://www.youtube.com/watch?v=Kc6CIwBVo5s) | [Video 3b](https://www.youtube.com/watch?v=9yhdBjGtxEM)



!!! question "Lava flows properties"

    What do you see? From the parameters described above, what can you infer on the underlying processes? 

    - How would you describe the advance rates of each lava flow type?
    - What distance from the vent is each flow? 
    - Where do you think the *local* effusion rate is the highest?




### Physical modelling as a hazard tool

These videos illustrate the **variety** and the **complexity** of processes controlling the spatio-temporal evolution of lava flows. Attempting to sum up *all* processes taking place in lava flow emplacement is difficult, but here are *some* of the *higher-level* parameters [^1][^2][^3][^4]:

- **Advance rate**:
    - Volumetric effusion rate 
    - Proximity to the vent
- **Flow length**:
    - Eruption rate (both magnitude and steadiness)
    - Slope traversed
    - Extent of topographic confinement
    - Initial lava temperature and rheological properties 
    - Emplacement conditions (open channel or insulating tube)

No model is yet able to capture the ensemble of these parameters, and therefore each model relies on different assumptions[^5]. For instance, the *FLOWGO* model[^6] describes the physics behind the down-flow evolution of thermal and rheological properties of lava flows, but assumes a **channel-contained** lava flow. Other models, such as *Q-LavHA*[^7] or *MrLavaLoba*[^8] bypass the use of physics and describe the emplacement of lava flows as **stochastic** processes. **Understanding both i) the issues behind the studied problem (e.g., process-driven research vs hazard assessment) and ii) the limitations behind numerical models is key to identify and adopt the appropriate modelling approach.**

!!! warning "Modeling natural phenomena"

    Don't forget the famous aphorism:

    > All models are wrong, but some are useful!

### The 2016 eruption of Pu‘u ‘Ō‘ō

As already discussed, the combination of all these parameters make **lava flow modeling** a complex problem associated with **large uncertainties**. One critical aspect of risk management is that these lava flow crises are often **long-lasting**, and predicting their spatio-temporal evolution is currently impossible beyond a time window of a few hours to days. This is especially true for **pāhoehoe flow fields**, where random processes are important [^1].

Let's use some [downward counterfactual thinking](https://www.frontiersin.org/articles/10.3389/feart.2019.00340/full) on the 2016 lava flow of Pu‘u ‘Ō‘ō in Hawai'i to appreciate the complexity of predicting the evolution of such an event. Fortunately, this event did not affect any settlements. Here is a summary of the chronology:

| Date       | Observation                                                |
|:-----------|:-----------------------------------------------------------|
| May 24     | Onset of summit eruption at Pu‘u ‘Ō‘ō                      |
| June 08    | Development of a compound lava flow going SE               |
| June 08-28 | Lava flow emplacement as pāhoehoe                          |
| June 28-30 | Lava reached the pali, transition to 'A'ā                  |
| June 30    | Onset of development of compound pāhoehoe on coastal plain |
| July 26    | Ocean entry, 11 km away from source                        |
| Until sept | Widening of the flow field                                 |

=== "Hawaii"

    <figure markdown>
    ![Hawaii](img/61g/HI.png)
    <figcaption>Figure 2: Overview of the Big Island of Hawai'i.</figcaption>
    </figure>

=== "2016 flow"

    <figure markdown>
    ![61g](img/61g/61g.jpg)
    <figcaption>Figure 3: Map of the 61g flow.</figcaption>
    </figure>

=== "Toes"

    <figure markdown>
    ![toes](img/61g/toes.jpg)
    <figcaption>Figure 4: Early emplacement of a new pāhoehoe flow as "toes" (Picture: S. Biass).</figcaption>
    </figure>

=== "Lava tube"

    <figure markdown>
    ![tube](img/61g/tube.jpg)
    <figcaption>Figure 5: Lava tube developed in a mature pāhoehoe field (Picture: S. Biass).</figcaption>
    </figure>

=== "Morphology transition"

    <figure markdown>
    ![pali](img/61g/pali.jpg)
    <figcaption>Figure 6: View of the Pali (meaning "cliff" in Hawaiian). At the top, the flow is pāhoehoe, but transitions to 'A'ā/open channel on higher slopes. At the bottom of the Pali, the flow reverts back to pāhoehoe (Picture: S. Biass).</figcaption>
    </figure>

#### Evolution of the flow field

The evolution of the pāhoehoe flow field was studied during the eruption using [structure-from-motion](https://en.wikipedia.org/wiki/Structure_from_motion) from helicopter [^9], from which 3D maps of **topographic** and **thermal** features were created. These maps capture the spatio-temporal evolution of the dynamics of lava flow emplacement and highlight the difficulty in *predicting* the ensemble of controlling processes.

=== "Topographic evolution"

    Figure 7 illustrates how compound pāhoehoe lava flows alter the topography, which affects the emplacement of subsequent flow units.

    <figure markdown>
    ![dem](img/61g/dem.png)
    <figcaption>Figure 7: Elevation changes calculated as the difference with the pre-flow DEM[^9].</figcaption>
    </figure>

=== "Thermal evolution"

    Figure 8 shows the thermal evolution of the surface of compound pāhoehoe lava flows. The initial, uniformly high surface temperature gradually decreases, which reflects the thermal insulation of the flow and the development of lava tubes. Lava tubes efficiently transport lava from the source to the front with little cooling, and drives the down-flow surface breakouts observed on 08/19.

    <figure markdown>
    ![thermal](img/61g/thermal.png)
    <figcaption>Figure 8: Thermal evolution of the flow's surface[^9].</figcaption>
    </figure>

=== "Steepest descent"

    Figure 9 shows the evolution of the prediction efficiency of the **path of steepest descent** approach as a consequence of the evolution of the DEM and the development of a tube system.

    <figure markdown>
    ![steepest](img/61g/steepest.png)
    <figcaption>Figure 9: Evolution of the stream network and comparison to the flow outlines and tube system[^9].</figcaption>
    </figure>


## :material-lightbulb-on:{ .icn } Conclusion 

Fundamental processes governing lava flow emplacement are numerous and complicated by feedbacks and non-linear interactions occurring at various temporal and spatial scales. The development of *predictive* models are impeded by two sources of uncertainties:

1. On the one hand, either the full range of parameters to accurately describe emplacement processes are rarely available (e.g., channelised flows) *or* physical models do not exist (e.g., pāhoehoe flows); this can be referred to as an **epistemic** uncertainty;
2. On the other hand, **stochastic** rather than physical processes dominate the emplacement dynamics (e.g., pāhoehoe flows); this can be referred to as an **aleatoric** uncertainty.

This limited ability to predict the evolution of lava flow crises result in high uncertainties during the management of long-lasting lava flow crises. In this context, lava flow hazard assessments should always be achieved with:

1. The understanding of the **limitations** of each models and their **sources of uncertainties**;
2. A framework to quantify and communicate uncertainties, which is out next topic.

## :material-check-bold:{ .icn } Summary

- **Lava flows** are non-newtonian fluids with a **yield strength**. 
- Their emplacement is controlled by **source conditions**, **topographic control** and **rheological properties**.
- No unified model for flow emplacement exists, and modelling approaches follow two main directions: **physical** and **stochastic** strategies.


## :fontawesome-solid-book:{ .icn } References

[^1]: Harris, A.J.L., Rowland, S.K., 2015. Lava Flows and Rheology. The Encyclopedia of Volcanoes 321–342. https://doi.org/10.1016/B978-0-12-385938-9.00017-1
[^2]: Kilburn, C.R.J.J., 2015. Lava Flow Hazards and Modeling. The Encyclopedia of Volcanoes 957–969. https://doi.org/10.1016/B978-0-12-385938-9.00055-9
[^3]: Cashman, K.V., Soule, S.A., Mackey, B.H., Deligne, N.I., Deardorff, N.D., Dietterich, H.R., 2013. How lava flows: New insights from applications of lidar technologies to lava flow studies. Geosphere 9, 1664–1680.
[^4]: Macdonald, G.A., 1953. Pahoehoe, aa, and block lava. American Journal of Science 251, 169–191. https://doi.org/10.2475/ajs.251.3.169
[^5]: Dietterich, H.R., Lev, E., Chen, J., Richardson, J.A., Cashman, K.V., 2017. Benchmarking computational fluid dynamics models of lava flow simulation for hazard assessment, forecasting, and risk management. Journal of Applied Volcanology 6, 9. https://doi.org/10.1186/s13617-017-0061-x
[^6]: Harris, A.J., Rowland, .S. FLOWGO: a kinematic thermo-rheological model for lava flowing in a channel. Bull Volcanol 63, 20–44 (2001). https://doi.org/10.1007/s004450000120
[^7]: Mossoux, S., Saey, M., Bartolini, S., Poppe, S., Canters, F., Kervyn, M., 2016. Q-LAVHA: A flexible GIS plugin to simulate lava flows. Computers & Geosciences 97, 98–109. https://doi.org/10.1016/j.cageo.2016.09.003
[^8]: de’ Michieli Vitturi, M., Tarquini, S., 2018. MrLavaLoba: A new probabilistic model for the simulation of lava flows as a settling process. Journal of Volcanology and Geothermal Research 349, 323–334. https://doi.org/10.1016/j.jvolgeores.2017.11.016
[^9]: Biass, S., Orr, T.R., Houghton, B.F., Patrick, M.R., James, M.R., Turner, N., 2019. Insights into pāhoehoe lava emplacement using visible and thermal structure-from-motion photogrammetry. Journal of Geophysical Research: Solid Earth 124. https://doi.org/10.1029/2019JB017444


*[ESP]: Eruption source parameter &rarr; most important initial conditions to a model
*[TGSD]: Total grain-size distribution
*[MER]: Mass eruption rate
*[VEI]: Volcanic explosivity index
*[HIM]: Hazard impact metrics
*[GAR]: Global assessment report
*[DDS]: Damage-Disruption states &rarr; one way of characterising vulnerability
*[GVP]: Global volcanism program 
*[GSD]: Grain size distribution
*[DEM]: Digital Elevation Model