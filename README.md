# Portfolio Optimization & Efficient Frontier Engine



A quantitative financial analytics engine built in Python that models optimal asset allocation using **Markowitz Modern Portfolio Theory (MPT)**. The tool ingests historical market data via `yfinance`, performs Monte Carlo simulations to plot the **Efficient Frontier**, and executes numerical optimization to construct risk-balanced portfolios.

---

## Key Capabilities & Features

* **Dynamic Data Ingestion:** Fetches real-time daily historical prices for customizable stock/ETF selections via `yfinance`.
* **Monte Carlo Simulation:** Simulates 10,000+ randomized portfolio allocations to map out the risk-return spectrum and visually locate the Efficient Frontier.
* **Numerical Optimization (`SciPy`):**
  * **Max Sharpe Ratio Portfolio:** Calculates the exact asset weight allocation that maximizes risk-adjusted returns against a customizable Risk-Free Rate.
  * **Minimum Variance Portfolio (MVP):** Identifies the combination of weights that yields the lowest possible volatility.
* **Dual-Panel Analytics Dashboard:** Generates interactive scatter plots of the Efficient Frontier alongside asset weight breakdown bar charts.
* **Colab Form HUD Integration:** Features user-friendly UI controls (dropdowns, sliders) for real-time scenario testing directly in Google Colab.

---

## Quantitative Framework

The engine operates on the following mathematical core:

1. **Annualized Returns & Risk:**
   $$\mu_p = \sum_{i=1}^{N} w_i \mu_i \quad \text{and} \quad \sigma_p = \sqrt{w^T \Sigma w}$$
   *(where $w$ represents asset weights and $\Sigma$ is the annualized covariance matrix)*

2. **Sharpe Ratio Maximization:**
   $$\text{Sharpe Ratio} = \frac{\mu_p - R_f}{\sigma_p}$$

3. **Constraints:**
   $$\sum_{i=1}^{N} w_i = 1.0 \quad \text{and} \quad 0 \le w_i \le 1 \quad (\text{Long-only constraint})$$

---

## How to Run in Google Colab

1. 
2. Select your desired assets and parameters in the interactive HUD.
3. Run all cells sequentially to generate the optimization report and visual charts.
