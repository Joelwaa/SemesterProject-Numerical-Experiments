##  Numerical Experiments for Time Series Forecasting

This repository contains Jupyter notebooks implementing two **time series forecasting algorithms** based on signature methods:

1. **Gaussian Process Regression (GPR)**
2. **Nonparametric Signature Regression (NPSR)**

---

###  Implementation Details

- **GPR:**  
  Includes a *custom signature kernel* implementation using standard **[scikit-learn](https://scikit-learn.org/)** libraries.

- **NPSR:**  
  Implements *Algorithm I* from the paper:  
  [Nonparametric Signature Regression — Blaser et al., 2023 (SAM Report 2023-45)](https://www.sam.math.ethz.ch/sam_reports/reports_final/reports2023/2023-45_rev1.pdf)

---

###  Analysis and Visualization

The notebooks include:
- **RMSE convergence analysis**  
- **Condition number analysis**
- **Multiple plots** visualizing intermediate steps and convergence behavior

---

###  Context

These notebooks complement a **theoretical review on signature-based regression**, providing numerical insights and empirical validation of the discussed algorithms.
