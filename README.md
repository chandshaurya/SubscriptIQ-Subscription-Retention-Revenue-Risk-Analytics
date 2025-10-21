### SubscriptIQ — Subscription Retention & Revenue Risk Analytics

**📘 Project Overview**

SubscriptIQ focuses on identifying customer churn patterns and revenue risk in subscription-based businesses using machine learning–driven analytics.  
The goal was to transform raw customer data into actionable insights to support **data-driven retention strategies** and improve customer lifetime value (CLV).

**🎯 Objective**

*   Detect customers at high churn risk.
*   Identify behavioral and demographic churn drivers.
*   Quantify potential revenue loss and simulate retention improvements.

**🧩 Dataset Summary**

*   **Size:** ~50,000 subscription records
*   **Domain:** Telecom/Subscription services
*   **Key Columns:**
    *   Customer ID, Contract Type, Billing Method, Tenure, Monthly & Total Charges, Internet and Streaming Services, Churn Label
*   **Target Variable:** Churn (Yes / No)

**🔍 Project Workflow**

**1️⃣ Data Understanding & Cleaning**

*   Loaded and explored raw subscription data (~50K rows).
*   Handled **missing values**, removed **duplicates**, and corrected data type inconsistencies.
*   Standardized categorical features such as Contract Type and Billing Method.
*   Treated skewed numeric fields and normalized inconsistent entries for model readiness.

🟩 _Outcome:_ Achieved a clean, consistent dataset ready for analysis and modeling.

**.**

**🔍 2️⃣ Exploratory Data Analysis (EDA)**

**The EDA phase focused on uncovering key behavioral and financial patterns that explain why customers churn and how different service, payment, and demographic factors influence retention.**

**A variety of univariate, bivariate, and correlation analyses were conducted using bar plots, box plots, histograms, and heatmaps.**

**1️⃣ Churn Distribution**

*   **Question: What percentage of customers are leaving the service?**
*   **Observation: Around 26.5% of customers were identified as churners, indicating a moderate but actionable churn level.**
*   **Insight: The churn base is significant enough to impact recurring revenue, suggesting that retention optimization could yield measurable ROI.**

**2️⃣ Contract Type vs Churn**

*   **Question: Does the type of contract affect customer churn?**
*   **Observation:**
    *   **Customers on Month-to-Month contracts showed ~43% churn,**
    *   **One-Year contracts had ~12%,**
    *   **Two-Year contracts only ~3%.**
*   **Graph Used: Clustered bar chart of churn rate by contract type.**
*   **Insight: Long-term contracts clearly drive retention. Transitioning customers from monthly to annual plans can reduce churn significantly.**

**3️⃣ Payment Method & Churn**

*   **Question: Is churn linked to how customers pay their bills?**
*   **Observation:**
    *   **Customers using electronic check payments had the highest churn rate (42%).**
    *   **Those paying via credit card or bank transfer showed much lower churn (~15–18%).**
*   **Graph Used: Bar chart comparing churn rate across payment methods.**
*   **Insight: Payment flexibility without automatic renewal mechanisms (like e-checks) leads to higher drop-offs.**

**4️⃣ Tenure vs Churn**

*   **Question: Do longer-tenure customers churn less?**
*   **Observation:**
    *   **Churn sharply declines after 12 months of tenure.**
    *   **Most churn occurs within the first 6 months.**
*   **Graph Used: Boxplot of tenure vs churn.**
*   **Insight: Early-stage retention programs (like loyalty offers or onboarding assistance) could reduce churn in the first year.**

**5️⃣ Monthly Charges vs Churn**

*   **Question: Do higher monthly charges influence churn?**
*   **Observation:**
    *   **Average monthly charge among churners = $75.3,**
    *   **Among retained users = $61.5.**
*   **Graph Used: Distribution plot and boxplot.**
*   **Insight: Customers paying higher rates are more likely to churn — possibly due to perceived value gaps. Tier-based pricing or value bundling could address this.**

**6️⃣ Service Features & Churn**

