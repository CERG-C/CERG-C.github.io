password: askja1875

## Path of steepest descent 

### Question 1: Path of steepest descent

#### Aim

Manually estimate the path of steepest descent.

#### Questions 

1. > Starting from this DEM, can you estimate the most likely flow direction and the flow accumulation values?
    - Discuss process

#### To discuss

- General philosophy.
- Mention how topographic lows can become numerical pits. 

---

### Question 2: Drainage basin

#### Aim

Get an idea of how topography controls the definition of drainage basins and, more generally, surface runoff

#### Questions

You can observe a large discrepancy in the **area** and the **shape** of the various drainage basins.

1. > How do they spatially vary over the island?
2. > How do they relate to the underlying topography? 
    - The higher the topography, the larger the drainage system &rarr; caldera 
    - When sharp topographic highs (e.g., ridge) &rarr; the basin is well-defined
    - Conversely, when flatter topography (e.g., south of the island) &rarr; basins become smaller, more irregular 
    - Close to the sea, many small basins 

#### To discuss

- **Maturity** of drainage system

---

### Question 3: Historical lava flows

#### Aim

Introduce the past lava flows at La Palma and how that will condition future hazard. Based on the observation of the geological map.

#### Questions

1. > Can you spot where historical lava flows occurred?
    - Find the lava flows based on the legend
2. > Are they originating from *a single* or *multiple* vents?
    - They occurred from multiple vents aligned along the N-S ridge
3. > In historical times, what part of the island has been most affected by lava flows?
    - South appears more active in historical time
4. > How do the directions of past flow match predictions from hydrological modeling?
    - They roughly follow paths of steepest descent, but they are wider

#### To discuss

- Concept of **monogenetic** vents and fields

---

### Question 4: Vent opening

#### Aim

Introduce the concept of vent opening uncertainty in hazard assessment

#### Questions

1. > If all vents in Figure 1 have an **equal probability of occurrence**, does that mean that the entire island is uniformly exposed to lava flow inundation? 
    - No. Basins defined by more mature hydrological networks will gather flow accumulation from a large number of vents &rarr; e.g., Los Llanos
2. > What parts of the island are most exposed to lava flow inundation?
    - Los Llanos is at the outlet of the largest drainage basin
3. > Are there any safe/shadow parts?
    - Regions with smaller basins that don't start from the ridge have lower relative probabilities of inundation

#### To discuss 

- Relationship between vent opening and drainage basin
- Assumption of uniform vent opening probability by Marrero et al. (2019) &rarr; motivated by high hazard/exposure/risk
- What is required to do better? i.e., long-term vs short-term hazard/risk assessments?

---

### Question 5: Evolution of the flow field

#### Aim

Put the path of steepest descent in perspective of the actual flow. Introduce uncertainties and *purpose* of hazard assessment

#### Questions

1. > How accurate would have been the **steepest descent** approach to *forecast* flow inundation of the 2021 eruption? How different is the actual flow compared to the drainage network?
      - The line of steepest descent captures the **main** inundation path, but fails to capture branching to secondary paths
2. > How dynamic is a months-long lava flow? Is it a *single* event or a compound *pulsatory* phenomena?
      - Compound, long-lasting flows are pulsatory phenomena. It is not only **one** but **many** that evolve with time throughout the eruption
3. > What event do you think corresponds to the dashed red line in Figure 2? What happens *before* and *after*?
      - Red line = Ocean entry
      - Before: Lengthening
      - After: Widening
4. > What are the *advance* and *widening* rates of the 2021 lava flow? Can you use it to estimate the advance and widening of possible lava flows from other vents?
      - Width: 3500 m / 30 days = ~116 m/day
      - Length: 6000 m / 10 days = 600 m/day during first phase, then ~1000 m in 80 days &rarr; 12.5 m/day

#### To discuss 

- See next point

---

### Question 6: Limitations

#### Aim

This is more of a reflection point based on the limitations raised during previous questions

#### To discuss 

- Compound lava flows evolve as a function of the **source conditions**, **rheology** and **morphology** (e.g., tube system?). Furthermore, previous flow units **permanently alter the topography**, which influences subsequent emplacement. 
- Lack of uncertainty 



