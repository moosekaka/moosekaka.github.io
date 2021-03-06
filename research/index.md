---
layout: default
---

# What is my research about?
Developing a set of open-source computational tools in Python to perform multi-scale analysis of structure-function relationship in mitochondrial networks. My model organism is *Saccharomyces cerevisiae*, also known as budding yeast.

<p align="center">
<img src="{{site.github.url}}/images/website.jpg" width="78%" />
</p>

## Segmentation of mitochondrial networks from live yeast cells 3D images taken with a *spinning disk confocal* microscope
- The segmentation pipeline utilizes [MitoGraph](https://github.com/vianamp/MitoGraph.git), a C++ skeletonization and segmentation program developed by Matheus Viana. It has been fully validated in yeast cells \([Viana, Lim *et al.*](http://www.ncbi.nlm.nih.gov/pubmed/25640425)).
- The [pipeline](https://github.com/moosekaka/sweepython/blob/master/pipeline) folder contains modules used to map mitochondrial function to structure. This pipeline utilizes Mayavi's version of [VTK](http://www.vtk.org/) which contains convenient Python wrappers for VTK functions.
- This [notebook](https://github.com/moosekaka/sweepython/blob/master/Pipeline.ipynb) shows an example of a typical workflow.
- The output data from the pipeline was 'munged' into a database using [`Pandas`](http://pandas.pydata.org/pandas-docs/stable/) before further calculations of various statistical and functional parameters.

## Modulation of mitochondrial function by altering carbon source growth conditions
- We modulated the metabolic state of the cell by altering the carbon source used during cell growth. This [notebook](https://github.com/moosekaka/sweepython/blob/master/o2_vr_dy_panel.ipynb) shows an example of how carbon source growth conditions alters oxygen consumption and mitochondrial membrane potential (Δψ), which is a key parameter of cell bioenergetics.

## Investigating the link between structure of mitochondria and heterogeneity of mitochondrial membrane potential (Δψ)
- We showed the non-random heterogeneous distribution of Δψ within a single mitochondrial tubule [example here](https://github.com/moosekaka/sweepython/tree/master/tubuleHet).

- We also detail our investigation into the relationship between heterogeneity of mitochondrial function and network topology [example here](https://github.com/moosekaka/sweepython/tree/master/networkHet).

## Analysis of mitochondrial functional asymmetry in mother and daughter yeast cells
- A [set of tools](https://github.com/moosekaka/sweepython/tree/master/mombud/vtk_viz) to interactively visualize the 3D mitochondrial skeleton and pick points to classify the cell as a mother or daughter region. This [Ipython notebook](https://github.com/moosekaka/sweepython/blob/master/mother%20bud%20analysis.ipynb) demonstrates an application of these tools to study how mitochondrial membrane potential (Δψ) is distributed differently between the mother and daughter cell.  


### Requirements
If you wish to download the source code for the pipeline, you need to have these dependencies installed:

* Pandas
* Matplotlib
* Mayavi\**
* NetworkX
* Numpy
* Seaborn
* Scipy
* VTK

\**MayaVi has a known conflict when run under IPython and Python 2.7, specifically incompatible API versions. To fix, set QT_API=pyqt under your enviroment variables, either in BASH or Windows advanced settings. The best way to ensure all dependencies are fulfilled is by installing the [Anaconda](https://www.continuum.io/downloads) Python package.