*   **Question: Which add-on services impact churn most?**
*   **Observation:**
    *   **Internet service users churn more than non-users (especially fiber-optic).**
    *   **Customers with streaming or tech support add-ons had lower churn.**
*   **Graph Used: Heatmap of service subscriptions vs churn.**
*   **Insight: Add-on services that increase engagement (like streaming bundles) indirectly improve retention.**

**7️⃣ Senior Citizen Analysis**

*   **Question: Does age group affect churn?**
*   **Observation:**
    *   **Senior citizens (age > 60) had a 42% churn rate, compared to 24% in non-seniors.**
*   **Graph Used: Bar chart comparing churn by senior citizen status.**
*   **Insight: Older customers are less tech-adaptive — churn reduction programs should focus on simplified service and dedicated support.**

**8️⃣ Correlation Analysis**

*   **Question: What are the strongest numerical relationships in the dataset?**
*   **Observation:**
    *   **Strong positive correlation between MonthlyCharges and TotalCharges.**
    *   **Moderate negative correlation between Tenure and Churn.**
*   **Graph Used: Pearson correlation heatmap.**
*   **Insight: Tenure remains the single most predictive continuous variable for churn, reaffirming the importance of early retention.**

**9️⃣ Customer Segmentation Insights**

*   **Applied K-Means clustering on normalized numerical variables (Tenure, MonthlyCharges, TotalCharges).**
*   **Identified 3 customer segments:**
    *   **Cluster 1: Long-tenure, high-value, loyal customers.**
    *   **Cluster 2: Mid-tenure, moderate spenders — retention potential.**
    *   **Cluster 3: New, high-charge users — highest churn risk.**
*   **Insight: Campaigns targeting Cluster 3 (e.g., discounts or onboarding offers) could yield maximum retention gain.**

**🧭 Key Analytical Takeaways**

| Finding | Business Impact |
| --- | --- |
| Month-to-Month contracts have 14× higher churn risk | Prioritize converting to annual plans |
| Electronic check users most volatile | Incentivize auto-pay or card-based renewals |
| 70% churn in first 6 months | Early onboarding support crucial |
| High monthly charges correlate with churn | Consider value bundling or loyalty pricing |
| Streaming & tech support add-ons lower churn | Promote engagement-linked services |

**3️⃣ Feature Engineering**

*   Created derived metrics such as **average monthly charge** and **tenure categories**.
*   Encoded categorical variables and standardized numeric fields for ML compatibility.
*   Designed final feature matrix for modeling and interpretation.

🟩 _Outcome:_ Enhanced model interpretability by transforming transactional attributes into analytical features.

**4️⃣ Predictive Modeling**

*   Applied multiple supervised models — **Logistic Regression**, **Decision Tree**, **Random Forest**, and **XGBoost**.
*   Evaluated on precision, recall, and F1-score metrics.
*   Best model (**Logistic Regression**) achieved **~79% accuracy**, demonstrating stable generalization.

🟩 _Outcome:_ Reliable churn prediction framework capable of identifying at-risk customers early.

**5️⃣ Churn Drivers & Retention Analysis**

*   Extracted feature importances and SHAP-based interpretations.
*   Identified **contract type**, **billing method**, and **tenure** as top churn influencers.
*   Simulated retention interventions — offering contract upgrades or billing changes — resulting in **~12% estimated improvement in CLV**.

🟩 _Insight:_ Converting flexible billing customers to long-term plans can substantially reduce churn.

**📊 Analytical Findings**

| Category | Insight | Impact |
| --- | --- | --- |
| Contract Type | Month-to-month users most likely to churn | High |
| Billing Method | Electronic billing linked to higher churn | Moderate |
| Tenure | Long-term customers are more stable | High |
| Monthly Charges | Higher charges increase churn probability | Moderate |

**🧠 Business Impact**

*   Improved churn detection accuracy by ~79%.
*   Enabled retention simulation models suggesting up to **12% CLV gain**.
*   Provided interpretable KPIs for churn segmentation and campaign planning.
