# Setting up QGIS

This section sets up `QGIS` for the hazard assessment exercises. We will install [Q–LavHA](https://we.vub.ac.be/en/q-lavha), a model for the probabilistic hazard assessment of lava flows working as a `QGIS` plugin. 

## Objectives

This section provides instructions on how to:

- Configure `QGIS`.
- Load the necessary data in `QGIS`.

## Installing QGIS 

Download the relevant `QGIS` version for your own operating system from [this page](https://qgis.org/en/site/forusers/download.html).

!!! warning "Warning"

    `QGIS` should already be installed on the computers in the lab. It should only be installed if you are planning on following the exercise on your own laptop. 


## Starting QGIS

- Search for `QGIS 3.2x` and start it. Depending on the computer, the version might vary between `3.20` and `3.23`. Please take the most advanced one. 

### Change the language

As `QGIS` will most likely be in French, let's change it to English:

1. From the [Menu Bar](QGIS_Intro.md#the-qgis-interface), choose `Préférences` > `Options` > `Général`
2. Change the *Langue de l'interface graphique* to English (Fig. 1)
3. Close and restart `QGIS`

<figure markdown>
  ![QGIS_language](img/qgis/qgis_language.png)
  <figcaption>Figure 1: Change the QGIS language</figcaption>
</figure>

### Activate the Coordinate Capture Tool

The *Coordinate Capture* allows to capture the coordinates when clicking on the map canvas, which will be useful throughout the exercices.

First install it: From the Menu bar, use the `Plugins > Manage and Install Plugins` tool and search for the `Coordinate Capture` tool and install it. To activate it, right-click anywhere in the [Toolbar](QGIS_Intro.md#the-qgis-interface) and activate the `Coordinate Capture Panel`.

