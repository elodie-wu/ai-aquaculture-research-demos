# 🌊 Environmental Risk and Anomaly Detection

This project explores how machine learning, feature selection, evolutionary optimisation, and anomaly detection can be used to analyse aquaculture water-quality data.

## 📊 Dataset

**Dataset:** [Aquaculture Water Quality Dataset](https://data.mendeley.com/datasets/y78ty2g293/2)

The dataset contains 14 environmental features and one target variable, `water_quality`.

The target contains three classes:

- 0 — Excellent
- 1 — Good
- 2 — Poor

## 🎯 Project Goals

This project investigates three main questions:

1. Which machine-learning models work well for water-quality classification?
2. Can feature selection reduce the number of input features while keeping similar performance?
3. Can anomaly detection identify unusual water-quality conditions?

## 🧠 Methods

### Classification

- K-Nearest Neighbours
- Decision Tree
- Random Forest
- AdaBoost

### Feature Selection

- Pearson correlation
- PCA
- Genetic Algorithm
- NSGA-II

### Anomaly Detection

- Isolation Forest
- Local Outlier Factor
- Isolation Forest + LOF ensemble

## 📈 Main Results

### Classification

Random Forest achieved the best validation performance, with a macro F1 score of about **0.997**.

Decision Tree achieved very similar performance, while KNN performed lower and AdaBoost performed poorly with the default settings.

### Feature Selection

The Genetic Algorithm reduced the feature set from **14 to 11 features** while keeping almost the same classification performance.

NSGA-II found a stronger trade-off solution using only **6 features**, with a search macro F1 score of about **0.995**.

When the same 6-feature subset was re-evaluated using Random Forest, the macro F1 score was about **0.997**.

### Anomaly Detection

Isolation Forest and Local Outlier Factor agreed on **34 anomaly samples**.

All 34 ensemble anomalies belonged to the **Poor** water-quality class.

The largest standardized differences were found in:

- BOD
- H2S
- Nitrite
- Alkalinity
- CO2

## 🔍 Key Findings

Evolutionary feature-selection methods performed better than Pearson-based selection and PCA on this dataset.

The results show that a smaller feature subset can keep very high classification performance.

The anomaly-detection results also suggest that some poor water-quality samples have clearly unusual environmental feature patterns.

## ⚠️ Limitations

- The `water_quality` labels are based on predefined ranges, so tree models may learn these rules very easily.
- The dataset does not contain long-term time-series data.
- The anomaly rate was set to 5% for Isolation Forest and LOF.
- The dataset may not fully represent different farms, fish species, or locations.
- This project is mainly an AI experiment and is not a real aquaculture decision-support system yet.

## 🚀 Future Work

Possible future improvements include:

- testing the models on real farm sensor data
- using time-series data to analyse water-quality changes
- comparing different anomaly-detection settings
- testing the selected feature subsets on other datasets
- combining the analysis with a small aquaculture monitoring prototype

## 🛠 Technologies

Python, Pandas, NumPy, Matplotlib, Scikit-learn, DEAP
