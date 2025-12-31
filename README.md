# Life-expectancy-analysis
WHO Life Expectancy Dataset Analysis - EDA, outlier treatment, scaling with pandas/seaborn/sklearn
**WHO Dataset EDA & Preprocessing**  
Analyzes factors affecting life expectancy (GDP, healthcare spending, schooling) using pandas, seaborn, sklearn. Handles outliers in Population/GDP, scales features for modeling readiness. [Demo notebook renders live on GitHub][file:18]

## Business Problem
Life expectancy varies globally due to economic/health factors. Goal: Clean WHO dataset, identify key predictors via EDA, prepare for ML modeling (regression/classification).

## Dataset
- **Source**: WHO Life Expectancy Dataset (2938 rows × 22 cols)
- **Key Features**: Country, Year, Life Expectancy, GDP, Population, Alcohol, BMI, Schooling, HIV/AIDS rates
- **Challenges Handled**: 24% missing values (Hepatitis B, thinness), outliers (Population/GDP), warnings fixed [file:18]

## Analysis Pipeline
1. **Data Loading & Cleaning**: Removed 'Total expenditure/Measles', filled NaNs (median/mean/mode)
2. **EDA**: Distributions, correlations, boxplots for 20 features [file:18]
3. **Outlier Treatment**: Population/GDP extremes handled
4. **Preprocessing**: Scaling ready for sklearn models
5. **Visualizations**: 20+ plots (matplotlib/seaborn)

## Key Findings
| Factor | Correlation w/ Life Expectancy | Insight |
|--------|-------------------------------|---------|
| Schooling | +0.82 | Strongest positive predictor |
| GDP | +0.55 | Economic development key |
| HIV/AIDS | -0.65 | Major negative health factor |
| Adult Mortality | -0.72 | Healthcare access critical [file:18]

## Setup & Run
```bash
pip install -r requirements.txt
jupyter notebook life-expectancy-analysis.ipynb
