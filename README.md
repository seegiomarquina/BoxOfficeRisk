#  BoxOfficeRisk AI
### Movie Box Office Success Classification & Revenue Prediction

**An End-to-End Data Science and Machine Learning Project**

## 1. Project Overview

BoxOfficeRisk AI is a machine learning project designed to analyse historical movie industry data and predict potential box-office performance.

The project combines two predictive systems:

1. **Movie Success Classification** – Classifies movies into Flop, Break-even / Moderate, or Hit.
2. **Box Office Revenue Prediction** – Estimates expected movie revenue using historical production and release characteristics.

It also includes exploratory data analysis, SQL analytics, feature engineering, model comparison, feature importance and interactive predictions.

## 2. Problem Statement

Movie production involves substantial financial uncertainty. A film's budget, genre, runtime, release timing and production characteristics may be associated with its box-office performance.

This project investigates these relationships using historical movie data and machine learning.

## 3. Dataset

**TMDB Box Office Dataset**

Source: https://huggingface.co/datasets/Jesscoyle111/TMDB-box-office

Dataset attributes include:
- Movie title
- Budget
- Revenue
- Genre
- Runtime
- Release date
- Production companies
- Cast
- Director
- Language
- Popularity and ratings

The dataset is loaded directly into Google Colab using Hugging Face Datasets.

Dataset license: CC-BY-NC-SA 4.0, as indicated by the dataset card. Review its terms before redistribution or commercial use.

## 4. Project Objectives

- Analyse historical box-office performance.
- Investigate relationships between budget and revenue.
- Identify genre-level performance patterns.
- Perform SQL-based industry analysis.
- Develop a movie success classification model.
- Develop a revenue prediction model.
- Compare machine learning algorithms.
- Interpret important prediction features.
- Create an interactive movie prediction function.

## 5. Machine Learning Methodology

### Classification

Three project-defined categories:

| Category | Gross Revenue / Budget |
|---|---|
| Flop | Below 1x |
| Break-even / Moderate | 1x to below 2x |
| Hit | 2x or above |

These are analytical categories, not official film-industry classifications.

### Regression

Predicts log-transformed box-office revenue and converts predictions back to the dataset's revenue units.

### Algorithms

**Classification**
- Dummy Classifier
- Random Forest Classifier
- Extra Trees Classifier

**Regression**
- Random Forest Regressor
- Extra Trees Regressor

## 6. Feature Engineering

- Log-transformed production budget
- Runtime
- Release month
- Release year
- Cast count
- Production company count
- Primary genre
- Original language
- Director category

Post-release information such as revenue, ratings, popularity and vote counts is excluded from model inputs.

## 7. Evaluation Metrics

**Classification**
- Accuracy
- Precision
- Recall
- Macro F1-score
- Weighted F1-score
- Confusion Matrix

**Regression**
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared
- Root Mean Squared Logarithmic Error (RMSLE)

Actual experimental results are saved in the reports folder.

## 8. SQL Analytics

SQLite is used to investigate:

- Genre performance
- Annual movie revenue patterns
- Average budget by success category
- Revenue-to-budget comparisons

## 9. Visualizations

- Movie success distribution
- Budget distribution
- Revenue distribution
- Genre performance analysis
- Budget vs Revenue
- Correlation matrix
- Classification confusion matrix
- Actual vs Predicted Revenue
- Classification feature importance
- Regression feature importance

## 10. Repository Structure

```text
BoxOfficeRisk-AI/
│
├── BoxOfficeRisk_AI_Day11.ipynb
├── outputs/
├── models/
├── reports/
├── data/
├── requirements.txt
├── README.md
└── .gitignore
```

## 11. How to Run

1. Open the notebook in Google Colab.
2. Run the complete implementation.
3. Allow the dataset to load automatically.
4. Review data analysis and visualizations.
5. Train and evaluate the models.
6. Test the interactive prediction function.

## 12. Limitations

- Historical associations do not establish causation.
- Revenue divided by production budget is not net profit.
- Marketing and distribution costs are not included.
- Historical data may not represent current cinema-market conditions.
- Random train/test splitting does not establish future-year forecasting performance.
- Model estimates should not be used for actual investment decisions.

## 13. Future Improvements

- Inflation-adjusted revenue prediction.
- Indian cinema-specific analysis.
- SHAP-based explainability.
- Temporal model validation.
- Marketing-cost modelling.
- Streamlit deployment.
- Automated data monitoring.

## 14. Author

**Aditya Dhage**

Data Science & AI Portfolio Project

## Disclaimer

This is an educational machine learning prototype, not a production-grade financial forecasting system.

Movie data is associated with The Movie Database (TMDB). This project is not endorsed or certified by TMDB.
