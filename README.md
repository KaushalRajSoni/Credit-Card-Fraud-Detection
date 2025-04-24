# Credit-Card-Fraud-Detection

### Project Overview
This project applies **Random Forest Classifier** to detect fraudulent credit card transactions. The dataset used is highly **imbalanced**, containing **284,807 transactions**, out of which only **492** are fraudulent (**0.172%** fraud rate). Our goal was to develop a model that can accurately identify frauds without being overwhelmed by the majority class.

---

### Dataset Summary
- Total Records: **284,807**
- Fraudulent Transactions: **492**
- Legitimate Transactions: **284,315**
- Class Imbalance Ratio: **1 fraud in ~578 transactions**

---

### Key Techniques Used
- **SMOTE (Synthetic Minority Oversampling Technique)** to handle class imbalance.
- **Train-Test Split**: 80/20
- **Random Forest Classifier** with hyperparameter tuning.
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score, ROC AUC.

### Model Performance (on Test Set)
| Metric           | Value      |
|------------------|------------|
| Accuracy         | **99.91%** |
| Precision        | **87.67%** |
| Recall (Sensitivity) | **84.26%** |
| F1 Score         | **85.94%** |
| ROC AUC Score    | **0.992**  |

### Confusion Matrix
```
            Predicted
               0    1
Actual     56863   59
               8   74
```
- **True Negatives (TN)**: 56,863
- **False Positives (FP)**: 59
- **False Negatives (FN)**: 8
- **True Positives (TP)**: 74

Only **8 frauds were missed**, and **precision is high**, meaning fewer false alerts.

---

### Visualizations

#### 1. ROC Curve
- AUC Score: **0.992**
- Almost hugging the top-left corner — this means **excellent classification power**.

#### 2. Precision-Recall Curve
- Area under the PR curve is also high, showing great balance.
###  Conclusion

The Random Forest model is highly effective with a **ROC AUC of 0.992**, **precision of 87.67%**, and **recall of 84.26%**. With proper threshold tuning and monitoring, this model can significantly assist financial institutions in reducing fraud losses.
