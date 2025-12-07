# Beating the Tennis Market with Machine Learning

This project builds a machine learning model to forecast ATP tennis match outcomes and evaluate potential inefficiencies in the betting market. Using ATP match results (2000–2024) and Bet365 odds, the model generates calibrated win probabilities, converts them into fair odds, and identifies positive expected-value (+EV) opportunities.

---

## Overview
- Built Elo-based and surface-adjusted performance features  
- Engineered ranking gaps, head-to-head history, and recent form metrics  
- Trained and tuned multiple ML models (XGBoost, Random Forests, SVM)  
- Selected **XGBoost** for its superior AUC and probability calibration  
- Compared model-generated fair odds to Bet365 prices  
- Flagged matches where market odds appeared mispriced  

---

## Key Features

### Elo Ratings
- Global + surface-specific  
- Updated dynamically with decay  

### Player Form
- Wins in last 5/10 matches  
- Recent win percentage  

### Context Features
- Surface, round, match format, ranking differential  

### Betting Market Comparison
- Converts predicted probabilities into fair odds  
- Computes expected value from sportsbook odds  

---

## Model Performance
- **AUC ≈ 0.73** using 5-fold cross validation  
- Well-calibrated win probabilities  
- Able to highlight match inefficiencies even when not outperforming the market overall  

---

## Files
app.py # real-time match prediction
pred_model.py # model training and evaluation
load_data.py # preprocessing utilities
pred_model.ipynb # notebook with all experiments
figures/ # feature importance and evaluation plots

---

## Next Steps
- Add detailed ATP player stats (serve %, break points, etc.)  
- Test neural networks and hybrid ensembles  
- Run full backtests of betting strategies  
- Integrate additional sportsbook odds  

---

## About
Project completed as part of a computational statistics course.  
My work focused on model development, feature engineering, and EV-based market analysis.
