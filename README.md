# german-credit-data
# German Credit Risk Modeling

This project focuses on analysis and modeling of the German Credit Data dataset for credit risk classification using various machine learning algorithms.

## 📦 Dataset Overview

The dataset classifies individuals as **good** or **bad** credit risks based on 20 features. It includes both categorical and numerical versions:

- `german.data` — categorical attributes  
- `german.data-numeric` — preprocessed version with numeric features

📌 [Original source (UCI ML Repository)](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)

**Key characteristics:**
- **Instances:** 1000  
- **Features:** 20  
- **Type:** Classification (Binary)  
- **Feature types:** Categorical, Integer  
- **Missing values:** No  
- **Requires cost-sensitive modeling**

## 📊 Project Goals

- Build classification models to predict creditworthiness
- Compare model performance with and without cost matrix
- Analyze feature importance
- Optimize model by reducing dimensionality

## ✅ Key Findings

### 1. Best Performing Model — **Linear Discriminant Analysis (LDA)**
- Accuracy: **81%**
- F1-score (bad clients): **0.64**
- ROC AUC: **0.81**

LDA offered the best balance between correctly classifying good and bad clients.

### 2. Cost-Sensitive Logistic Regression
- Accuracy: **60%**
- Recall for bad clients: **83%**
- Total misclassification cost reduced from **145 to 120**

Using a cost matrix significantly reduced financial risk, even if accuracy was lower.

### 3. KNN — High Accuracy, Poor Risk Detection
- Recall (good clients): **96%**
- Recall (bad clients): **19%**

KNN failed to identify high-risk clients and is not suitable for this task.

### 4. Most Influential Features
- **Credit purpose** (e.g. education, used car, retraining)
- **Account status** (e.g. no account → negative impact)
- **Employment status** (e.g. unemployed → strong negative impact)

### 5. Feature Selection Improves Model
- Reducing to top 5–10 features:
  - Reduced error cost to **93**
  - Maintained high model performance

---

## 📌 Conclusion

- **LDA** is the best base model, but **Logistic Regression with cost matrix** is preferred when minimizing financial losses.
- **Error cost matters more than raw accuracy** in credit scoring.
- **Feature selection** can simplify models without losing effectiveness.

---

## 📁 Files

- `german.data-numeric` (99.6 KB)
- `german.data` (77.9 KB)
- `german.doc` — dataset documentation
- Project notebooks and scripts

---

## 📚 License

Include a license if you want others to use or build on your work. MIT is a common open-source choice.
