# 🛫 Flight Price Prediction using Stacking Ensemble
> **Advanced Predictive Modeling for Dynamic Airfare Analysis**

---

## 🔍 Project Overview
Flight ticket pricing is a prime example of **dynamic pricing**, where rates fluctuate based on demand, timing, and competition. This project focuses on developing a robust machine learning pipeline to forecast these prices, providing transparency for consumers and strategic insights for market analysts.
By segmenting the dataset by cabin class, this study captured class-specific pricing behaviors that are often overlooked in existing studies, resulting in a more granular and accurate prediction.

## 🔬 Technical Methodology: Stacking Ensemble
To overcome the limitations of individual algorithms, I implemented a **Stacking Ensemble** architecture. This method combines the strengths of multiple models to achieve superior predictive accuracy and stability.

1.  **Level-0 (Base Models)**: 
    *   **XGBoost & LightGBM**: Utilized for their high efficiency in handling non-linear relationships and large datasets.
    *   **Random Forest**: Employed to reduce variance and capture diverse feature interactions.
2.  **Level-1 (Meta-Learner)**: 
    *   A final **Linear Regression** model serves as the meta-learner, intelligently weighting the predictions from the base models to produce a refined final output.

## 🛠 Tech Stack
*   **Language**: `Python 3.x`
*   **Core Libraries**:
    *   `Scikit-learn`: For the StackingCVRegressor and preprocessing pipelines.
    *   `XGBoost` / `LightGBM`: Gradient boosting frameworks.
    *   `Pandas` / `NumPy`: For complex feature engineering (e.g., flight duration, day-of-week encoding).
    *   **`SHAP (SHapley Additive exPlanations)`**: For Explainable AI (XAI) to interpret model decisions.

## 📊 Key Analysis & Insights
*   **Feature Engineering**: Transformed raw timestamps into meaningful predictors like "Days until Departure" and "Peak Hour Flags."
*   **Explainable AI (XAI)**: Used **SHAP Summary Plots** to move beyond a "black-box" approach. This analysis revealed that 'Days remaining before flight' has a non-linear but strong negative correlation with price until a certain threshold.
*   **Data Visualization**: Conducted an extensive EDA to visualize the price gap between different airlines and the impact of stopovers on the final fare.

## 📂 Repository Structure
```text
.
├── Flight_Price_Prediction.ipynb  # End-to-end analysis & modeling pipeline
├── data/                          # Processed and raw flight datasets
├── Final Report/                  # Methodology, research process, results & conclusion, limitations & future work
└── README.md                      # Project documentation
