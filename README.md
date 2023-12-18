# Sorghastrum Nutans Habitat Suitability Model
[![DOI](https://zenodo.org/badge/732454940.svg)](https://zenodo.org/doi/10.5281/zenodo.10399448)

## Overview

The final project of GEOG 4463-5463 (Earth Analytics Bootcamp) is to look into building a habitat suitability model for Sorghasstrum Nutans.

This repository contains a Jupyter Notebook (`sorghastrum-nutans.ipynb`) which is the core of the content. 
A HTML file is generated so you can preview the results. All supporting images are stored in the `\img` folder.

## Data Sources

* **Grassland Shape Files:** From USFS at data.fs.usda.gov
* **Elevation Data:** SRTM (NASA Shuttle Radar Topography Mission) via APPEEARS API
* **Soil pH:** Polaris dataset from Duke University
* **Climate Data:** MACAv2 Precipitation and Humidity datasets


## How to Run

### Set up Environment
```
conda activate base
conda install -c conda-forge mamba
mamba env create -f environment.yml
conda activate earth-analytics-python
pip install git+https://github.com/earthlab/earthpy@apppears
```

### Quirks 
Comment out any `hvplot()` related code before you run this notebook.
When you save a Jupyter notebook to HTML using the `nbconvert` command, the Python kernel is not included.
Due to that, I had to comment the `hvplot()` parts out and referenced saved images in order to generate a desired HTML.
