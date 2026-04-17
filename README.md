E-Commerce Purchasing Intention Classifier

Revenue Prediction & Session Analysis using Ensemble Learning

This project focuses on predicting consumer behavior in a digital retail environment. Using the Online Shoppers Intention dataset, I developed a classification system to identify whether a user session will result in revenue. 

 Strategic Overview

    Objective: Predict user conversion (Revenue = True/False) based on administrative, informational, and product-related page metrics.

    Imbalanced Class Handling: Expertly managed a significant class imbalance (most visitors do not buy) using SMOTE and Class Weighting strategies.

    Advanced Modeling: Comparative analysis between Random Forest and Adaptive Boosting (AdaBoost) to find the optimal balance between precision and recall.

 Technical Stack

    Language: Python

    Key Libraries: Scikit-Learn, Pandas, Imbalanced-Learn (SMOTE), Matplotlib, Seaborn.

    Methodology: Grid Search Cross-Validation, Permutation Importance, Pipeline Architecture.

 Methodology
 
1. Data Cleaning & Feature Engineering

    Audit: Performed a deep-dive data audit to handle millisecond timestamps and unique session identifiers.

    Normalization: Applied StandardScaler within a pipeline to ensure distance-based metrics were treated fairly across different feature scales.

2. Experimental Design

I created modular "experiment functions" to systematically test model performance across four key configurations:

    Base Model (No scaling/No SMOTE)

    Scaled Model (StandardScaler)

    Resampled Model (SMOTE)

    Optimized Model (Scaling + SMOTE + Hyperparameter Tuning)

3. Model Interpretability

Instead of a "black box" approach, I utilized Feature Importance and Permutation Importance to identify the key drivers of revenue:

    Key Insight: PageValues and ExitRates were the strongest indicators of purchase intent, allowing for targeted UX interventions.

 Key Results

    Precision/Recall Trade-off: Successfully tuned the AdaBoost classifier to achieve a high F1-Score, ensuring we catch as many potential buyers as possible without over-targeting non-converters.

    Pipeline Robustness: Demonstrated the use of imblearn.pipeline.Pipeline to prevent data leakage during the cross-validation and resampling stages.
