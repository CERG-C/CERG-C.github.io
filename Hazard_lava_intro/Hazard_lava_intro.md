# Probabilistic hazard assessment for lava flow inundation 

Lava flows - beside being mesmerising to watch - are highly destructive volcanic phenomena. Over the past years, volcanic crises in [Hawaii](https://www.usgs.gov/volcanoes/kilauea/2018-lower-east-rift-zone-eruption-and-summit-collapse) in 2018, in [DRC](https://en.wikipedia.org/wiki/2021_Mount_Nyiragongo_eruption) and [La Palma](https://en.wikipedia.org/wiki/2021_Cumbre_Vieja_volcanic_eruption) in 2021 have demonstrated the difficulty in managing these long–lasting crises. This is due to the fact that lava flows are governed by complex rheological processes, making their paths hard to predict. As a result, forecasts are often associated with large uncertainties that makes them unusable *during* crisis management.

!!! help "Does this mean that we are helpless in reducing the risk associated with lava flows?"

Well, no, not entirely. In this exercise, we will differentiate between various purposes of hazard (and risk!) assessments for different parts of the *risk cycle*, contrasting between actions taken *long before* the event during the **prevention** phase - where the idea here is to *plan ahead* to reduce the risk - and actions taken *short before* or *during* the event in the **preparedness** and **response** phases - where the aim is to minimise immediate impacts. We will discuss these concepts throughout the exercise and in the field, but refer to the [ADVISE](https://appliedvolc.biomedcentral.com/articles/10.1186/s13617-021-00108-5)[^1] approach for an overview of the risk framework we are applying here.
 
<!--## Case-study: La Palma -->

## Exercise outline

In this exercise, we will look at two complementary approaches to assess the hazard associated with lava flow inundation that are the **path of steepest descent** and the **Q-LavHA** model. 

### Path of steepest descent 

Firstly, we will have a look at how simple hydrological tools can help us estimate the direction of lava flows. The **path of steepest descent** approach, which estimates flow direction based only on the hydrological properties of the terrain. Despite its simplicity, this is the [preferred method](https://www.usgs.gov/media/images/map-steepest-descent-paths-area-eruptive-fissures-k-lauea) used by [USGS](https://www.usgs.gov) and [Hawaii Volcano Observatory](https://www.usgs.gov/observatories/hvo) (HVO) to communicate with stakeholders during lava flow crises. 

### Q-LavHA

Secondly, we will test the **Q-LavHA** model, which goes one step forward in attempting to *predict* lava flow inundation using some stochastic strategies to estimate the uncertainty associated with lava flow emplacement processes.

## Objectives 

With this exercise, using two types of approaches to estimate the hazard associated with lava flow inundation, you will:

- Compare *deterministic* and *probabilistic* approaches.
- Understand the value of *uncertainty quantification* and its role in risk communication.
- Appreciate the difference between short-term hazard communication during crises and long-term hazard assessment for risk mitigation.


!!! info "Communicating uncertainties during lava flow crises" 
    Since the beginning of the Pu‘u‘ō‘ō eruption in 1983 to [its end in 2018](https://www.usgs.gov/volcanoes/kilauea/puuoo-eruption-lasted-35-years), the Big Island of Hawaii has been periodically affected by lava flow crises. These repeated crises have provided important lessons on how to communicate hazard uncertainties during crises. During the 2014 crisis, the flow field was dangerously heading towards the town of Pāhoa. Under pressure from decision makers, HVO attempted to provide a *forecast* and estimated that the flow *might* reach the town of Pāhoa within *a few* to *tens* of days... only that the media only reported the "a few" days, creating panic amongst the community.

    HVO realised the difficulty in communicating such a large uncertainty in operational activities and decided to cease providing forecasts. Instead, they reverted back to the **steepest descent method** which, although over-simplifying complex flow-emplacement processes, has the benefit of being transparent. In addition, HVO conducted meetings with stakeholders, agencies and the public, where they explained the limitations encountered when modeling lava flows. This combination of the use of a simplistic model with outreach events proved out to be the most efficient communication procedure and contributed to both increasing the trust in HVO and efficiently reducing the risk[^2][^3].

## References

[^1]: Bonadonna, C., Frischknecht, C., Menoni, S., Romerio, F., Gregg, C.E., Rosi, M., Biass, S., Asgary, A., Pistolesi, M., Guobadia, D., Gattuso, A., Ricciardi, A., Cristiani, C., 2021. Integrating hazard, exposure, vulnerability and resilience for risk and emergency management in a volcanic context: the ADVISE model. J Appl. Volcanol. 10, 7. https://doi.org/10.1186/s13617-021-00108-5
[^2]: Poland, M., Orr, T.R., Kauahikaua, J.P., Brantley, S.R., Babb, J.L., Patrick, M.R., Neal, C.A., Anderson, K.R., Antolik, L., Burgess, M., 2016. The 2014–2015 Pāhoa lava flow crisis at Kīlauea Volcano, Hawai ‘i: Disaster avoided and lessons learned. GSA Today 26, 4–10.
[^3]: Neal, C.A., Brantley, S.R., Antolik, L., Babb, J., Burgess, M., Calles, K., Cappos, M., Chang, J.C., Conway, S., Desmither, L., Dotray, P., Elias, T., Fukunaga, P., Fuke, S., Johanson, I.A., Kamibayashi, K., Kauahikaua, J., Lee, R.L., Pekalib, S., Miklius, A., Million, W., Moniz, C.J., Nadeau, P.A., Okubo, P., Parcheta, C., Patrick, M.P., Shiro, B., Swanson, D.A., Tollett, W., Trusdell, F., Younger, E.F., Zoeller, M.H., Montgomery-Brown, E.K., Anderson, K.R., Poland, M.P., Ball, J., Bard, J., Coombs, M., Dietterich, H.R., Kern, C., Thelen, W.A., Cervelli, P.F., Orr, T., Houghton, B.F., Gansecki, C., Hazlett, R., Lundgren, P., Diefenbach, A.K., Lerner, A.H., Waite, G., Kelly, P., Clor, L., Werner, C., Mulliken, K., Fisher, G., 2018. The 2018 rift eruption and summit collapse of Kīlauea Volcano. Science 7046, eaav7046. https://doi.org/10.1126/science.aav7046

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