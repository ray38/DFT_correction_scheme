# DFT_correction_scheme
correction of DFT energy via understanding of electronic environments


# Training Workflow # 

## 0: Data preparation ##

Generate data for training the correction scheme. A list of sample training systems are given in the `./preparation/sample_files` folder. It's a list of C, H, O, N containing small molecules with single point calculation done at CCSD(T)/cc-PVTZ level of theory pull down from the NIST CCCBDB dataset. Two parts of information from the high level calculation are needed: energy and coordinates, as given in the folder of each system. With these information, input files for SPARC are prepared that could calculate the energies on DFT level, and the corresponding features for each point in space.

Please run the calculations and get the feature files. it should be a series of csv files corresponding to each features.

Note: only need to run the calcualtions for the functionals of interest instead of all of them, but make sure to change your code for the later part of the workflow


Once all the calculations are finished, please run `./preparation/save_to_hdf5.py` script to collect the energy and feature information of all the systems with all functionals of interests into one giant .h5 file.

Note: Please change the path and list of functionals accordingly

## 1: Subsampling envrionment for each system ##

once
