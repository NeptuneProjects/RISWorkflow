# RISWorkflow

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
