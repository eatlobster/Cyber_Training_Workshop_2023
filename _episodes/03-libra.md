---
title: "3. Nonadiabatic Dynamics and More with Libra"
---

<a name="toc"></a>
# Table of Content
1. [General overview and Installation]](#1)
2. [Theoretical Background](#2)
3. [Tutorials](#3)
  3.1. [Getting Started](#3.1)
  3.2. [General-purpose capabilities](#3.2)
  3.3. [NA-MD (TSH and Ehrenfest dynamics) for model Hamiltonians](#3.3)
  3.4. [NA-MD (TSH) for atomistic systems](#3.4)
  3.5. [Wavepackets and Quantum Trajectories with Adaptive Gaussians (QTAG)](#3.5)
  3.6. [Exact dynamics via SOFT-DVR](#3.6)
  3.7. [Hierarchical Equations of Motion (HEOM)](#3.7)
  3.8. [Auxiliary methods for computational chemistry codes](#3.8)


<a name="1"></a>
## 1. General overview of Libra. 
[Back to TOC](#toc)

### 1.1. Overview and Installation

This workshop will involve experience with Python-based software and packages. One that will be used extensively throughut 
the event is the [Libra](https://github.com/Quantum-Dynamics-Hub/libra-code/tree/devel) package developed by the 
[Akimov group](https://akimovlab.github.io/). 

Although Libra and some of its strong and weak dependencies are already installed on UB CCR and will be directly accessible via
the Jupyter notebooks on OnDemand, you may want/need to install them locally. Since most of the calculations we'll be doing 
are not too intensive computationally, runnig most of them on your laptop shall not be a problem. 

You may want to use this option, if you want to follow the hands-on exercises with Libra, but you have not been accepted as a fully-fledged 
participant (the participant without full access to UB CCR resources, which may be because of your geographic location at the moment).

Please follow the [installation instructions](https://github.com/Quantum-Dynamics-Hub/libra-code/tree/devel) to build the corresponding 
environment, install all needed dependencies and packages, and build and install the Libra code itself. **Make sure to use the "devel" branch**. 


### 1.2. Slides 

  To be Added

  * [From summer 2022](../files/Alexey_Akimov/July5-morning.pdf)


### 1.3. Videorecording of the session

  To be Added 


## 2. Theoretical Background
[Back to TOC](#toc)

### 2.1. Slides

  To be Added

### 2.2. Videorecording of the session

  To be added 



<a name="3"></a>
## 3. Tutorials
[Back to TOC](#toc)

<a name="3.1"></a>
### 3.1. Getting Started

  To start - clone thetutorials repository into your working directory

      git clone https://github.com/compchem-cybertraining/Tutorials_Libra.git


<a name="3.2"></a>
### 3.2. General-purpose capabilities

  * [Basic algebra](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/3_linear_algebra/1_vector_matrix_cmatrix_basics/tutorial.ipynb)
  * [Matrix decompositions](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/3_linear_algebra/2_matrix_functions/tutorial.ipynb)
  * [Statistics](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/7_special_functions/4_random_numbers/1_basics/tutorial.ipynb)
  * [Metropolis](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/7_special_functions/4_random_numbers/2_metropolis/tutorial.ipynb)
  * [Runge-Kutta for classical MD](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/2_integrators/1_runge_kutta_4th_order/tutorial.ipynb)
  * [Runge-Kutta for Liouville Eq](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/2_integrators/2_runge_kutta_4_for_Liouville/tutorial.ipynb)
  * [Program-specific utility functions](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/11_program_specific_methods/2_qe_methods)
  * [ML Basics](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/9_machine_learning/1_basics_of_mlp/tutorial.ipynb)
  * [ML Derivatives](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/9_machine_learning/2_ann_derivatives/tutorial.ipynb)
  * [ML Advanced](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/9_machine_learning/3_advanced_ann/tutorial.ipynb)


### 3.3. NA-MD (TSH and Ehrenfest dynamics) for model Hamiltonians


  * [namd_workflow, scattering calculations](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/1_trajectory_based/8_model_nonadiabatic/tutorial.ipynb)
  * [lower level functions, adiabatic, Ehrensfest, and TSH calculations](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/1_trajectory_based/2_model_adiabatic_ehrenfest_fssh/tutorial.ipynb)


### 3.4. NA-MD (TSH) for atomistic systems

  * [Slides from the summer 2022 workshop](../files/Mohammad_Shakiba/July5-morning.pdf)
  * [Step 1, cp2k/DFT](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/2_nbra_workflows/6_step1_cp2k/1_DFT/1_example_TiO2/tutorial.ipynb)
  * [Step 2, cp2k/DFT](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/2_nbra_workflows/7_step2_cp2k/1_DFT/2_hpc/1_example_TiO2/tutorial.ipynb)
  * [Step 3, cp2k/DFT](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/2_nbra_workflows/8_step3_cp2k/1_DFT/tutorial.ipynb)
  * [Step 4, cp2k/DFT](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/2_nbra_workflows/9_step4_cp2k/tutorial.ipynb)
  * [Interfaces with other codes](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/8_model_hamiltonians/2_interfaces_with_qchem_codes/tutorial.ipynb)

    For the DFTB+ part, make sure to download the parameters files and change kernel to libra-latest

  * [DFTB+, command-line example](https://github.com/compchem-cybertraining/Tutorials_DFTB_plus)

    Make sure to download the parameters files and change kernel to `libra-latest`

  * [QE, Jupyter demonstration](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/2_nbra_workflows/1_step1_qe/tutorial.ipynb)

    Make sure to download the PP files and change kernel to `libra-latest`

  * [QE, Jupyter demonstration](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/2_nbra_workflows/3_step2_qe/tutorial.ipynb)

    Make sure to download the PP files and change kernel to `libra-latest`
    Make sure to use the absolute path for the pseudopotential dir

  * [QE, command-line and Jupyter examples](https://github.com/compchem-cybertraining/Tutorials_QE_and_eQE/tree/master/7_eqe_nacs)

    Show the NAC calculcations with eQE


### 3.5. Wavepackets and Quantum Trajectories with Adaptive Gaussians (QTAG)

  * [1_gaussian/1_matrix_elements](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/4_wavepackets/1_gaussian/1_matrix_elements/tutorial.ipynb)
   
   computing matrix elements, exercises
 
  * [2_dvr_basics/tutorial](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/4_wavepackets/2_dvr_basics/tutorial.ipynb) 
   and [4_more/Tutorial1](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/4_wavepackets/4_more)

  * [QTAG basics](https://github.com/compchem-cybertraining/Tutorials_Libra/blob/master/6_dynamics/5_qtag/1_basics/tutorial.ipynb)


### 3.6. Exact dynamics via SOFT-DVR

  * [3_soft_propagation/tutorial](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/4_wavepackets/3_soft_propagation/tutorial.ipynb)

   the wrapped up SOFT simulation and cool visualization


### 3.7. Hierarchical Equations of Motion (HEOM)

  * [HEOM tutorial](https://github.com/compchem-cybertraining/Tutorials_Libra/tree/master/6_dynamics/3_heom/1_dynamics_and_lineshapes/tutorial.ipynb)


### 3.8. Auxiliary methods for computational chemistry codes

  To be Added 

   