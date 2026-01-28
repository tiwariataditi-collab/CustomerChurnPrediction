# CustomerChurnPrediction
This project focuses on predicting customer churn for a telecom company using machine learning techniques. Customer churn refers to customers who stop using a numpy

company’s services. By identifying patterns in customer behavior, businesses can take proactive steps to improve retention. 

🧰 Technologies Used:
  Python,
  Pandas, NumPy,
  Matplotlib, Seaborn'
  Scikit-learn,

📂 Dataset:

  Source: Telco Customer Churn Dataset,
  
  Target Variable: Churn (Yes / No),
  
  Features include:
  
  Demographics (gender, senior citizen, partner, dependents),
  
  Services (internet, phone, streaming, security, backup),
  Account information (contract type, payment method, charges),

🔍 Project Workflow

1️⃣ Data Loading

  Imported necessary libraries
  
  Loaded the dataset using pandas.read_csv()
  
  Displayed first and last rows to understand the structure

2️⃣ Data Exploration

  Checked dataset shape and column data types
  
  Used info() and describe() for statistical insights
  
  Analyzed churn distribution

3️⃣ Data Cleaning & Preprocessing

  Converted TotalCharges column to numeric
  
  Handled missing values using median imputation
  
  Replaced inconsistent categorical values (e.g., "No phone service" → "No")
  
  Dropped unnecessary column (customerID)

4️⃣ Exploratory Data Analysis (EDA)

  Visualized churn distribution
  
  Used pair plots, count plots, and box plots
  

5️⃣ Feature Encoding

  Converted binary categorical columns into numerical form
  
  Applied One-Hot Encoding to multi-class categorical features like PaymentMethod
  
  Ensured all features were model-ready

6️⃣ Feature Scaling

  Applied StandardScaler to normalize numerical features
  
  Improved model performance and stability

7️⃣ Train-Test Split

  Split data into 80% training and 20% testing
  
  Ensured balanced evaluation of the model

8️⃣ Model Building

  Used Random Forest Classifier
  
  Configured with:
  
   n_estimators = 100
   
   random_state = 42
   
   Trained the model on the training dataset

9️⃣ Model Evaluation

  Generated predictions on test data
  
  Evaluated using:
  
  Accuracy Score
  
  Classification metrics
  
  Displayed results using a custom evaluation function

🔟 Feature Importance

  Analyzed which features contributed most to churn prediction
  
  Visualized feature importance using bar plots
  
  Key influencing factors included:
  
   Contract type
   
   Monthly charges
   
   Internet service
   
   Payment method

✅ Results

  The Random Forest model achieved strong predictive performance
  
  Successfully identified key churn drivers
  
  Demonstrated how machine learning can help businesses reduce customer attrition

🔁 Postdictive Analysis (Predicted vs Actual Churn)

Postdictive analysis evaluates how well the model’s predictions match actual customer churn outcomes and helps understand both strengths and weaknesses of the model.

📌 Predicted Churn vs Actual Churn

 ~The model correctly identified a large proportion of non-churn customers, showing strong performance in recognizing loyal users.
 
 ~It also successfully detected many high-risk churn customers, especially those with short tenure and month-to-month contracts.
 
 ~Some churn cases were misclassified, particularly where customer behavior was less consistent.

✅ Where the Model Performed Well

The model performed strongly in the following areas:

Long-term contract customers

→ Accurately predicted low churn due to stable customer behavior

Customers with high monthly charges + short tenure

→ Correctly flagged as high churn risk.

Clear behavioral patterns

→ Customers using electronic check payments and fiber-optic internet were predicted accurately.

Non-churn prediction

→ The model showed high reliability in predicting customers who are likely to stay.

❌ Where the Model Failed & Why

Despite good performance, the model had some limitations:

~False Negatives (Actual churn but predicted as non-churn)

  ~Customers who churned suddenly due to reasons not captured in data (e.g., service issues, competition offers).
  
  ~Long-tenure customers who unexpectedly left.


~False Positives (Predicted churn but actually stayed)

  ~Price-sensitive customers who were flagged but remained due to discounts or loyalty benefits.
  
  ~Customers with mixed signals (high charges but strong service usage).

~Reasons for failure:

 ~Lack of qualitative data (customer satisfaction, complaints, network quality).
 
 ~External factors not included in the dataset (market competition, regional issues).
 
 ~Class imbalance between churn and non-churn customers.

💼 Business Recommendations---

🎯 Actions to Reduce Customer Churn---

  1. Promote Long-Term Contracts

      Offer discounts or perks for customers switching from month-to-month to annual contracts.

     
  2. Target High-Charge Customers
  
   Provide personalized pricing plans or loyalty discounts for customers with high monthly charges.


  3.Improve Fiber-Optic Service Experience
  
  Investigate service quality issues leading to higher churn in fiber-optic users.

    
  4.Review Payment Methods
  
  Encourage customers using electronic checks to switch to auto-debit or credit card payments.

    
  5.Early-Stage Engagement
  
  Focus retention efforts on new customers within the first few months of service.

⭐ Customers to Prioritise

 The company should prioritize customers who meet multiple risk criteria:
  
  Month-to-month contract holders 
  
  High monthly charges 
  
  Short tenure
  
  Fiber-optic internet users
  
  Electronic check payment users

These customers have the highest churn probability and should receive targeted retention offers.

🧠 Strategic Insight

   By combining machine learning predictions with business strategy, companies can move from reactive churn handling to proactive customer retention,
   
   improving revenue stability and customer satisfaction.
