# 📊 QuantRisk Pro Terminal — Portfolio Analytics & Risk Dashboard

**QuantRisk Pro Terminal** is a single-file, production-grade Web Application designed for investors, portfolio managers, and financial analysts to analyze performance, measure risk exposure, stress test portfolios, and execute strategic rebalancing.

Unlike simple stock trackers that only display asset values, QuantRisk processes real-time transaction data and price histories to deliver institutional-grade portfolio metrics such as **XIRR (via Newton-Raphson method)**, **Sharpe Ratio**, **Annualized Volatility**, **Portfolio Beta**, **Value at Risk (VaR)**, and **Herfindahl Concentration Index (HHI)**.

---

## 🌟 Key Features & Modules

### 1. 📈 Dynamic KPI & Performance Engine
* **Portfolio Value & P&L**: Tracks invested capital vs current market value in real time.
* **XIRR (Annualized Return)**: Implements cashflow-based Extended Internal Rate of Return.
* **Benchmark Comparison**: Real-time relative performance against Nifty 50.

### 2. 🛡️ Quantitative Risk Analytics
* **Sharpe Ratio**: Measures risk-adjusted excess returns over the risk-free rate ($R_f = 6.5\%$).
* **Annualized Volatility ($\sigma$)**: Standard deviation of annualized daily return fluctuations.
* **Portfolio Beta ($\beta$)**: Measures systemic risk sensitivity relative to broad market benchmarks.
* **Value at Risk (VaR 95%)**: Statistically estimates maximum expected single-day loss at a 95% confidence interval.
* **Herfindahl Concentration Index (HHI)**: Quantifies asset concentration to detect over-exposure.
* **Maximum Drawdown**: Measures peak-to-trough historical portfolio declines.

### 3. 🧪 Stress Testing & Scenario Simulator
* **Macro Shock Presets**: Test resilience against standard market crashes, inflation spikes, tech sell-offs, and gold rallies.
* **Interactive Sliders**: Real-time adjustment of Equity, Debt, and Gold yield shocks.
* **Automated Hedging Recommendations**: Actionable strategies to mitigate tail risk during market downturns.

### 4. ⚖️ Modern Portfolio Theory (MPT) Rebalancing Engine
* **Asset Allocation Drift Detection**: Monitors deviations against target weights across Equity, Debt, Gold, ETFs, and Cash.
* **Smart Order Generator**: Automatically computes exact **Buy/Sell** trade orders required to restore target risk exposure.
* **One-Click Rebalance Simulation**: Allows instant theoretical realignment of asset weights.

### 5. 🔔 Automated Smart Risk Alerts
* **Concentration Alerts**: Triggers when any sector exceeds 25% or an individual holding exceeds 18% portfolio weight.
* **Allocation Drift Alerts**: Alerts users when equity allocation strays more than 5% from target ranges.

---

## 📐 Mathematical Formulas & Algorithms

### 1. Extended Internal Rate of Return (XIRR)
Calculated using the **Newton-Raphson** numerical optimization algorithm:
$$NPV(r) = \sum_{i=1}^{N} \frac{C_i}{(1 + r)^{\frac{d_i - d_1}{365.25}}} = 0$$

Iteratively updated until convergence:
$$r_{n+1} = r_n - \frac{NPV(r_n)}{NPV'(r_n)}$$

### 2. Sharpe Ratio
$$\text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}$$
* Where $R_p$ is annualized portfolio return, $R_f$ is risk-free rate ($6.5\%$), and $\sigma_p$ is annualized portfolio volatility.

### 3. Value at Risk (VaR 95%)
$$\text{VaR}_{95\%} = \text{Portfolio Value} \times (1.645 \times \sigma_{\text{daily}})$$

### 4. Herfindahl Index (HHI)
$$\text{HHI} = \sum_{i=1}^{N} w_i^2$$
* Where $w_i$ is the weight of security $i$ in the portfolio. Scores $< 0.15$ indicate optimal diversification.

---

## 🚀 Getting Started

Since the dashboard is built as an **all-in-one single-file application**, no complex build steps, package installations, or Node.js environments are needed.

### Running Locally
1. Download or save `index.html`.
2. Double-click `index.html` to open it in any modern browser (Chrome, Firefox, Edge, Safari).
3. The dashboard will load with pre-filled realistic sample portfolio data.

---

## 🛠️ Tech Stack & Dependencies

* **Frontend**: HTML5, JavaScript (ES6+)
* **Styling**: [Tailwind CSS](https://tailwindcss.com/) (via CDN)
* **Charts**: [Chart.js](https://www.chartjs.org/) (Data Visualizations)
* **Icons**: [FontAwesome 6](https://fontawesome.com/)
* **Data Persistence**: HTML5 `localStorage` (Preserves user custom holdings across reloads)

---

## 📱 Browser & Mobile Compatibility
* Fully responsive layout tailored for desktop terminals, tablets, and mobile devices.
* Dark-mode interface inspired by institutional Bloomberg & Refinitiv trading terminals.