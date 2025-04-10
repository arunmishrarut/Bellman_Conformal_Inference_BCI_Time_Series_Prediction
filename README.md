# Bellman Conformal Inference (BCI) – Time Series Prediction

Overview:

This project reproduces the results from the research paper:
"Bellman Conformal Inference: Calibrating Prediction Intervals for Time Series" by Yang et al. (2024).
The paper introduces Bellman Conformal Inference (BCI), an extension of Adaptive Conformal Inference (ACI), which dynamically calibrates multi-step ahead prediction intervals using stochastic control techniques.

Core Concepts:

Conformal Inference: Distribution-free method to generate prediction intervals

ACI: Adapts intervals based on past coverage errors (gradient descent-style)

BCI: Optimizes interval length + coverage using Bellman's equation and Model Predictive Control (MPC)

⚙Models & Implementation:

Reproduced Models from the paper:

ARMA-GARCH(1,1) for stock return volatility (Microsoft stock via Yahoo Finance)

Transformer-based model for returns

LSTM for Google Trends (keyword: "deep learning")

Interval methods compared:

Fixed-width

ACI

BCI (main contribution)

Reproduction Setup:

Config files modified to include ACI, BCI, and Fixed models

Miscoverage rates (β) computed using z-scores

Evaluation at multiple confidence levels: 95%, 80%, 50%

Key Results:

BCI outperforms ACI in maintaining coverage while minimizing average interval length

BCI avoids infinite-length intervals, which were observed in ACI under tight constraints

Results are consistent with findings reported by Yang et al. (2024)

⚠Limitations:

BCI has higher computational complexity due to dynamic optimization

Difficult to tune for datasets with high volatility or noise

Reproduction may vary slightly with different random seeds and window sizes

📚 References

📄 Original Paper – Yang et al., 2024

Gibbs & Candès (2021) – Adaptive Conformal Inference under Distribution Shift

Xu & Xie (2021), Sun & Yu (2023) – Extensions of conformal methods in time serie
