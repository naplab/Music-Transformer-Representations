# Standalone Software for Extracting Music Transformer Representations

This includes the code for extracting music transformer representations from the `musicautobot` model, since this portion of our analysis is not a standard method used across the field. We provide the code for extracting these representations from midi files, which are then used to train temporal receptive field (TRF) models which predict neural responses.

## System Requirements

This requires Python>=3.6 and MuseScore.

This has been tested with python version 3.9 and MuseScore 3


## Installation Guide

- MuseScore can be downloaded here: https://musescore.org/en/handbook/3/download-and-installation
- One simple way to install python is with Anaconda: https://docs.anaconda.com/anaconda/install/

The remaining python package dependencies can be downloaded and installed into a conda environment using the provided `environment.yml` file, by running the following command:

```
conda create -f environment.yml
```

## Demo

We provide a file called `Demo_Midi_Representations.ipynb` which is a jupyter notebook file that is run with python. It will first download the pretrained Musicautobot transformer model weights, and then instantiate a model and extract layer activations from the midi files.

The expected output should be saved files containing the representations for TRF analysis.

The longest portion of the runtime is from downloading the model, which may take about 20-30 minutes.

## Instructions for Use

First, download the Midi stimuli files here: https://datadryad.org/stash/dataset/doi:10.5061/dryad.g1jwstqmh

Simply run `Demo_Midi_Representations.ipynb` with jupyter-notebook to extract layer representations from the Midi files.