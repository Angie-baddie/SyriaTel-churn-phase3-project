# SyriaTel-churn-phase3-project
# SyriaTel Customer Churn – Phase 3 Classification Project

## Overview
Goal: predict *customer churn* (0=stay, 1=churn) to help SyriaTel target retention actions.

## Business & Data Understanding
- *Stakeholder:* SyriaTel (telecom) — wants to reduce churn costs.
- *Dataset:* ~3.3k customer records, usage/plan/customer-service features, labeled churn.
- *Target:* churn (binary).

## Modeling (Iterative)
1. *Baseline:* Logistic Regression (scaled numeric, encoded categorical).  
2. *Nonparametric:* Decision Tree.  
3. *Tuning:* class weights / hyperparameters; compared on *test* ROC AUC, F1, accuracy.

## Evaluation (Test set)
- *Primary metric:* ROC AUC (class-imbalance-aware) + F1.
- (Insert your actual numbers here)

## Key Insights
- Top churn drivers (examples): international_plan, customer_service_calls, total_day_minutes.
- LR coefficients (±) indicate risk direction; Tree importances show split strength.

## Recommendations
- Proactively reach out to high-risk segments (intl plan + many service calls).
- Consider retention offers and service quality improvements for those segments.

## Files
- Phase3_churn_project.ipynb – full analysis notebook
- notebook.pdf – PDF export of the notebook
- presentation.pdf – non-technical slides for stakeholders

## How to Reproduce
```bash
# Python 3.10+ recommended
pip install -r requirements.txt  # (if provided)
# Or install: pandas, numpy, scikit-learn, matplotlib, seaborn
# Open the notebook
jupyter notebook Phase3_churn_project.ipynb
