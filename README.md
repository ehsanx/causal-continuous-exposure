# Causal Inference with Continuous Exposures: A Tutorial with Application to ICU Data

This repository accompanies the tutorial **"Causal Inference with Continuous Exposures: A Tutorial with Application to ICU Data"**, which demonstrates how to estimate marginal causal effects when the exposure variable is continuous. The tutorial includes both real-world data analysis and a simulation study comparing multiple estimation strategies.

## 📁 Repository Structure

```
├── RHC Analysis        # Real-world data application using the SUPPORT dataset
├── simulation          # Code and results for simulation study
├── LICENSE             # License information 
└── README.md           # This file
```

## 🔍 Description

The tutorial focuses on estimating the effect of a continuous exposure (e.g., blood pressure) on a binary outcome (e.g., in-hospital death) using three causal inference methods:

- **Inverse Probability Weighting (IPW)** assuming a normal exposure model
- **IPW with quantile binning** (distribution-free)
- **Targeted Maximum Likelihood Estimation (TMLE)** with a shift intervention

These methods are implemented and compared in:

- A **real-world ICU dataset** (RHC data from the SUPPORT study)
- A **simulation study** based on a known data-generating mechanism

## 📂 Contents

### 1. `RHC Analysis/`

- Data download, cleaning, and variable coding
- Implementation of the three methods
- Diagnostic checks (weight distributions, covariate balance, exposure overlap)
- Visualizations: distribution plots, forest plots

### 2. `simulation/`

- Simulation of a heteroscedastic continuous exposure
- Comparison of methods using performance metrics (bias, MSE, coverage)
- Summary plots

## 🛠️ Requirements

- R (≥ 4.1.0)
- Required R packages:  
  `tmle3`, `tmle3shift`, `sl3`, `simcausal`, `rsimsum`, `ggplot2`,  
  `dplyr`, `nnet`, `survey`, `MatchIt`, `cobalt`, `Publish`,  
  `tableone`, `patchwork`, `officedown`, `bookdown`

Install packages with:

```r
install.packages(c("ggplot2", "nnet", "survey", "MatchIt", "cobalt",
                   "tableone", "patchwork", "dplyr", "Publish", "rsimsum"))

# From GitHub:
devtools::install_github("tlverse/tmle3")
devtools::install_github("tlverse/tmle3shift")
devtools::install_github("tlverse/sl3")
devtools::install_github("osofr/simcausal")
```

## 🔗 Access the Tutorial

All analysis scripts and data processing workflows are available in this repository.  
For full documentation and reproducible examples, see:

👉 https://github.com/ehsanx/causal-continuous-exposure

## 📄 Citation

If you use this material, please cite:

> Karim, M. E. (2025). *Causal Inference with Continuous Exposures: A Tutorial with Application to ICU Data*. [In submission].

## 📫 Contact

For questions or feedback, please open an [issue](https://github.com/ehsanx/causal-continuous-exposure/issues)  
or reach out to [@ehsanx](https://github.com/ehsanx).
