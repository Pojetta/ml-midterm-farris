# Midterm Analysis: Banknote Authentication

## Overview
This project builds classification models to predict whether a banknote is **authentic** or **forged** using four numerical features derived from wavelet-transformed images. These features—variance, skewness, kurtosis, and entropy—summarize different statistical characteristics of each banknote image, providing clear signals for distinguishing the two classes.

---

## Exploratory Data Analysis
Histograms and boxplots showed **distinct distribution shapes** across the four features.  
No missing values were present, and the target variable (`class`) was **balanced**, supporting effective model training.

- **Variance** was roughly symmetric.  
- **Skewness** showed greater dispersion and hints of bimodality.  
- **Kurtosis** displayed a strong right skew with high-end outliers.  
- **Entropy** was left-skewed with several low-value extremes.

These patterns indicate that each feature captures different image characteristics, which likely improves classification performance.

---

## Feature Selection
All four features (variance, skewness, kurtosis, entropy) were included because each contributes meaningful information about the transformed image:

- **Variance** → spread of intensity changes  
- **Skewness** → directional asymmetry  
- **Kurtosis** → presence of extreme deviations  
- **Entropy** → randomness or disorder  

Together, these features provide complementary signals that help the model separate forged from authentic notes.

---

## Modeling
Two classification models were trained:

- **Logistic Regression**  
- **Decision Tree Classifier**

An 80/20 train–test split was used. No scaling or feature engineering was required because the dataset was already numeric, clean, and well-structured.

---

## Results
- **Logistic Regression** achieved **perfect accuracy** on the test set.  
- **Decision Tree** performed nearly as well, dropping only slightly on the test data.  

The exceptional performance across both models suggests the dataset is highly separable. Logistic Regression generalized more effectively, especially in avoiding overfitting.

---

## Reflections

### **Reflection 2: Patterns & Preprocessing**
The feature distributions revealed varied shapes, skews, and ranges. These differences suggest that each feature captures a unique aspect of banknote texture. No meaningful preprocessing was needed, as the dataset contained no missing values and all features were numerical. The only adjustment made was excluding the target column from visualizations to keep layout symmetry.

### **Reflection 3: Why These Features?**
I chose variance, skewness, kurtosis, and entropy because they represent different statistical characteristics of the wavelet-transformed images. Each one reflects a distinct type of structure—spread, asymmetry, tail behavior, and randomness—which collectively provide strong cues for distinguishing authentic from forged notes.

### **Reflection 4: Model Performance**
Logistic Regression reached near-perfect performance, with precision, recall, and F1-scores effectively at 1.0. While surprising at first glance, this makes sense given how distinct the statistical features are between the two classes. The Decision Tree also performed extremely well, though it showed a slight tendency to overfit compared to the linear model.

### **Reflection 5: Which Model Was Best?**
Logistic Regression outperformed the Decision Tree by achieving perfect accuracy on the test set. The Decision Tree performed perfectly on training data but dropped slightly on the test split, indicating mild overfitting. Logistic Regression performed best because the dataset is clean, balanced, and nearly linearly separable—conditions where linear models excel.

---

### **Reflection 6.1: Summary of Findings**
Both models performed exceptionally well in classifying banknotes using only four statistical features. Logistic Regression achieved perfect accuracy, and the Decision Tree fell only slightly short. The results demonstrate that the features extracted from wavelet-transformed images provide extremely strong, separable signals for distinguishing genuine versus forged banknotes.

### **Reflection 6.2: Challenges Faced**
The primary challenge was developing a clear conceptual understanding of how the dataset was constructed—specifically, how wavelet transforms produce coefficients and how statistical measures summarize those coefficients. The technical coding steps were straightforward; the conceptual reasoning behind the dataset was the deeper challenge.

### **Reflection 6.3: If More Time Were Available**
With more time, I would explore Random Forests, Support Vector Machines, and cross-validation. I would also experiment with visualizing decision boundaries and possibly examine alternative feature extraction methods from the original images.

### **Reflection 6: What I Learned**
I learned how statistical measures can effectively represent complex image information, allowing simple models to perform extremely well. I gained practice interpreting evaluation metrics and understanding how model performance reflects the underlying structure of the dataset. Most importantly, I saw how model choice depends on data characteristics—simple models can be more powerful than complex ones when the data is clean and highly separable.

---

## Conclusion
This project demonstrates how engineered numerical features can accurately separate authentic and forged banknotes. Logistic Regression generalized best, confirming the dataset’s strong linear separability. Both models performed exceptionally well, showing the value of well-designed statistical features for classification tasks.
