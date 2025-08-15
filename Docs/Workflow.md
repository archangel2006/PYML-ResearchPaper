# WORKFLOW

<img width="836" height="1350" alt="image" src="https://github.com/user-attachments/assets/fc928ea8-1fe8-4783-b60c-9e39f9c46857" />

---

# ✅ PHASE 1: SETUP & DATA UNDERSTANDING

### 1. Import Libraries
- Setup Google Colab or Jupyter Notebook.
- Import all necessary libraries.

### 2. Load Dataset
- Download dataset from Kaggle: [Kaggle WHO Dataset](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)
- Load CSV into pandas DataFrame.
  ```
  df = pd.read_csv("Life Expectancy Data.csv")
  ```

---

# ✅ PHASE 2: EXPLORATION & CLEANING
### 3. Initial Data Exploration
```
df.info() → check nulls, datatypes.

df.describe() → summary stats.

df['Status'].value_counts() → see class distribution (Developed/Developing).

Identify duplicate rows or anomalies.
```

# 4. Handle Missing Values

```
Fill or drop nulls:

For numerical columns: df.fillna(df.mean())

For categorical: mode or forward fill

Optionally, drop columns with too many nulls.

```
---

# ✅ PHASE 3: EDA (Exploratory Data Analysis)

### 5. Data Visualization

```
Distributions: Histogram or KDE for each feature.

Boxplots: Outliers per region/status.

Correlation Heatmap.

Compare distributions between Developed vs Developing:

sns.boxplot(x='Status', y='Life expectancy ', data=df)

```

### 6. Insights on Health & Socioeconomic Features

```
Groupby plots: e.g. df.groupby('Status')['BMI'].mean()

Pairplots or scatterplots for important variables.
```
---

# ✅ PHASE 4: FEATURE ENGINEERING & ENCODING

### 7. Feature Encoding

```
Convert Status (Developed/Developing) to numeric using:

df['Status'] = df['Status'].map({'Developed': 1, 'Developing': 0})

```

### 8. Correlation Analysis
   
```
Use .corr() to find most related features to life expectancy.

Drop highly correlated redundant features.
```
---

# ✅ PHASE 5: MODEL PREP & SPLITTING

### 9. Feature Selection
```
Separate target:
y = df['Life expectancy ']
X = df.drop(['Life expectancy ', 'Country', 'Year'], axis=1)

Check feature importance using models like Random Forest.
```

### 10. Train-Test Split
```
from sklearn.model_selection import train_test_split  
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

### 11. Feature Scaling
```
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()  
X_train_scaled = scaler.fit_transform(X_train)  
X_test_scaled = scaler.transform(X_test)
```

---

# ✅ PHASE 6: MODELING & TUNING

### 12. Model Development
```
Linear Regression
Ridge/Lasso (L1/L2)
Decision Tree
Random Forest
XGBoost
```
```
from sklearn.linear_model import LinearRegression, Ridge, Lasso
from sklearn.ensemble import RandomForestRegressor
from xgboost import XGBRegressor
```

### 13. Hyperparameter Tuning

```
from sklearn.model_selection import GridSearchCV, RandomizedSearchCV

Tuning n_estimators, max_depth, learning_rate for XGBoost or RandomForest.
```
---

# ✅ PHASE 7: MODEL EVALUATION

### 14. Evaluation Metrics
```
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score

RMSE: np.sqrt(mean_squared_error(y_test, y_pred))

MAE: mean_absolute_error(y_test, y_pred)

R²: r2_score(y_test, y_pred)
```

### 15. Compare Models Visually
```
📍Bar chart:
X-axis: Model names
Y-axis: RMSE, MAE, R²
```
---

# ✅ PHASE 8: COMPARATIVE ANALYSIS

### 16. Developed vs Developing Insights

```
Filter datasets:

df_dev = df[df['Status'] == 1]
df_devp = df[df['Status'] == 0]

Run same models on each and compare:
  - Feature importance
  - Evaluation metrics
  - Top predictors for each group

```
---

# ✅ PHASE 9: FINAL VISUALIZATIONS & REPORT

### 17. Make Visual Plots
```
1. Feature importance
2. Metric comparison
3. Developed vs Developing insights
4. Correlation heatmaps
5. Any impactful insights
```
---
# ✅ PHASE 10: Research Paper
