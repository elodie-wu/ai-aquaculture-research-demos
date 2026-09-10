# Aquaculture AI Research Demos

This repository contains small applied AI experiments exploring how machine learning and optimisation techniques can support decision-making in aquaculture.

## Current Projects

### 1. Environmental Risk and Anomaly Detection

**Dataset:** [Aquaculture Water Quality Dataset](https://data.mendeley.com/datasets/y78ty2g293/2)

This project explores aquaculture water-quality assessment using supervised machine learning, feature selection, evolutionary optimisation, and anomaly detection.

#### Methods

- K-Nearest Neighbours
- Decision Tree
- Random Forest
- AdaBoost
- Pearson feature selection
- PCA
- Genetic Algorithm feature selection
- NSGA-II feature selection
- Isolation Forest
- Local Outlier Factor

#### Main Results

- Random Forest achieved the best classification performance with a macro F1 score of about 0.997.
- A Genetic Algorithm reduced the feature set from 14 to 11 while keeping almost the same performance.
- NSGA-II found a 6-feature solution with a search F1 score of about 0.995.
- When the 6-feature subset was re-evaluated with Random Forest, the macro F1 score was about 0.997.
- Isolation Forest and LOF agreed on 34 anomaly samples, and all of them belonged to the Poor water-quality class.
- BOD, H2S, nitrite, alkalinity, and CO2 showed the largest differences in the anomaly samples.

#### Key Finding

Evolutionary feature selection performed better than Pearson-based selection and PCA for this dataset. NSGA-II found a much smaller feature subset while keeping very high classification performance.

#### Limitations

- The `water_quality` labels are based on predefined ranges, so tree models may learn these rules very easily.
- The dataset does not contain long-term time-series data.
- The anomaly rate was set to 5% for Isolation Forest and LOF.
- This project is mainly an AI experiment and is not a real aquaculture decision-support system yet.

---

### 2. Fish Disease Detection

Planned computer vision experiment for fish disease classification using CNN and transfer learning.

---

### 3. Production Yield Prediction

Planned future experiment using environmental and production data to predict aquaculture yield.
