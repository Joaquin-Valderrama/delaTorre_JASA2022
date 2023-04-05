# delaTorre_JASA2022
Supplementary materials (SuppPub2) for "de la Torre et al. (2022)".

SUBSPACE CONSTRAINED DECONVOLUTION OF AUDITORY EVOKED POTENTIALS
Angel de la Torre, Joaquin T Valderrama, Jose C Segura, Isaac M Alvarez

DESCRIPTION OF THE SIMULATIONS

This Readme.txt file describes how to run simulations related to the
subspace-constrained deconvolution of auditory evoked potentials.

Background:

* The "latency-dependent filtering and down-sampling" (LDFDS) mrethod provides
a transformation of the representation space that provides an appropriate
representation of the evoked responses with a significant reduction of
the dimensionality (compared with conventional uniform sampling).
* Subspace-constrained deconvolution proposes to perform the deconvolution
in the reduced representation space provided by LDFDS.
* In this simulations, from a clean AEP response, a noisy EEG is synthesized
and different deconvolution methods are compared:
      - conventional LS deconvolution (LS), 
      - LS deconv. transformed to the reduced representation space (LS-R)
      - and subspace-constrained LS deconv. (SC-LS)
* The methods are implemented with matrix division (RSLSD) and with 
iterative estimation (IRSA).
* This simulation is intended to be run with MatLab or Octave.

The simulation package includes the following files:
- Basis_LinLog_RRC.m   MatLab/Octave function providing the V transformation
- IRSA_LS.m            MatLab/Octave function providing the IRSA-LS deconv.
- IRSA_LSR.m           MatLab/Octave function providing the IRSA-LS-R deconv.
- IRSA_SCLS.m          MatLab/Octave function providing the IRSA-SC-LS deconv.
- RSLSD_LS.m           MatLab/Octave function providing the RSLSD-LS deconv.
- RSLSD_LSR.m          MatLab/Octave function providing the RSLSD-LS-R deconv.
- RSLSD_SCLS.m         MatLab/Octave function providing the RSLSD-SC-LS deconv.
- script_simulation_SCLSDec.m   MatLab/Octave script performing the simulation
- response_30_60_subj1.mat      MatLab/Octave binary file containing the reference AEP
- Readme.txt           This file describing the simulation package.

In order to run the simulation:
Step 1: put all the files in a directory (for example "./Code_demo_SCLSDec/")
Step 2: run MatLab or Octave
Step 3: run "script_simulation_SCLSDec" in the command line

In the case of Octave, if the system ask for the "signal processing package" 
execute the following command in the command line: "pkg load signal".

The users are encouraged to run the simulations and modify the different variables 
(e.g. noise level, length of the response, maximum and minimum ISI, etc.) 
to observe the effect on the deconvolution.

Please note that the outcome of the simulations provided by this script may not 
match exactly the results presented in the paper due to the random nature of 
synthesized noise.

GNU Octave is a high-level language intended for numerical computations with 
a similar synthax as Matlab. GNU Octave is a freely redistributable software, 
and can be downloaded from the following website: https://www.gnu.org/software/octave/.

For questions and comments about these functions and scripts, please 
contact Dr Angel de la Torre Vega (atv@ugr.es) or Dr Joaquin T Valderrama 
(joaquin.valderrama@nal.gov.au).
