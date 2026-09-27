# 🏠 House Price Predictor

Predicting median house values in California districts using Linear Regression, built as an end-to-end supervised learning workflow: data loading, train/test split, model training, evaluation and visualization.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lidiyajohnson07/House-price-predictor/blob/main/House_price_predictor.ipynb)

## 📌 Problem
Given information about a housing district (median income, house age, average rooms, population, location, etc.), predict the district's median house value. This is a **regression** task.

## 📂 Dataset
- **California Housing** dataset (loaded via `sklearn.datasets.fetch_california_housing`)
- 20,640 samples, 8 numerical features
- Target: median house value (in units of $100,000)

## ⚙️ Approach
1. Loaded the data into a pandas DataFrame
2. Split into 80% training and 20% test data (`random_state=42` for reproducibility)
3. Trained a **Linear Regression** model with scikit-learn
4. Evaluated on the unseen test set
5. Plotted actual vs. predicted prices to inspect errors

## 📊 Results
| Metric | Value |
|---|---|
| Mean Squared Error (test set) | 0.56 |
| Root Mean Squared Error | ≈ 0.75 (≈ $75,000) |

The actual-vs-predicted plot shows the model captures the overall trend but underestimates the most expensive houses, since the dataset caps values at $500,000 and a linear model cannot capture non-linear effects.

## 🔭 Possible Improvements
- Feature scaling and feature engineering
- Non-linear models (e.g., Random Forest, Gradient Boosting)
- Cross-validation and additional metrics (R², MAE)

## 🛠️ Tools
Python · pandas · scikit-learn · matplotlib · Google Colab

## ▶️ How to Run
Click the **Open in Colab** badge above and run all cells. No local setup needed.

## 👩‍💻 Author
**Lidiya Johnson**, M.Sc. Computational Engineering, FAU Erlangen-Nürnberg
GitHub: [@Lidiyajohnson07](https://github.com/Lidiyajohnson07)

