# Premier League Analysis - Goal Prediction

## Overview
This project analyzes Premier League football match statistics to predict the number of goals the home team will score. Using machine learning models, we explore whether match statistics can accurately predict full-time home team goals.

## Research Question
**Can we accurately predict the number of Full Time Home Team Goals using match statistics?**

## Dataset
The dataset (`PremierLeague.csv`) contains match statistics including:
- Home/Away team shots
- Home/Away team corners
- Half-time goals (home/away)
- Yellow cards (home/away)
- Team points (home/away)
- **Target:** Full Time Home Team Goals

**Location:** `/content/drive/MyDrive/ITE224/PremierLeague.csv` (Google Drive)

## Project Structure

### Step 1: Introduction & Data Loading
- Imports required libraries (pandas, matplotlib, seaborn)
- Mounts Google Drive and loads the dataset
- Displays data overview (head, tail, describe, info)

### Step 2: Data Cleaning, Preprocessing & EDA
- **Feature Selection:** 10 numerical features + 1 target
- **Missing Values:** Filled using median (robust to outliers)
- **EDA Visualizations:**
  - Histogram of target variable
  - Scatter plot (HomeTeamShots vs Goals)
  - Correlation heatmap
  - Boxplot for outlier detection

### Step 3: Data Splitting & Model Training
- **Split:** 80% training / 20% testing (random_state=42)
- **Models:**
  - Linear Regression
  - Decision Tree Regressor
- **Evaluation Metrics:** MSE and R² Score

### Step 4: Model Evaluation & Comparison
- Compares regression models using R² bar chart
- **Additional Classification Task:** Predicts `HomeTeamYellowCards` using:
  - Logistic Regression
  - Decision Tree Classifier
- Evaluated with accuracy score and confusion matrices

### Step 5: Visualization & Conclusion
- Actual vs Predicted scatter plots (both models)
- Feature importance visualization (Decision Tree)

## Requirements

```
pandas
matplotlib
seaborn
scikit-learn
numpy
google.colab (for Google Drive mount)
```

## Usage

1. Open the notebook in **Google Colab**
2. Ensure `PremierLeague.csv` is uploaded to `/content/drive/MyDrive/ITE224/`
3. Run all cells sequentially

## Models & Results

### Regression (Predicting FullTimeHomeTeamGoals)
| Model | MSE | R² |
|-------|-----|-----|
| Linear Regression | *see output* | *see output* |
| Decision Tree Regressor | *see output* | *see output* |

### Classification (Predicting HomeTeamYellowCards)
| Model | Accuracy |
|-------|----------|
| Logistic Regression | *see output* |
| Decision Tree Classifier | *see output* |

## Key Findings
- Feature importance analysis identifies which match statistics most influence home team goals
- Correlation heatmap reveals relationships between features
- Model comparison shows which approach performs better for this prediction task

## Notes
- All selected features are numeric; no categorical encoding was required
- Median imputation was chosen for missing values due to potential outliers
- The classification task (yellow cards) serves as an additional analysis beyond the primary regression goal

## Author
Premier League Analysis Project - ITE224

## License
Educational use only.# ITE224-Final-
