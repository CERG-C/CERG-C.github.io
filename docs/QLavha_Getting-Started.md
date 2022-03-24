# Setting up QGIS

This section sets up `QGIS` for the hazard assessment exercises. We will install [Q–LavHA](https://we.vub.ac.be/en/q-lavha), a model for the probabilistic hazard assessment of lava flows working as a `QGIS` plugin. 

## Objectives

This section provides instructions on how to:

- Configure `QGIS`.
- Install `Q–LavHA`.
- Load the necessary data in `QGIS`.

## Installing Q-LavHA 

1. Download `Q–LavHA` from this link.
2. In Windows, navigate to the following folder, where `$USER` is your ISIS username:

```
C:\Users\$USER\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins
```

!!! note
    If the `plugins` folder doesn't exist, then create it.

3. Copy the `Qlavha_v3` to the `plugins` folder.

## Starting QGIS

- Search for `QGIS 3.2x` and start it. Depending on the computer, the version might vary between `3.20` and `3.23`. Please take the most advanced one. 

### Change the language

As `QGIS` will most likely be in French, let's change it to English:

1. From the [Menu Bar](QGIS_Intro.md#the-qgis-interface), choose `Préférences` > `Options` > `Général`
2. Change the *Langue de l'interface graphique* to English (Fig. 1)
3. Close and restart `QGIS`

<figure markdown>
  ![QGIS_language](../img/QGIS/qgis_language.png)
  <figcaption>Figure 1: Change the QGIS language</figcaption>
</figure>

### Activate the Coordinate Capture Tool

The *Coordinate Capture* allows to capture the coordinates when clicking on the map canvas, which will bu useful throughout the exercices. To activate it, right-click anywhere on the in the [Toolbar](QGIS_Intro.md#the-qgis-interface) and activate the `Coordinate Capture Panel`.

## Activate Q-LavHA

To activate `Q–LavHA` in `QGIS`:

1. Re-open `QGIS` as previously.
2. From the [Menu Bar](QGIS_Intro.md#the-qgis-interface), open the `Plugins` > `Manage and Install Plugins` window.
3. Following Figure 3, search for `lava` and activate the plugin.
4. There should now be a `Q-LavHA` icon in the [Toolbar](QGIS_Intro.md#the-qgis-interface).

<figure markdown>
  ![QGIS_plugin](../img/QGIS/qgis_plugin.png)
  <figcaption>Figure 2: Activate the Q–LavHA plugin</figcaption>
</figure>
 
## Loading data