# L-Estimation for the Enriched Truncated Exponentiated Generalized (ETE-G) Family of Distributions

## Overview

This repository contains the Python implementation for the dissertation:

**"L-Estimation Methods for the Enriched Truncated Exponentiated Generalized Family of Distributions with Applications to Insurance Loss Modeling"**

by **Amina Issoufou Anaroua**, PhD Candidate in Big Data Analytics  
University of Central Florida, Spring 2026  
Advisor: Dr. Chudamani Poudyal

## Research Summary

This work develops robust L-estimation methods for the ETE-G family of distributions, extending Kumaraswamy-weighted L-estimation frameworks to the complex ETELL (ETE-Log-Logistic) and ETELN (ETE-Lognormal) models. The proposed L-estimators achieve near-optimal asymptotic relative efficiency (up to 0.999) while maintaining superior robustness compared to Maximum Likelihood Estimation (MLE), particularly in the presence of extreme outliers.

### Key Contributions

- Extension of L-estimation techniques to the ETELL and ETELN distribution families
- Comprehensive Monte Carlo simulation studies comparing L-estimators with MLE
- Demonstration of L-estimator stability under data contamination where MLE fails catastrophically
- Application to Norwegian fire insurance claims data with risk measures (VaR, TVaR) calculations
- Evidence that L-estimators produce reliable, regulatory-compliant risk measures even with extreme outliers

## Repository Structure

```
├── README.md
├── requirements.txt
├── data/
│   └── norwegian_fire_insurance.csv
├── etell/
│   ├── etell_estimation.py          # ETELL parameter estimation (MLE & L-estimation)
│   ├── etell_simulation.py          # Monte Carlo simulation studies for ETELL
│   ├── etell_risk_measures.py       # VaR and TVaR calculations for ETELL
│   └── etell_contamination.py       # Contamination/robustness studies for ETELL
├── eteln/
│   ├── eteln_estimation.py          # ETELN parameter estimation (MLE & L-estimation)
│   ├── eteln_simulation.py          # Monte Carlo simulation studies for ETELN
│   ├── eteln_risk_measures.py       # VaR and TVaR calculations for ETELN
│   └── eteln_contamination.py       # Contamination/robustness studies for ETELN
├── common/
│   ├── quadrature.py                # Gauss-Legendre quadrature utilities
│   ├── distributions.py             # ETE-G distribution functions (PDF, CDF, quantile)
│   └── utils.py                     # Shared helper functions
├── figures/
│   └── ...                          # Generated plots and visualizations
└── results/
    └── ...                          # Simulation output tables and summaries
```

## Methods

- **L-Estimation**: Robust parameter estimation using Kumaraswamy-weighted L-moments
- **Maximum Likelihood Estimation (MLE)**: Standard benchmark estimation method
- **Monte Carlo Simulation**: Parallel simulation studies for comparing estimator performance
- **Numerical Integration**: Gauss-Legendre quadrature for implicit estimation equations
- **Risk Measures**: Value-at-Risk (VaR) and Tail Value-at-Risk (TVaR) computation

## Requirements

- Python 3.8+
- See `requirements.txt` for package dependencies

## Installation

```bash
git clone https://github.com/amissana21/ete-g-l-estimation.git
cd ete-g-l-estimation
pip install -r requirements.txt
```

## Usage

```python
# Example: Run ETELL parameter estimation on Norwegian fire data
python etell/etell_estimation.py

# Example: Run Monte Carlo simulation for ETELN
python eteln/eteln_simulation.py
```

## Data

The real data application uses **Norwegian fire insurance claims** data, a standard benchmark dataset in actuarial science for modeling heavy-tailed loss distributions.

## Citation

If you use this code, please cite:

```
Issoufou Anaroua, Amina. (2026). L-Estimation Methods for the Enriched Truncated Exponentiated 
Generalized Family of Distributions with Applications to Insurance Loss Modeling. 
PhD Dissertation, University of Central Florida.
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

- **Email**: amissana21@gmail.com
- **University**: University of Central Florida, Department of Statistics and Data Science
- **Advisor**: Dr. Chudamani Poudyal
