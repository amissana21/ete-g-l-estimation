# L-Estimation for the Enriched Truncated Exponentiated Generalized (ETE-G) Family of Distributions

## Overview

This repository contains the Python implementation for the dissertation:

**"L-Estimation Methods for the Enriched Truncated Exponentiated Generalized Family of Distributions with Applications to Insurance Loss Modeling"**

by **Amina Issoufou Anaroua**, PhD Candidate in Big Data Analytics  
University of Central Florida, Spring 2026  
Advisor: Dr. Chudamani Poudyal

## Research Summary

This work develops robust L-estimation methods for the ETE-G family of distributions, extending Kumaraswamy-weighted L-estimation frameworks to the complex ETELL (ETE-Log-Logistic) and ETELN (ETE-Lognormal) models. The proposed L-estimators achieve near-optimal asymptotic relative efficiency (ARE up to 0.999) while maintaining superior robustness compared to Maximum Likelihood Estimation (MLE), particularly in the presence of extreme outliers.

### Key Contributions

- Extension of L-estimation techniques to the ETELL and ETELN distribution families
- Two estimation designs: **Design A** (same J, J₁ = J₂) and **Design B** (different J, J₁ ≠ J₂)
- Comprehensive Monte Carlo simulation studies comparing L-estimators with MLE
- Demonstration of L-estimator stability under data contamination where MLE fails catastrophically
- Application to Norwegian fire insurance claims data with risk measures (VaR, TVaR) calculations
- Evidence that L-estimators produce reliable, regulatory-compliant risk measures even with extreme outliers

## Repository Structure

```
ete-g-l-estimation/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── etell/                              # ETE-Log-Logistic distribution
│   ├── README.md
│   ├── design_a/                       # Design A: Same J (J₁ = J₂)
│   │   ├── 01_ARE.ipynb                    # Asymptotic Relative Efficiency tables
│   │   ├── 02_Simulation.ipynb             # Monte Carlo simulation study
│   │   ├── 03_Real_Data.ipynb              # Norwegian fire insurance analysis
│   │   ├── 04_Risk_Measures.ipynb          # VaR and TVaR calculations
│   │   └── 05_Contamination_Study.ipynb    # Robustness under contamination
│   │
│   └── design_b/                       # Design B: Different J (J₁ ≠ J₂)
│       ├── 01_ARE.ipynb                    # Asymptotic Relative Efficiency tables
│       ├── 02_Simulation.ipynb             # Monte Carlo simulation study
│       ├── 03_Real_Data.ipynb              # Norwegian fire insurance analysis
│       └── 04_Risk_Measures.ipynb          # VaR and TVaR calculations
│
├── eteln/                              # ETE-Lognormal distribution
│   ├── README.md
│   ├── 01_ARE.ipynb                        # ARE tables (both designs)
│   ├── 02_Simulation.ipynb                 # Monte Carlo simulation (both designs)
│   ├── 03_Real_Data.ipynb                  # Norwegian fire insurance analysis (both designs)
│   └── 04_Risk_Measures.ipynb              # VaR and TVaR calculations (both designs)
│
└── data/
    └── README.md                       # Data source information
```

## Notebook Descriptions

Each distribution folder contains notebooks numbered in the recommended order of execution:

| # | Notebook | Description |
|---|----------|-------------|
| 01 | **ARE** | Computes Asymptotic Relative Efficiency of L-estimators vs. MLE using Gauss-Legendre quadrature |
| 02 | **Simulation** | Monte Carlo simulation studies comparing L-estimator and MLE performance across sample sizes |
| 03 | **Real Data** | Parameter estimation on Norwegian fire insurance claims (original and contaminated datasets) |
| 04 | **Risk Measures** | Value-at-Risk (VaR) and Tail Value-at-Risk (TVaR) computation and comparison |
| 05 | **Contamination Study** | *(ETELL Design A only)* Robustness analysis under tail-extrapolation contamination |

## Estimation Designs

- **Design A (Same J):** Uses J₁ = J₂ in the Kumaraswamy weight functions with different score functions h
- **Design B (Different J):** Uses J₁ ≠ J₂ with the same score function h = log(x)

For ETELL, each design has its own set of notebooks. For ETELN, both designs are contained within each notebook.

## Methods

- **L-Estimation**: Robust parameter estimation using Kumaraswamy-weighted L-moments
- **Maximum Likelihood Estimation (MLE)**: Standard benchmark estimation method
- **Monte Carlo Simulation**: Parallel simulation studies for comparing estimator performance
- **Gauss-Legendre Quadrature**: Numerical integration for implicit estimation equations
- **Asymptotic Theory**: Efficiency computation via the Implicit Function Theorem
- **Risk Measures**: Value-at-Risk (VaR) and Tail Value-at-Risk (TVaR) at standard regulatory levels

## Data

The real data application uses **Norwegian fire insurance claims**, a standard benchmark dataset in actuarial science for modeling heavy-tailed loss distributions. See `data/` for details.

## Requirements

- Python 3.8+
- See `requirements.txt` for package dependencies
- Notebooks were developed and tested in Google Colab

## Installation

```bash
git clone https://github.com/amissana21/ete-g-l-estimation.git
cd ete-g-l-estimation
pip install -r requirements.txt
```

## Citation

If you use this code, please cite:

```
Issoufou Anaroua, A. (2026). L-Estimation Methods for the Enriched Truncated Exponentiated 
Generalized Family of Distributions with Applications to Insurance Loss Modeling. 
PhD Dissertation, University of Central Florida.
```

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Contact

- **Author**: Amina Issoufou Anaroua
- **University**: University of Central Florida, Department of Statistics and Data Science
- **Advisor**: Dr. Chudamani Poudyal
