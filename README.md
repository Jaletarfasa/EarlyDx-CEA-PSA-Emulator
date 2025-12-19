# 📊 Early Diagnosis Cost-Effectiveness Model (CEA + PSA + Emulator)

This repository contains a **decision-analytic health economic model** evaluating an early cancer diagnosis intervention using:

- Cost-Effectiveness Analysis (CEA)
- Probabilistic Sensitivity Analysis (PSA, Monte Carlo)
- A **machine-learning emulator** (R-only, xgboost) for rapid policy exploration

All results are generated using **synthetic simulation data** produced by the model itself.  
**No patient-level or confidential data are used.**

---

## 🔬 What the model does

The model compares two strategies:

- **Standard diagnosis**
- **Early diagnosis intervention**

For each strategy, the model simulates:

- Diagnosis stage (early vs late)
- Survival time
- Costs
- Quality-Adjusted Life Years (QALYs)

### Key outputs

- Incremental costs (ΔC)
- Incremental QALYs (ΔQ)
- ICER (ratio of means)
- Probability of cost-effectiveness
- CEAC and PSA diagnostics

---

## 🤖 ML Emulator (R-only)

To enable rapid scenario testing, the repository includes a **machine-learning emulator** that learns the mapping:

**Model inputs → Economic outcomes**

The emulator predicts:

- Mean incremental cost
- Mean incremental QALYs
- Probability of cost-effectiveness

This allows instant *“what-if”* analysis **without rerunning full PSA**, while preserving the structure of the underlying decision model.

---

## 📁 Repository structure

