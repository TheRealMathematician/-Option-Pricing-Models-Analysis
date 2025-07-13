# -Option-Pricing-Models-Analysis

## 📘 Project Overview

This project presents a **comparative analysis of advanced option pricing models**, focusing on the **Heston Stochastic Volatility Model** and the **Merton Jump Diffusion Model**. Both **European and American options** are evaluated using **Monte Carlo simulations**. The work explores how different **market assumptions** (like correlation and jump intensity) impact pricing, Greeks, and moneyness behavior. This project provides a **robust framework** for understanding and comparing **advanced option pricing models** using real-world assumptions. It not only captures the theoretical mechanics of Heston and Merton models but also translates them into **practical pricing insights** using Python and Monte Carlo methods.

> 📚 Completed as part of a financial modeling curriculum. Designed for research, academic exploration, and practical implementation.

---

## 🧩 Key Components

### 1️⃣ **📈 Model Implementations**

#### ⚙️ **Heston Model (Stochastic Volatility)**

* Applied to **at-the-money (ATM) European options**
* Tested with correlation values: `ρ = -0.30` and `ρ = -0.70`
* Calculated **Greeks**: delta, gamma
* ✅ Verified **put-call parity**
* Analyzed **moneyness effects** within `0.85–1.10` range

#### ⚙️ **Merton Model (Jump Diffusion)**

* Priced European options with **jump intensities**: `λ = 0.25` and `λ = 0.75`
* Computed **Greeks** and examined **price impact of jumps**
* Verified **put-call parity**
* Evaluated pricing across **different strike levels**

#### 🧾 **American Options**

* Compared pricing with equivalent **European options**
* Demonstrated the **early exercise premium**

#### 💥 **Exotic Options**

* Priced **European Up-and-In (UAI) Call Options**
* Valued **European Down-and-In (DAI) Put Options**
* Highlighted **barrier dependency** in exotic pricing

---

### 2️⃣ **🔍 Key Findings**

#### 💲 **Pricing Comparisons**

* **Heston Model (ATM Options)**

  * ρ = -0.30: Call = `2.87`, Put = `2.89`
  * ρ = -0.70: Call = `2.07`, Put = `3.47`
* **Merton Model (Jump Diffusion)**

  * λ = 0.75: Call = `8.32`, Put = `7.06`
  * λ = 0.25: Call = `6.80`, Put = `5.83`
* **American Options** were consistently priced **higher** due to early exercise capability

#### 🧮 **Greeks Analysis**

* **Gamma** in Heston model showed high sensitivity to changes in **correlation**
* **Delta** in Merton model varied with **jump intensity**
* Overall Greek behavior reflected distinct **volatility mechanics** across models

#### ⚖️ **Moneyness Effects**

* Both models showed **price decay** as strike price increases
* Merton consistently yielded **higher option values** across moneyness
* Heston had steeper decay in **out-of-the-money (OTM)** conditions

#### 🚧 **Exotic Options**

* European UAI Call = `0.2998`
* European DAI Put = `5.3857`
* Illustrated **path dependency** and **barrier activation mechanics**

---

### 3️⃣ **🛠️ Technical Implementation**

#### **📊 Methodology**

* **Monte Carlo Simulations** (10,000+ paths)
* **Stochastic Volatility Modeling** (Heston)
* **Jump Diffusion Processes** (Merton)
* **Barrier Option Pricing** with path tracking

#### **✅ Validation**

* Put-call parity tested for both models
* Monte Carlo convergence confirmed
* Cross-model comparisons for robustness

#### **📈 Numerical Results**

* Confirmed **put-call parity** holds across pricing models
* Quantified **early exercise premium** for American options
* Measured **sensitivity to volatility, correlation, and jumps**

---

## 🗂️ Repository Structure

```
/project
│── /notebooks
│   ├── heston_model.ipynb          # Heston pricing & Greeks
│   ├── merton_model.ipynb          # Merton jump diffusion model
│   └── american_exotics.ipynb      # American & barrier option pricing
│── /data
│   ├── parameters.json             # Model parameters
│   └── results.csv                 # Output pricing data
│── /docs
│   └── methodology.pdf             # Full documentation
├── README.md
└── requirements.txt
```

## 🚀 Future Work

1. 📈 Extend models to **multi-asset options** (e.g., basket or rainbow options)
2. 🧮 Implement **control variates** for better variance reduction in simulations
3. 📉 Add **local volatility surfaces** for more realistic modeling
4. 📊 Develop **real-time dashboard** for live option pricing and visualization
5. 🤖 Incorporate **machine learning** for parameter calibration and volatility forecasting





