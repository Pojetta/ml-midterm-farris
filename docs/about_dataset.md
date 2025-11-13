# 📊 About the Dataset: Banknote Authentication  

## Overview  
The dataset used in this project comes from the **UCI Banknote Authentication Repository** and was created using statistical features extracted from **wavelet-transformed images** of real and forged banknotes.

Instead of raw images, the dataset includes four numerical measures that summarize the distribution of pixel intensities. These features are specifically engineered to help distinguish authentic notes from counterfeit ones.

---

## Dataset Structure  

| Component | Details |
|----------|---------|
| **Source** | UCI Machine Learning Repository |
| **Instances** | 1,372 banknotes |
| **Features** | 4 numerical features |
| **Target Variable** | `class` (0 = forged, 1 = authentic) |
| **Missing Values** | None |
| **Balance** | Nearly 50/50 between authentic and forged |

---

## Features Explained  
Each banknote image was transformed using a **Discrete Wavelet Transform (DWT)**, which decomposes the image into localized frequency components. From the resulting transformed image, four statistical descriptors were calculated:

- **Variance**  
  Measures how spread out the wavelet coefficients are. Large variance indicates stronger fluctuations in the image.

- **Skewness**  
  Indicates whether the transformed image values lean more to one side of the distribution.

- **Kurtosis**  
  Measures the “tailedness” of the distribution — high kurtosis indicates more extreme deviations.

- **Entropy**  
  Represents the degree of randomness or disorder in the image.

These features make it possible for machine learning models to classify banknotes without ever seeing the raw images.

---

## Why This Dataset Works Well  
- The features offer **strong separability** between authentic and forged notes.  
- The dataset is **clean**, has **no missing data**, and requires **minimal preprocessing**.  
- Its simplicity highlights core machine learning concepts without overwhelming complexity.

---

## File Location  
This dataset is included locally in your project under:

