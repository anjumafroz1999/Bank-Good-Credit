# Bank-Good-Credit
# Bank Good Credit – Customer Credit Risk Analysis

## 📌 Project Overview
This repository contains a **credit risk analysis project** using data from three tables:  
- `cust_demo` – Customer demographic information  
- `cust_details` – Account and transaction details  
- `cust_land` – Loan and enquiry records  

The goal is to **merge these datasets into a unified DataFrame** and build models that predict customer creditworthiness.  
This helps banks identify **low-risk customers** eligible for favorable loan terms and flag **high-risk customers** for closer monitoring.

---

## 📂 Dataset Structure
The merged dataset includes:
- **Demographics**: Age, Gender, Education, Occupation, Region  
- **Account details**: Account type, Opening date, Current balance, Credit exposure  
- **Loan & enquiry records**: Loan type, Enquiry frequency, High credit amount, Repayment behavior  
- **Target variable**: `Bad_label` (binary indicator of credit risk – 0 = good credit, 1 = bad credit)

---

## ⚙️ Methodology
1. **Data Integration**  
   - Merge `cust_demo`, `cust_details`, and `cust_land` using `customer_id` as the key  
   - Ensure consistency across categorical and numeric fields  
2. **Exploratory Data Analysis (EDA)**  
   - Distribution of features (education, occupation, account type) vs. credit risk  
   - Balance amount and enquiry frequency analysis  
   - Correlation heatmaps for feature selection  
3. **Data Preprocessing**  
   - Handle missing values and outliers (IQR method)  
   - Encode categorical variables (one-hot encoding)  
   - Balance classes using **SMOTE**  
4. **Model Building**  
   - Logistic Regression, Random Forest, SVC, MLP  
   - Hyperparameter tuning with GridSearchCV and RandomizedSearchCV  
5. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1-score  
   - Confusion Matrix interpretation (focus on Recall for bad credit class)  

---

## 📈 Key Insights
- **Education level** strongly correlates with repayment behavior – graduates and post-graduates show lower default rates.  
- **Occupation** in Banking & Financial Services has higher credit card activity with strong repayment records.  
- **Card type analysis** revealed RBL Bank Fun+, Insignia, and Platinum Cricket card holders have perfect credit scores.  
- **Balance vs. risk**: Customers with higher current balances tend to have better credit scores.  
- **Enquiry frequency**: Frequent loan enquiries in the past 365 days correlate with higher bad credit risk.  

git clone https://github.com/yourusername/bank-good-credit.git
cd bank-good-credit
