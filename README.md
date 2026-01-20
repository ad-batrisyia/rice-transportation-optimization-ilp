# Rice Transportation Cost Optimization Using Integer Linear Programming (ILP)

## 📘 Overview
This project presents a **transportation optimization model** that minimizes the total
cost of distributing processed rice from multiple rice mills to centralized warehouses
in Northern Peninsular Malaysia.

The model is inspired by the structure of Malaysia’s rice supply chain and applies
**Integer Linear Programming (ILP)** to derive a feasible and near-optimal transportation plan
under supply and demand constraints.

---

## 🎯 Problem Definition
The distribution network consists of:
- **6 rice mills** (supply nodes)
- **3 warehouses** (demand nodes)

The optimization objectives are to:
- Minimize total transportation cost
- Satisfy all warehouse demand requirements
- Comply with the supply limits at each rice mill
- ROute rice only through feasible cost-defined connections

---

## 🧮 Methodology
- **Model Type:** Transportation Problem (ILP)
- **Decision Variables:** Quantity transported from each rice mill to each warehouse
- **Objective Function:** Minimize total transportation cost (RM)
- **Constraints:** Supply, demand, and non-negativity

### Initial Feasible Solutions
- Northwest Corner Method (NWC)
- Least Cost Method (LCM)
- Vogel’s Approximation Method (VAM)

### Optimization Tool
- **Excel Solver (Simplex Method)**

---

## 🔍 Scenario Analysis
Two disruption scenarios were tested:
1. Increase in warehouse demand
2. Reduction in rice mill supply

Unbalanced cases were handled by introducing dummy supply nodes with an
**unmet demand penalty cost of RM600 per ton**, discouraging reliance on unmet demand.

---

## 📊 Key Results

| Scenario | Total Transportation Cost (RM) |
|--------|--------------------------------|
| Base Case (Optimal) | 246,660 |
| Increased Demand | 306,060 |
| Reduced Supply | 263,460 |

The results show that supply or demand disruptions significantly increase optimal
transportation costs.

---

## 📂 Data Sources & Assumptions
This project uses **estimated and publicly informed data** to simulate a realistic
transportation network.

### Transportation Cost
- Road distances estimated using **Google Maps**
- Cost assumed at **RM3 per kilometer per ton**, reflecting inland freight charges
- Cost matrix represents realistic relative costs, not actual contractual rates

### Supply Estimation
- Total supply assumed at **1,000 tons** (balanced model)
- Supply proportions informed by **USDA Rice Explorer** paddy production statistics

### Demand Estimation
- Warehouses assumed to be centralized in **Seberang Perai, Penang**
- Demand distributed approximately as **350 – 300 – 350 tons**, allowing minor variation
  based on assumed warehouse capacity

> All values are intended for modeling and scenario analysis purposes.

---

## 🛠 Tools & Skills
- Integer Linear Programming (ILP)
- Transportation Models
- Excel Solver (Simplex Method)
- Scenario & Sensitivity Analysis
- Supply Chain Optimization

---

## 📁 Repository Content
- `README.md` – Project overview, methodology, assumptions, and results summary
- `slides/` – [Detailed explanation of the model, formulation, and findings](slides/rice_transportation_optimization.pdf)
- `model/` – [Excel Solver implementation containing data, assumptions, and scenario analysis](model/transportation_optimization_model.xlsx)

---

## ⚠ Disclaimer
This project is a conceptual case study for analytical and modeling purposes and does
not represent operational data or decisions of BERNAS.