## Q-LavHA


### Question 1: Single-vent simulations

#### Aim

- Run Q-LavHA simulations for single vents
- Discuss their outputs

#### Questions

1. > How do modelled flows compare to <a href="../files/GeologicalmapofLaPalma.pdf", target="_blank">historical lava flows</a> in terms of length and width?
      - They capture the general trend, but they are usually **not as wide** &rarr; single vs compound flow
2. > Analyse and discuss the spatial distribution of inundation probability. How do they compare to flow accumulation rasters and the path of steepest descent approach?
      - Highest probabilities tend to overlap with paths of steepest descents, which confirms the usefulness of hydrological modeling
3. > Where do branching occur?
      - Where two flow accumulation branches with high values are close &rarr; denotes similar topographic constraints
4. > Chose *one vent* for which you will produce another run with the same parameters as above. Are they **exactly** the same? If not, why?
      - There are differences, which are due to the stochastic nature of `Q-LavHA` &rarr; probabilistic modeling
5. > Compare simulations from **vent 2** with the flow outlines of the 2021 eruption. **When** and **where** is the model doing a good job? **When** and **where** is it not? Why?
      - `Q-LavHA` does a good job at capturing the path of the **early** date of the flow. It captures especially well the flow outlines until ocean entry. 

#### To discuss 

- `Q-LavHA` models only **a single** flow, not a compound field
- Variability due to several vent opening during a same eruptive event is not accounted for

--- 

### Question 2: Simulation with surface area

#### Aim

- Understand how the uncertainty on vent location affects hazard quantification

#### Questions

1. > Compare the run with its single-vent counterpart. How do they differ and why?
      - For well constrained basins (e.g., vent 3), the width is ± the same, but some channels have higher probabilities than before (e.g., the N channel becomes the most likely). 
      - In other cases (e.g., vents 1 and 2), the scenarios reveal new paths of inundation that tend to widen the predictions, but they have **low** probabilities of inundation &rarr; indicates the likelihood of low probability events &rarr; how do you account for these in risk planning?
      - Conversely, other vents (e.g., 4 and 5) show that vent opening uncertainty open access to entirely new drainage basins. This is due to larger-scale topographic constraints, either the ridge (vent 5) or previous lava channels (vent 4).


#### To discuss 

- Outline how **ignoring uncertainties** can result in a **fragmented** vision of the hazard.

--- 

### Question 3: Forecasting the flows from the 2021 eruption

#### Aim

- Understand how the uncertainty on vent location affects hazard quantification

#### Questions

1. > From what you know about both the 2021 eruption and the dynamics of lava flows, compare and discuss the hazard forecast and the actual deposit. What are `Q-LavHA`'s strengths and limitations?
      - The predicted inundated area corresponds fairly well to what really happened
      - The highest-probability channel captures the first ocean entry 
      - **However** &rarr; is that just a coincidence?
          - `Q-LavHA` simulates only a single flow &rarr; which means that the low probability areas represent what **could have happened** with the first flow unit
          - It does not capture the **dynamic evolution** of a flow field


#### To discuss 

- Illustrations of uncertainties and how to communicate them 
- "If a numerical model does a too good job to fast, there is probably something wrong"
- Be critical of outputs

--- 



### Resources

#### Areas for surface simulations 

| Vent   | Easting (m) | Northing (m) | xL     | xR     | yD      | yU      |
|:-------|:------------|:-------------|:-------|:-------|:--------|:--------|
| Vent 1 | 222340      | 3169746      | 222090 | 222590 | 3169496 | 3169996 |
| Vent 2 | 219728      | 3168426      | 219478 | 219978 | 3168176 | 3168676 |
| Vent 3 | 221922      | 3165623      | 221672 | 222172 | 3165373 | 3165873 |
| Vent 4 | 224646      | 3167772      | 224396 | 224896 | 3167522 | 3168022 |
| Vent 5 | 221357      | 3155562      | 221107 | 221607 | 3155312 | 3155812 |

