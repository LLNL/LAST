### Dataset Overview:

This dataset is associated with our publication titled "A Global Perspective on Supercomputer Power Provisioning: Case Studies from United States and Europe", to appear at the ACM International Conference on Supercomputing in June 2025 (DOI: TBD). Please cite this paper when using this dataset.

It contains power telemetry data from seven supercomputers across six sites.
The supercomputers considered at each site, identified by their name and associated Top500 rank at the time of data collection, are:
1. Perlmutter (\#12) and Cori (\#60), at National Energy Research Scientific Computing Center (NERSC), United States
2. Summit (\#7), Oak Ridge National Laboratory (ORNL), United States
3. Sierra (\#10), Lawrence Livermore National Laboratory (LLNL), United States
4. Marconi-100 (\#35), CINECA, Italy
5. Lumi (\#5), CSC IT Center for Science Ltd., Finland
6. Hawk (\#42), High-Performance Computing Center Stuttgart (HLRS), Germany

### Authors:
- Tapasya Patki, LLNL, patki1@llnl.gov
- Barry Rountree, LLNL, rountree4@llnl.gov
- Torsten Wilde, HPE, wilde@hpe.com
- Christian Simmendinger, HPE, christian.simmendinger@hpe.com
- Ralf Schneider, HLRS,ralf.schneider@hlrs.de
- Stephanie Brink, LLNL, brink2@llnl.gov
- Kathleen Shoga, LLNL, shoga1@llnl.gov
- Zhengji Zhao, LBL, zzhao@lbl.gov
- Ermal Rrapaj, LBL, ermalrrapaj@lbl.gov
- Nicholas Wright, LBL, njwright@lbl.gov
- Woong Shin, ORNL, shinw@ornl.gov
- Matthias Maiterth, ORNL, maiterthm@ornl.gov
- Jim Rogers, ORNL, jrogers@ornl.gov
- Esa Heiskanen, CSC, esa.heiskanen@csc.fi
- Andrea Bartolini, Cineca, a.bartolini@unibo.it
- Sachin Satish Idgunji, Nvidia, sidgunji@nvidia.com

### CSV Descriptions:

Each CSV file is identified by the system it belongs to along with the sampling rate of power measurements (frequency of data collection).  
It has two columns, timestamp (in seconds) and measured power in kilowatts.

- Cori (LBL), Perlmutter (LBL), Marconi-100 (Cineca), Lumi (CSC) and Hawk (HLRS) are full datasets.
- Summit (ORNL) and Sierra (LLNL) datasets are a summary providing quartile information only.

Note: The Hawk dataset has ~1500 rows with leading zeros in the beginning, we did not modify the original dataset.

In addition to system-level telemetry, two additional application-level power measurement datasets (`lumi_hpcg_data` and `hlrs_hpl_hpcg_data` folders) have been included. These are:
- High Performance Conjugate Gradients (HPCG) Benchmark power data from Lumi supercomputer.
- High-Performance Linpack (HPL) Benchmark and HPCG power data, along with the different power capping algorithms (Figure 5 in the paper), from the Hawk supercomputer.

### Acknowledgments
Authors wish to thank Pekka Lehtovuori from CSC IT Center for
Science Ltd., Finland for help with collection, review and release
of the Lumi dataset. 

Part of this work was performed under the
auspices of the U.S. Department of Energy by Lawrence Livermore
National Laboratory under Contract DE-AC52-07NA27344 (LLNL-
CONF-862432). 

Part of this material is based upon work supported
by the Advanced Scientific Computing Research Program in the
U.S. Department of Energy, Office of Science, under Award Number
DE-AC02-05CH11231 and used resources of the National Energy
Research Scientific Computing Center (NERSC), which is supported
by the Office of Science of the U.S. Department of Energy under Con-
tract No. DE-AC02-05CH11231. 

Part of this research was sponsored
by and used resources of the Oak Ridge Leadership Computing
Facility (OLCF), which is a DOE Office of Science User Facility at
the Oak Ridge National Laboratory (ORNL) supported by the U.S.
Department of Energy under Contract No. DE-AC05-00OR22725.

This work was partially funded by the German Federal Ministry
of Education and Research (BMBF) and the Ministry of Science,
Research and the Arts Baden-Württemberg (MWK) as part of the
SiVeGCS project.

### License
Creative Commons Attribution 4.0 International Public License

LLNL Sierra summary data release number: LLNL-MI-862385.
