# Experimentation Readouts: MDE & Power Analysis

## Executive Summary
This repository demonstrates an end-to-end A/B experimentation workflow, focused on how Big Tech economists design, analyze, and communicate experiments for decision-making. The project emphasizes clear readouts, uncertainty quantification, and statistical power, mirroring industry standards used at firms like Amazon and Google.

The core output is a decision-first experiment readout supported by robust statistical analysis, including MDE and power calculations and optional CUPED variance reduction.

**Decision Summary:** The treatment shows a statistically significant positive lift with adequate power; results support rollout subject to guardrail monitoring.

---

## Business Problem
Product and policy changes are frequently evaluated using controlled experiments. Economists must answer not only whether an effect exists, but:

- Is the experiment sufficiently powered?
- What is the minimum detectable effect (MDE)?
- How precise is the estimate (confidence intervals, uncertainty)?
- Can variance be reduced (CUPED)?
- What is the recommended decision given the evidence?

This repository provides a reproducible framework to answer these questions.

---

## Methodology Overview
The analysis follows a standard Big Tech experimentation pipeline:

1. Experimental Design  
   - Treatment vs control groups  
   - Pre-specified MDE and power targets  
   - Guardrail metrics  

2. Statistical Inference  
   - Two-sample tests (means/proportions)  
   - Standard errors and 95% confidence intervals  
   - Lift estimation  

3. Power & MDE Analysis  
   - Sample size vs detectable effect trade-offs  
   - Power curves  

4. Variance Reduction  
   - CUPED implementation using pre-period metrics (optional)  

5. Decision-Focused Readout  
   - Clear summary table  
   - Explicit decision recommendation at the top  

---

## Key Outputs

**Primary Artifacts (Start Here):**

- **Experiment Readout (HTML):**  
  `outputs/experiment_readout_mde_power_cuped.html`  
  A decision-focused experiment handout summarizing treatment effect, CUPED adjustment, MDE, and statistical power.

- **Executive Summary (Markdown):**  
  `outputs/experiment_summary.md`  
  A concise written summary highlighting experimental design, results, and decision implications.

- **Experiment Readout Table:**  
  - Mean(T), Mean(C)  
  - Difference and standard error  
  - 95% confidence interval  
  - Lift (%)  
  - Power  
  - CUPED applied (Yes/No)  

- MDE & Power Calculator  
  - Interactive notebook for scenario analysis  

- Visualization  
  - Lift and confidence interval plots  

---

## Repository Structure
```
Experimentation-Readout-MDE-Power/
│
├── README.md
├── data/
│   └── ab_synthetic.csv
│
├── notebooks/
│   ├── 01_ab_readout.ipynb
│   └── 02_mde_power_calculator.ipynb
│
├── outputs/
│   ├── readout_table.csv
│   └── lift_plot.png
│
└── LICENSE
```

---

## Tools & Stack
- Python  
- NumPy, pandas  
- scipy / statsmodels  
- matplotlib  
- Jupyter Notebook  

---

## How to Use
1. Open `notebooks/01_ab_readout.ipynb` to view the experiment analysis and readout.  
2. Open `notebooks/02_mde_power_calculator.ipynb` to explore MDE and power trade-offs.  
3. Review `outputs/` for generated tables and plots.

---

## Key Takeaways
- Emphasis on interpretability and decision-making, not just statistical significance  
- Clear separation between analysis and business recommendation  
- Reproducible and extensible framework suitable for real-world experimentation  

---

## Disclaimer
All data used in this repository is synthetic and created solely for demonstration purposes.

---

## Author
**Vamakshi Chaturvedi**  
Economist | Experimentation & Causal Inference
