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

###  Numerical Experiments on GBM and NS Data

The experiments were carried out on two representative time-series datasets:

- **Geometric Brownian Motion (GBM):** 
  A stochastic process following  

  
  $$dX_t = \mu X_t\,dt + \sigma X_t\,dW_t$$
  

  simulated as  

  
  $$X_t = X_0 \exp\left((\mu - \tfrac{1}{2}\sigma^2)t + \sigma W_t\right)$$
  

  modeling multiplicative noise dynamics commonly used in financial contexts.

- **Noisy Sinusoidal Data (NS):**  
  Deterministic sinusoidal signals perturbed by Gaussian noise.

  $$y_i = \sin(x_i) + \varepsilon_i \text{ with }  \varepsilon_i \sim \mathcal{N}(0, \sigma_{\varepsilon}^2)$$
  

Both datasets were used to evaluate and compare the performance of **GPR** and **NPSR** under varying:
- Sample sizes \(M\),
- Discretization levels \(N\),
- Signature truncation depths.

Model performance was quantified via **Root Mean Square Error (RMSE)** and complemented by a **condition number analysis** to assess numerical stability.  
Empirically:
- **NPSR** demonstrated flexibility but increased sensitivity to conditioning at higher signature truncations.  
- **Signature-kernel GPR** achieved smoother convergence and provided uncertainty quantification via posterior variance estimates.

---

###  Analysis and Visualization

The notebooks include:
- **RMSE convergence analysis**  
- **Condition number analysis**
- **Multiple plots** visualizing intermediate steps and convergence behavior

---

###  Context

These notebooks complement a **theoretical review on signature-based regression**, providing numerical insights and empirical validation of the discussed algorithms.
