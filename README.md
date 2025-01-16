
# Evaluating the Performance of a New Credit Card Launch Using Data Science

## 📌 Project Overview
This project involves analyzing customer and transactional data to evaluate the performance of a newly launched credit card. The project is divided into two parts:

1. **Data Analysis and Feature Engineering:** Three datasets were cleaned, merged, and explored to derive key insights into customer behavior and financial patterns.
2. **A/B Testing:** A two-sample z-test was conducted to determine whether the new credit card outperformed existing ones in terms of transaction metrics.

---

## 📂 Table of Contents
1. [Objective](#objective)
2. [Datasets](#datasets)
3. [Methodology](#methodology)
4. [EDA Findings](#eda-findings)
5. [A/B Testing and Results](#a-b-testing-and-results)
6. [Conclusion](#conclusion)
7. [Technologies Used](#technologies-used)

---

## 🎩 Objective
The primary goal of this project was to:
- Perform data cleaning and feature engineering to create a consolidated dataset.
- Analyze customer demographics, credit behavior, and transactional data through EDA.
- Use A/B testing to validate the hypothesis that the newly launched credit card performs better than existing credit cards.

---

## 📊 Datasets
### **Dataset 1: Customer Information**
- **Columns:**
  - `cust_id`: Unique customer ID
  - `name`: Customer name
  - `gender`: Gender of the customer
  - `age`: Age of the customer
  - `location`: Geographic location
  - `occupation`: Occupation type
  - `annual_income`: Annual income of the customer
  - `marital_status`: Marital status (e.g., single, married)
  - `age_group`: Categorized age groups (18-25, 26-48, 49-65) — added via feature engineering

### **Dataset 2: Credit Information**
- **Columns:**
  - `cust_id`: Unique customer ID
  - `credit_score`: Customer credit score
  - `credit_utilisation`: Credit utilization ratio
  - `outstanding_debt`: Total outstanding debt
  - `credit_inquiries_last_6_months`: Number of credit inquiries in the last six months
  - `credit_limit`: Maximum credit limit
  - `credit_score_range`: Categorized credit scores (e.g., Poor, Fair, Good, Excellent) — added via feature engineering
  - `credit_limit_mode`: Mode-based classification of credit limits — added via feature engineering

### **Dataset 3: Transactional Data**
- **Columns:**
  - `tran_id`: Unique transaction ID
  - `cust_id`: Unique customer ID
  - `tran_date`: Transaction date
  - `tran_amount`: Transaction amount
  - `platform`: Platform used for the transaction (e.g., online, offline)
  - `product_category`: Product category of the transaction
  - `payment_type`: Payment method (e.g., credit card, debit card, GPay)

### **Final Testing Dataset**
- **Columns:**
  - `campaign_date`: Date of the campaign
  - `control_group_avg_tran`: Average transaction amount for the control group (existing cards)
  - `test_group_avg_tran`: Average transaction amount for the test group (new card)

---

## 🔢 Methodology
### **Part 1: Data Analysis and Feature Engineering**
1. Imported three separate CSV files.
2. Performed data cleaning:
   - Handled null values.
   - Identified and resolved outliers.
   - Ensured consistency in column formats.
3. Created additional features, such as:
   - `age_group` (for demographic segmentation).
   - `credit_score_range` and `credit_limit_mode` (for credit behavior analysis).
4. Merged the datasets into a single consolidated dataset using `cust_id` as the primary key.
5. Conducted EDA to explore key trends and patterns in customer demographics, credit usage, and transaction behavior.

### **Part 2: A/B Testing**
1. Imported the testing dataset containing campaign results.
2. Conducted a two-sample z-test:
   - Null Hypothesis: The new credit card performs the same as the existing cards.
   - Alternative Hypothesis: The new credit card performs better than the existing cards.
3. Calculated the p-value and compared it with the significance level (α = 0.05).

---

## 📊 EDA Findings
- **Demographics:**
  - The majority of customers (55.5%) fall in the 26-48 age group.
  - Higher average annual income observed in the 49-65 age group.

- **Credit Behavior:**
  - Customers aged 49-65 have the highest average credit limit and credit scores.
  - Credit utilization is inversely proportional to credit score.

- **Transaction Trends:**
  - Payment types vary significantly across age groups:
    - Younger customers prefer digital wallets like GPay and PhonePe.
    - Older customers rely more on traditional methods like credit cards and net banking.
  - Product categories like electronics and fashion are most popular among the 26-48 age group.

---

## 🌐 A/B Testing and Results
- **Statistical Test Used:** Two-sample z-test
- **Results:**
  - p-value = 0.001 (< 0.05)
  - Null Hypothesis rejected.
- **Conclusion:**
  - The test group (new credit card) had a significantly higher average transaction value compared to the control group (existing cards).
  - The new credit card demonstrates superior performance.

---

## 🏆 Conclusion
This project successfully analyzed customer and transactional data to derive insights and validate the performance of a new credit card. Through EDA and hypothesis testing, the project concluded that the new credit card outperformed existing offerings in key metrics like transaction value and adoption rate.

---

## 🛠️ Technologies Used
- **Programming Language:** Python
- **Libraries:**
  - pandas, numpy (data manipulation)
  - matplotlib, seaborn (visualization)
  - scipy, statsmodels (statistical testing)

---






