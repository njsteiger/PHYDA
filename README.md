# PHYDA

This repository contains the code necessary for performing the reconstructions of the Paleo Hydrodynamics Data Assimilation product (PHYDA) presented in: Steiger, N. J., Smerdon, J. E., Cook, E. R., and Cook, B. I., "A reconstruction of global hydroclimate and dynamical variables over the Common Era", Scientific Data, 5:180086, doi: 10.1038/sdata.2018.86.

Steps in reproducing the reconstructions using the MATLAB code:

(1) Download all github code into the working directory

(2) Download the subdirectories containing all the input data from: clifford.ldeo.columbia.edu/nsteiger/hydro_input into the working directory.

(3) Make a selection of the reconstruction choices (e.g., seasonality of the reconstruction, state variables to include, etc.) by directly editing and commenting out key lines in the file 'prmtrs_ann_da.m'. This file sets the parameters of the reconstruction and can be modified by the user to reproduce the reconstructions in PHYDA (or to create reconstructions using different choices). For reproducing PHYDA, only modify the lines indicating the seasonality of the reconstruction (lines 22/23, 26/27, 30/31) with all other lines remaining as they are. See the PHYDA publication for more reconstruction details.

(4) The reconstructions can then be run by invoking 'da_ann.m'.

Please note that a large amount of RAM may be required to perform reconstructions using this code, depending on the choice of state variables that are included in the reconstruction or if the full posterior ensembles are to be saved; some choices may result in state variables several tens of GB or possibly over 100 GB in size. These reconstructions were run using Matlab2015a on a Linux machine with 128 GB of RAM.

Nathan Steiger, LDEO, Columbia University, May 2018.



