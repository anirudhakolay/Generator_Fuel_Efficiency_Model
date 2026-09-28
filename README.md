# 🚢 Offshore Generator Energy Efficiency & Fuel Optimization

> **Data Science & ML Engineering Case Study**: Predictive Daily Diesel Fuel Consumption Modeling and Constrained Load Optimization for Offshore Oil Platforms.

---

## 📌 Project Overview
Offshore oil & gas platforms operate heavy diesel generators ($G_1, G_2, G_3, G_4$) to support dynamic power loads. Fuel consumption is a major operating expense and primary source of $CO_2$ emissions.

This project delivers an end-to-end data-driven solution:
1. **Predictive Modeling:** High-precision Machine Learning regression to predict `daily_diesel_consumption_litres` ($R^2 = 99.51\%$, $\text{MAE} = 15.61$ L/day).
2. **Prescriptive Optimization:** Constrained load allocation optimization to identify minimum-fuel generator loading combinations $(L_1, L_2, L_3, L_4)$ for any given power demand.

---

## 📊 Dataset & Generator Specifications
* **Dataset Size:** 15,057 daily logs $\times$ 18 features.
* **Target Variable:** `daily_diesel_consumption_litres` (Mean: 4,960.7 L/day).
* **Installed Platform Capacity:**
  * **$G_1, G_2$:** 1,200 kW Max Capacity each.
  * **$G_3, G_4$:** 1,000 kW Max Capacity each.
  * **Total Capacity:** 4,400 kW.

---

## 📈 Model Performance Benchmark

| Model | $R^2$ Score | MAE (Litres/day) | RMSE (Litres/day) | MAPE (%) | Key Finding |
| :--- | :---: | :---: | :---: | :---: | :--- |
| 🥇 **Random Forest (Tuned)** | **`0.9951`** | **`15.61 L`** | **`28.74 L`** | **`0.31%`** | 🏆 **Top Model:** Accurately models non-linear BSFC engine curves. |
| 🥈 **Decision Tree** | `0.9856` | `28.21 L` | `48.51 L` | `0.57%` | High accuracy, slightly higher prediction variance. |
| 🥉 **HistGradientBoosting** | `0.9427` | `74.97 L` | `97.91 L` | `1.51%` | Solid non-linear model. |
| ❌ **Linear Regression** | `0.7387` | `165.71 L` | `209.03 L` | `3.42%` | ⚠️ Fails due to linear assumption over non-linear engine curves. |
| ❌ **Ridge Regression** | `0.7387` | `165.71 L` | `209.03 L` | `3.42%` | ⚠️ Fails due to linear assumption over non-linear engine curves. |

---

## 💡 Key Business & Operational ROI
* **Daily Diesel Savings:** $\sim 150 - 250$ Litres/day saved ($3\% - 5\%$ fuel reduction).
* **Annual Financial Impact:** **$\sim \$73,000$ saved per year** per platform.
* **Environmental Carbon Impact:** **$\sim 190$ Metric Tons of $CO_2$ reduced** per year.

---

## 🛠️ Environment Setup & Quick Start

```bash
# 1. Clone repository
git clone https://github.com/anirudhakolay/Generator_Fuel_Efficiency_Model.git
cd Generator_Fuel_Efficiency_Model

# 2. Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate

# 3. Install required packages
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter

# 4. Launch Jupyter Notebook
jupyter notebook Generator_Efficiency_EDA_and_Optimization.ipynb
```

---

## 📁 Repository Structure
```
├── Generator_Efficiency_EDA_and_Optimization.ipynb  # Main End-to-End Case Study Notebook
├── oil_platform_generator_optimization_synthetic_15057.csv # Offshore Platform Dataset
├── README.md                                         # Project Documentation
└── .gitignore                                        # Ignored files
```
