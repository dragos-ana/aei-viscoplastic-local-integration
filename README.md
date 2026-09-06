# An Adaptive Strategy for Initial Estimates in the Local Newton–Raphson Integration of (Visco)plasticity Models

This repository provides the 4C input files utilized to reproduce the data presented in: 

*D. C. Ana, C. P. Schmidt, W. A. Wall, An Adaptive Strategy for Initial Estimates in the Local Newton–Raphson Integration of (Visco)plasticity Models (submitted as a preprint)*.

The utilized 4C code is available [here](https://github.com/dragos-ana/4C/tree/add-analysis-suite-for-viscoplast-model-split).

## Structure of the repository
The repository consists of 6 directories containing data from the monotonic loading and non-monotonic loading studies, at the constant logarithmic rates



$$
\dot{\varepsilon} \in \{ 0.001 \ \text{s}^{-1}, 1 \ \mathrm{s}^{-1}, 1000 \ \mathrm{s}^{-1}  \}.
$$

Inside each directory, the data is split according to the loading conditions applied: uniaxial tension, plane stress shear, and tension--shear (combined-loading).
Each of these subdirectories contains data for each of the initialization strategies:
 
- R: reference elastic predictor initialization

- IC: $I_{\mathrm{const}}$  variant of the adaptive estimate interpolation, using constant starting points

- IH: $I_{\mathrm{history}}$ variant of the adaptive estimate interpolation, using history-inferred starting points


At the corresponding directory level, each method directory contains data for the computational efficiency and for the numerical robustness studies. 

The naming of input files  `*_0.4C.yaml` is based on the utilized time step, where `*d*` stands for *dot*, i.e., `0d001s_0.4C.yaml` corresponds to the input file employing $\Delta t = 0.001 \ \mathrm{s}$. 
Input files for failing time steps, i.e., time steps that are higher than the maximum enabled time step sizes presented in the paper, are also contained within this repository.

