# HR Analytics – Predicting Employee Attrition  

## 📌 Objective  
Use analytics to understand the main causes of employee resignation and predict future attrition.  

---

## 1. Data Understanding & Preparation  
- Imported and explored the HR dataset (**1,470 employee records with 35 variables**).  
- Verified there were no missing values.  
- Removed non-informative columns: `EmployeeCount`, `EmployeeNumber`, `StandardHours`, `Over18`.  
- Converted the target variable **Attrition** into binary format (`Yes = 1`, `No = 0`).  

---

## 2. Exploratory Data Analysis (EDA)  
- **Department-wise attrition**: Highest in **Research & Development**, lowest in **Human Resources**.  
- **Salary bands**: Higher attrition in **lower salary band** compared to medium and high.  
- **Promotions**: Employees with fewer or no promotions in recent years were more likely to leave.  
- **Tenure**: Shorter-tenure employees had higher attrition.  
- **Overtime**: Employees working overtime were more prone to attrition.  
- **Marital Status**: Single employees showed higher attrition than married or divorced employees.  

---

## 3. Feature Engineering  
- Created **Income Bands** → grouped into Low, Medium, High.  
- Derived a **Tenure** feature → `YearsAtCompany / TotalWorkingYears`.  
- Added a **Promotion Gap** → measured promotion delays for modeling.  

---

## 4. Modeling  
- Split dataset into **training and testing** (stratified by attrition).  
- Preprocessing:  
  - Standardized numerical variables.  
  - One-hot encoded categorical variables.  
- Built two models:  
  - **Logistic Regression** → strong performance, identified key risk factors like **Overtime, Low Salary, Job Role type**.  
  - **Decision Tree** → interpretable rules, key drivers included **Total Working Years, Overtime, Daily Rate, Age**.  

---

## 5. Model Comparison  
- **Logistic Regression** → better predictive accuracy and generalization.  
- **Decision Tree** → slightly less accurate, but easier interpretability for HR decision-making.  

---

## 6. Feature Importance (Decision Tree)  
Top predictors of attrition:  
- **Total Working Years**  
- **Overtime**  
- **Monthly Income**  
- **Daily Rate**  
- **Age**  
- Categorical factors → **Single employees**, **Job Role (Research Scientist)**  

---

## 7. Data Export for Visualization  

  ### 📂 Data Sources  

- **Actual dataset** → [`HR Employee Attrition.csv`](https://github.com/Progati00/Predicting-Employee-Attrition/blob/main/HR%20Employee%20Attrition.csv)
  
- **Transformed dataset** → [`cleaned_hr_data.csv`](https://github.com/Progati00/Predicting-Employee-Attrition/blob/main/cleaned_hr_data.csv)  
  - Encoded + scaled features  
  - Used for machine learning modeling  

- **Original dataset** → [`hr_data_cleaned_original.csv`](https://github.com/Progati00/Predicting-Employee-Attrition/blob/main/hr_data_cleaned_original.xlsx)  
  - Retained categorical + numerical values  
  - Used for **Power BI dashboards** and business-friendly reporting  

---

## 8. Power BI Dashboard Insights  
- **Overall Workforce & Attrition**: Majority are active, but attrition ~16%.  
- **Department-wise**: R&D and Sales show highest attrition counts; HR shows proportionally high attrition despite smaller size.  
- **Income & Attrition**: Lower-income employees leave most often; high attrition also seen among **high-income Sales Executives**.  
- **Job Role Trends**: Laboratory Technicians, Research Scientists, Sales Reps → higher attrition at lower incomes; Sales Executives attrition across income levels.  
- **Career Stage**: Younger employees most prone to leave (especially in Sales & HR); attrition decreases steadily with seniority.  
- **Other Key Drivers**: **Overtime** and **lack of promotions** strongly linked with resignations.  

---

## 🚀 Deliverables  
- EDA insights on attrition by department, salary, promotions, overtime, demographics.  
- Classification models (**Logistic Regression & Decision Tree**) with comparison.  
- Feature importance analysis for HR policy recommendations.  
- **Power BI dashboard** with attrition insights.  
- Exported datasets for ML and visualization.  
