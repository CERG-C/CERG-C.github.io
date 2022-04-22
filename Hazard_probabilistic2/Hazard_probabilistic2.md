# Probabilistic modelling: Part 2

We have [previously](Hazard_probabilistic1.md) looked at probabilistic modeling for lava flows, where we accounted for the uncertainty of vent location on hazard quantification. However, probabilistic hazard assessment strategies often have to account for the uncertainty on **more than one** parameter. This section sets the stage for probabilistic assessment of tephra fallout and digs one step further into the mechanics of probabilistic hazard modeling.

## :material-format-list-checks:{ .icn } Objectives

- Understand the concepts of **probabilistic eruption scenarios**.
- Review the concepts of **deterministic**, **scenario-based probabilistic** and **probabilistic** volcanic hazard assessments.
  
## Probabilistic modeling workflow 

From now on, we will refer to model inputs as **Eruption Source Parameters** - or **ESP**. Probabilistic modeling requires one to:

1. Identify relevant ESPs for a problem.
2. Estimate the uncertainty on each ESP.



The first aspect to identify is **what ESP is critical** for the hazardous phenomenon of interest. For instance, important ESP for tephra accumulation include the plume height, the erupted mass, the mass eruption rate and the grain-size distribution. 

The choice of ESP must be put in context of the **selected model** for hazard assessment. Typically, **complex numerical models** are very **accurate** but require a **large number of ESPs**, which can be difficult to obtain. For instance, `FLOWGO` is a model that simulates lava flows based on the evolution of thermo-rheological properties that requires the identification of tens of different ESPs. Conversely, **simpler models** rely on simpler assumptions, usually require **less ESPs** but typically have a lower accuracy (e.g., `Q-LavHA`).



## Estimate the uncertainty of ESPs 

Probabilistic modeling requires to define ESPs not as **single** but as **distributions** of values, generally defined as:

1. A **range** of values (i.e., the `minimum` and `maximum` values to explore).
2. A **shape** of distribution. 

These two components reflects the **knowledge** that we, as "experts", have of the problem. Figure 4 illustrates 4 types of uncertainty distributions that can be applied to ESPs:

- The **top left** example is a `uniform` distribution: In this case, any value between `min` and `max` has an **equal probability of occurrence**. This is often referred to as a *maximum level of ignorance*. 
- The **top right** example is a `logarithmic` distribution: In this case, we assume that **smaller values** have higher probabilities of occurrence **than larger** ones. For instance, large earthquakes occur more often than small ones. 
- The **bottom left** example is a `gaussian` distribution: Here we assume that **a central value** has the highest probability of occurrence, but it can divert from it in a **symmetrical** fashion.
- Finally, the **bottom right** example represent an unrealistic case where `min`=`max`. This would only occur if there was **no uncertainty**.

<figure markdown>
  ![esp](img/ESP/ESP.png){ width="600" }
  <figcaption>Figure 4: Various approaches to quantify ESP uncertainties during probabilistic modeling.</figcaption>
</figure>


!!! info "What uncertainty"

    Conceptually, uncertainties can be classified in two categories:

    - **Epistemic uncertainty**  derives from the lack of knowledge regarding a phenomena. In theory, we could reduce epistemic uncertainties if more observations of the phenomena were available to help us better constrain the underlying processes and behaviours.
    - **Aleatoric uncertainty** is associated with the inherent randomness of natural processes. 

    The types of distributions shown in Figure 4 combine both types of uncertainties. Although a better characterisation of the **epistemic** uncertainty would help to refine the *top left* distribution towards a distribution centered on a *best guess* values, the constant presence of an **aleatoric** component of uncertainty is the reason why the *bottom right* distribution is impossible to achieve.

**How do we improve our knowledge of the uncertainties around ESPs?** Ideally, identifying the range of ESPs is based on **extensive field studies**. By reconstructing the **stratigraphy** of a volcanic edifice, we can study its **past eruptive history**, which is then used to estimate the potential future **eruption scenarios**. 


## Various approaches for hazard assessment

### Deterministic scenarios

**Deterministic** hazard assessments: Usually based on past events, they express the hazard should *the exact same event* happen again in the future. As we have seen, this is impossible, and, in the end, this approach fails to account for and quantify uncertainties. However, their benefit is that they are easy to communicate with decision makers. Deterministic scenarios are mostly used for the development of contingency plans in contexts, **only when** a well-established communication channel exists between monitoring agencies, decision-makers and stakeholders. 

### Scenario-based 

### Probabilistic volcanic hazard assessments

Probabilistic volcanic hazard assessments - or **PVHA**





