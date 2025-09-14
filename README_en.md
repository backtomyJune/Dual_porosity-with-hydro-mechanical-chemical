<p align="center">
  <a href="https://github.com/backtomyJune/Dual_porosity-with-hydro-mechanical-chemical/">中文</a>
  ｜
  English
</p>

# Dual_porosity-with-hydro-mechanical-chemical
DP and H-M-C Multi-Field Coupling Solver Platform for Cohesive Soil

# DP-HMC Coupling Simulator: Service Life Prediction for Bentonite-Based Anti-Seepage Materials
## Project Overview
This project aims to develop a numerical simulation platform based on the Dual-Porosity (DP) model and coupled Hydro-Mechanical-Chemical (HMC) processes.

- The core objective is to tackle the key industry challenges of unclear performance degradation mechanisms and inaccurate long-term life prediction for bentonite-based anti-seepage materials under complex multi-physical field coupling service environments.
- The solver can simulate fluid flow, solute transport, mechanical deformation,and their coupled interactions.
- Due to funding requirements, only part of the code is open-sourced for reference and learning.
  
If this project is helpful to you :thumbsup:, please give it a Star :star: in the upper right corner to show your support!! Thank you!!
## Current Research Progress
Currently, the development of the core modules of the simulator has been completed:
### :white_check_mark: Implemented Features:
### 1. Advection-Dispersion Equation Solver (ADE Solver)
Used to simulate solute transport processes in single-porosity media.
### 2. Dual-Porosity / Two-Domain Model Solver (DP Solver)
Aimed at media like bentonite-based anti-seepage materials with significant macro-micro pore characteristics. It implements mass exchange between mobile and immobile zones, more accurately capturing non-Fickian diffusion and time-dependent retardation effects in solute transport.
### 3. COMSOL Secondary Development & Parametric Modeling
Parametric modeling for COMSOL using Python based on the open-source mph library (https://mph.readthedocs.io/en/1.2/). The construction of random 2D porous media models has been completed.
### 4. Integrated Machine Learning Model for Service Life Prediction: Extreme Gradient Boosting (XGBoost)
Based on the XGBoost integrated ML model, time series analysis is incorporated to analyze the impact of DP+HMC multi-physical field coupling on the service life of bentonite-based anti-seepage materials.

## :children_crossing: Work in Progress
### 1. DP+HMC Full Coupling Framework Extension
Building upon the existing solute transport (Chemical field, C) module, control equations for the Hydraulic field (H) (e.g., fluid flow) and Mechanical field (M) (e.g., stress, deformation) are being integrated.
The goal is to ultimately achieve a truly fully coupled Hydro-Mechanical-Chemical solver to simulate the complex processes experienced by bentonite-based anti-seepage materials in practical engineering scenarios (e.g., chemical erosion).

### 2. Extending Secondary Development Model Content
Planning to develop a user interaction UI interface and related programs.

### 3. Extending Other Ensemble Deep Learning and Machine Learning Models
Planned models to be integrated include:
Light Gradient Boosting Machine (LightGBM), Adaptive Boosting (AdaBoost), Random Forest (RF).

## Technology Stack
- Simulation Software: COMSOL Multiphysics 6.2
- Development Tools/Language: Python 3.9 (Key libraries: scikit-learn, numpy, pandas, Matplotlib, etc.), PyCharm 2024

## Future Directions
- Complete the development and validation of the full HMC coupled solver.
- Introduce machine learning methods (such as Physics-Informed Neural Networks - PINNs, surrogate modeling) for accelerated computation, parameter inversion, and uncertainty quantification.
- Develop advanced application cases and life prediction toolchains for specific engineering scenarios (e.g., landfill liner/barrier systems near-field environments).
- Develop UI interactive applications.

## Contact Me
- If you have any questions or collaboration intentions, please contact via:
- Email: 2311110061@nbu.edu.cn / 289176263@qq.com

## Acknowledgments
- Thanks to my supervisor and the funding from the National Natural Science Foundation of China (Grant Nos. 42477151; 42107174), the China Postdoctoral Science Foundation (Grant No. 2023M743058), the Key Project of Zhejiang Provincial Natural Science Foundation (LZ25E080009), and the Zhejiang Provincial Postdoctoral Science Foundation (Grant No. ZJ2023111).
- Thanks to Ningbo Zhongchun High-Tech Co., Ltd. for providing the test site.
