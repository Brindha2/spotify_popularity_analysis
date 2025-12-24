# Spotify Popularity Prediction

Predicting Spotify track popularity using audio features and machine learning models.

---

## Problem Statement

Spotify provides a popularity score (0–100) that reflects how widely a track is streamed on the platform.  
This project investigates whether **audio features alone** (e.g., danceability, energy, tempo) can be used to predict that popularity score.

The task is formulated as a **supervised regression problem**.  
This analysis focuses on **prediction and correlation**, not causation.

---

## Dataset

- Source: The dataset used in this project is synthetically generated to resemble Spotify audio features, allowing focus on             the machine-learning workflow rather than data acquisition.
- Target variable: `popularity`
- Features include: danceability, energy, loudness, tempo, etc.
- Dataset location: `data/spotify_synthetic_popularity_dataset.csv`

---

## Approach

1. Exploratory Data Analysis (EDA) to understand feature distributions and target behavior  
2. Baseline Linear Regression model  
3. Random Forest Regressor with 5-fold cross-validation  
4. Evaluation using MAE, RMSE, and R²  
5. Permutation-based feature importance for interpretability  

---

## Results

- **MAE:** 6.61  
- **RMSE:** 8.43  
- **R²:** 0.42
- **Baseline MAE:**6.15
The Random Forest model could not outperform the baseline linear model indicating that either the relationship was linear or the features lack information needed for nonlinear gains.

---

## Limitations

- Spotify popularity is influenced by non-audio factors such as marketing, playlist placement, and artist visibility  
- The dataset does not capture temporal dynamics or listener behavior  
- Results should not be interpreted causally  

---

## Future Work

- Reformulate the problem as a ranking task instead of regression  
- Incorporate release date and temporal trends  
- Use SHAP values for deeper feature interpretability  
- Explore gradient boosting or neural models  

---

## How to Run

1. Clone the repository  
2. Ensure `spotify_synthetic_popularity_dataset.csv` is placed in the `data/` directory  
3. Open the notebook  
4. Run all cells top to bottom  

---

## Requirements

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib / seaborn  
