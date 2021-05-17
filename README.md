# RISWorkflow
This repository contains data and instructions for how to implement the RISCluster package.

RISCluster is a package that implements **deep embedded clustering** (DEC) of
seismic data recorded on the Ross Ice Shelf, Antarctica from 2014-2017. This
package is an accompaniment to a paper submitted to the Journal of Geophysical Research (Jenkins II et al., submitted).

RISCluster is in the process of being restructured so that it can be installed
and run on a Mac or Linux environment.

This repository is a PyTorch implementation of DEC. The workflow is as follows:
1. Load and pre-process data
2. Construct a convolutional auto-encoder (AEC)
3. Tune, train, and validate AEC
4. Incorporate clustering layer into AEC model architecture
5. Intialize clusters (K-Means, GMM available)
6. Train the DEC model: clustering and model training are simultaneous.
7. Once trained, infer class labels for remainder of the data set.

***
### Installation
1. Install RISCluster using instructions contained in the [RISCluster repository readme.md](https://github.com/NeptuneProjects/RISCluster).
2. Clone this repository to your desired working directory.
3. Unzip environmental data files.

***
### Usage
The Jupyter notebook **[Workflow.ipynb](https://github.com/NeptuneProjects/RISWorkflow/blob/main/Workflow.ipynb)** contains an end-to-end workflow control that guides the user through all steps of the project, including downloading and pre-processing the seismic data.  All necessary configuration files and command-line scripts are generated within the notebook.  Actual command-line scripts are copied from the Jupyter notebook into a terminal window.

***
### References
*Submitted*: William F. Jenkins II, Peter Gerstoft, Michael J. Bianco, Peter D. Bromirski; *Unsupervised Deep Clustering of Seismic Data: Monitoring the Ross Ice Shelf, Antarctica.* Submitted to Journal of Geophysical Research on 20 Jan 2021; doi: https://doi.org/10.1002/essoar.10505894.2

Dylan Snover, Christopher W. Johnson, Michael J. Bianco, Peter Gerstoft; *Deep Clustering to Identify Sources of Urban Seismic Noise in Long Beach, California.* Seismological Research Letters 2020; doi: https://doi.org/10.1785/0220200164

Junyuan Xie, Ross Girshick, Ali Farhadi; *Unsupervised Deep Embedding for Clustering Analysis.* Proceedings of the 33rd International Conference on Machine Learning, New York, NY, 2016; https://arxiv.org/abs/1511.06335v2
***
### Author
Project assembled by William Jenkins
<br>wjenkins [@] ucsd [dot] edu
<br>Scripps Institution of Oceanography
<br>University of California San Diego
<br>La Jolla, California, USA
