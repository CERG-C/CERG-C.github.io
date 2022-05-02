password: askja1875

## Exercise

### Question 1: Eruptive history
1. > On the cumulative GVP plot, what does the slope of the plot (i.e., the ratio of `y` to `x`) represent?
      - It represents the eruption frequency
2. > How does it vary in time, and how do you explain it?
      - It can be broken in two segments that indicate changes in eruption frequency. This, however, is an artefact. The *oldest* segment represents the geological record (where larger VEIs are usually preserved), whereas the *youngest* segment represents the historical record, which fully accounts for small eruptions but might be too short to account for large eruptions.
3. > What is the **annual frequency of eruption** for the recent history?
      - There has been 8 eruptions since 1480 &rarr; $8 / (2022-1480) = 0.015$ eruption per year, or about 1 eruption every 67 years.

--- 

### Question 2: Wind conditions

1. > Visualize these wind patterns in the context of a hazard assessment. What is the main wind direction? How will that affect tephra dispersal?
      - Below 1 km, most of the dispersal is towards SW, with a slightly more S component for the month of May 
2. > How does the mean wind direction vary with height? How is that affecting eruptions of different sizes? (&rarr; refer to the note about *VEI and plume heights* above).
      - Between 1-10 km, there is a wider spread: winter months have a greater S component, other months have a stronger E component
3. > Do you notice any seasonality? If yes, identify during what months it happens.
      - Summer months have the lowest wind velocities below the tropopause

--- 

### Question 3: ESP

1. > Analyse the distributions of sampled ESP. For each ESP, discuss:
   > - From what distribution have each ESP been sampled from?
   > - What *prior knowledge* do these distribution reflect?

     - **Height:** logarithmic &rarr; small heights have more probability of occurrence 
     - **Mass:** gaussian &rarr; most likely mass ~4, but symmetric error 
     - Other: uniform, equal probabilities of occurrence


--- 

### Question 4: Probability calculation

1. > The [previous module](Hazard_probabilistic2.md) has introduced how to compute *exceedence probability* for tephra accumulation. Based on the 10 simulations below for pixel $x,y$, what are the probabilities of this pixel to suffer tephra accumulations exceeding:

    - 50 $kg/m^2$ &rarr; $10/10 = 100\%$
    - 100 $kg/m^2$ &rarr; $7/10 = 70%\%$
    - 150 $kg/m^2$ &rarr; $2/10 = 20%\%$

2. > Similarly, we also learned how to estimate a **typical accumulation** associated with a given probability of occurrence. The figure below shows the [survivor function](Hazard_probabilistic2.md#hazard-outputs) for the data in the table above. Estimate the typical load associated with probability values of:

   - 25% &rarr; ~122 $kg/m^2$
   - 75% &rarr; ~85 $kg/m^2$

--- 

### Question 5: Probability maps

1. > Describe the geometry (i.e., extent, orientation) of selected probability maps.
2. > With your knowledge of hazardous thresholds of tephra accumulations previously discussed, what can you conclude with respect to the risk related to tephra fallouts?

❗ to do