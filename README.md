# 🏦 Beta Bank – Customer Churn Prediction

## 🔍 Project Overview  
Beta Bank is facing customer attrition on a monthly basis. To address this challenge, the bank has decided to use supervised learning techniques to **predict whether a customer is likely to leave**, with the goal of retaining existing users—an approach that is more cost-effective than acquiring new ones.

The objective of this project is to **develop a machine learning model that maximizes the F1-score**, with a minimum target of **0.59**. Additionally, the **AUC-ROC** metric is used to compare and supplement model performance.

---

## 🛠️ Technologies and Tools
- **Python**  
- **Libraries**: `pandas`, `sklearn`  
- **Metrics**: F1-score, AUC-ROC  
- **Models**:  
  - Logistic Regression  
  - Decision Tree Classifier  
  - Random Forest Classifier  
- **Class Balancing**:  
  - Undersampling  
  - Oversampling  

---

## ⚙️ Process

### 1. Data Inspection and Initial Model
A logistic regression model was trained without addressing class imbalance. The performance was poor:

- **F1-score**: 0.024  
- **AUC-ROC**: 0.66  

This highlighted a significant **class imbalance**, with the model failing to detect the minority class (churners).

---

### 2. Class Imbalance Solutions
To improve model performance, two approaches were tested:

- **Option 1**: Undersampling the majority class  
- **Option 2**: Oversampling the minority class  

### 3. Model Training and Evaluation

#### ✅ Logistic Regression (Balanced)
- **F1-score**: 0.669  
- **AUC-ROC**: 0.703  
- Moderate performance; improved but still limited predictive power.

#### ✅ Decision Tree Classifier
- **F1-score**: 0.723  
- **AUC-ROC**: 0.781  
- Balanced accuracy, decent generalization.

#### 🏆 Random Forest Classifier (Best Model)
- **F1-score**: 0.761  
- **AUC-ROC**: 0.849  
- Excellent balance between precision and recall.  
- Outperformed other models in both metrics.  
- Very good at differentiating churners from loyal customers.

---

## ✅ Conclusion
This project successfully addressed Beta Bank’s churn problem using supervised learning.  
The **Random Forest Classifier** stood out as the most effective solution, delivering strong predictive performance with:
- **F1 = 0.76**
- **AUC-ROC = 0.85**

By implementing this model, Beta Bank can now **proactively identify customers at risk**, enabling the creation of targeted **retention strategies** to improve loyalty and reduce attrition.

---

## 💡 Future Improvements
- Explore additional feature engineering or customer segmentation.
- Deploy the model to monitor churn probability in real time.
- Test ensemble models like **XGBoost** or **CatBoost** for potential performance boosts.
