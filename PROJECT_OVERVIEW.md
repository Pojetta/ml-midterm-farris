# 🧾 Project Overview: Banknote Authentication Midterm  
**Author:** Joanna Farris  
**Date:** November 12, 2025  

## Purpose of the Project  
The goal of this project is to build, evaluate, and compare machine learning classification models that can determine whether a banknote is **authentic** or **forged**. The dataset used for this analysis comes from the **UCI Banknote Authentication Repository**, which provides four numerical features extracted from wavelet-transformed images of banknotes.

These features—**variance**, **skewness**, **kurtosis**, and **entropy**—summarize the distribution of pixel intensities in each scanned note and allow the models to identify patterns that differentiate genuine notes from counterfeit ones.

---

## Dataset Summary  
- **Source:** UCI Machine Learning Repository  
- **Observations:** 1,372 banknotes  
- **Features:**  
  - Variance of wavelet-transformed image  
  - Skewness of wavelet-transformed image  
  - Kurtosis of wavelet-transformed image  
  - Entropy of wavelet-transformed image  
- **Target:** `class` (0 = forged, 1 = authentic)  
- **Missing Values:** None  
- **Data Balance:** Approximately even between forged and authentic notes

---

## Methods and Workflow  
This project follows a structured machine learning workflow:

1. **Data Loading and Inspection**  
   - Verified dataset structure  
   - Confirmed no missing values  

2. **Exploratory Data Analysis**  
   - Histograms and boxplots for each feature  
   - Interpretation of distribution patterns and potential outliers  
   - Check for class balance  

3. **Feature and Target Assignment**  
   - Feature matrix `X` includes all four numerical features  
   - Target vector `y` includes the banknote class  

4. **Train–Test Split**  
   - 80% training data, 20% testing data  

5. **Model Training**  
   - Logistic Regression  
   - Decision Tree Classifier  

6. **Evaluation Metrics**  
   - Accuracy  
   - Precision  
   - Recall  
   - F1-Score  
   - Confusion Matrices  
   - Interpretation of results  

7. **Model Comparison**  
   - Strengths and weaknesses of each classifier  
   - Discussion of why Logistic Regression performed best  

---

## Key Results  
Both models achieved high accuracy, but **Logistic Regression reached perfect classification performance** on the test set. This strong performance indicates that the four numerical features separate the classes clearly and consistently.

A fully customized, color-coded **Decision Tree visualization** was also created to interpret model behavior and understand feature-based decision paths.

---

## Files Included  
- **README.md** — Project introduction and summary  
- **notebook/midterm-farris.ipynb** — Full data analysis and modeling workflow  
- **peer_review.md** — Peer review for another classmate  
- **PROJECT OVERVIEW.md** — High-level summary of the project  
- **notebook/data/pretty_trees.png** — Custom decision tree visualization  

---

## Reflection  
This project demonstrates how a small set of well-engineered features can produce highly accurate classification results. It also provided hands-on experience with:

- Visualization of feature distributions  
- Interpreting skewness, kurtosis, and entropy  
- Model training and evaluation  
- Understanding when linear models outperform tree-based models  
- Customizing and rendering decision trees with Graphviz  

The process highlighted the importance of clear feature behavior and consistent preprocessing in achieving excellent predictive performance.

---

## Next Steps  
With more time, further exploration could include:

- Support Vector Machines (SVM)  
- Random Forests or Gradient Boosting  
- Cross-validation for robustness  
- Feature importance analysis  
- Visualization of decision boundaries  

These additions could refine understanding of model generalization and provide deeper insights into the relationship between the four wavelet-based features and banknote authenticity.
