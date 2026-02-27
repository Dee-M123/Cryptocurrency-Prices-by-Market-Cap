📊 **Macroeconomic Conditions & Sovereign Default Risk**

**Research Question:**

**What macroeconomic conditions increase sovereign default risk?**


1️⃣ **Project Overview**

This project examines the relationship between macroeconomic instability and sovereign default risk using descriptive statistical analysis.

The analysis focuses on inflation dynamics, crisis indicators, and historical instability patterns.


2️⃣ **Data Source**

**The dataset is sourced from Kaggle:**

Africa Economic, Banking and Systemic Crisis Data
https://www.kaggle.com/datasets/chirin/africa-economic-banking-and-systemic-crisis-data

The dataset compiles historical macroeconomic and crisis-related indicators across multiple African countries.


3️⃣ **Data Structure**

The dataset is structured as a panel dataset, meaning:

    - Multiple countries
    
    - Observed across multiple years
    
    - Each row represents a country-year observation


**Key Variables Used**

- inflation_annual_cpi → Annual CPI inflation rate

- sovereign_external_debt_default → Binary indicator (0 = No Default, 1 = Default)

- banking_crisis → Banking crisis indicator

- year → Time dimension

This structure allows cross-country and time-series descriptive comparisons.


4️⃣ **Data Cleaning & Preparation**

To ensure analytical quality:

- Missing values were reviewed and handled appropriately

- Variable types were validated

- Binary crisis indicators were confirmed (0/1 format)

- Inflation outliers were identified using the Interquartile Range (IQR) method
  

**Data was analyzed under three conditions**:

    - Full dataset
    
    - Normal inflation observations
    
    - Inflation outlier observations
  

5️⃣ **Analytical Approach**

Because the project focuses on descriptive statistics, the following techniques were applied:

- Correlation analysis

- Grouped mean comparison

- Crisis probability calculation

- Time-period aggregation

- Data visualization using Matplotlib / Seaborn

No predictive modeling or causal inference was performed.

**The goal was to uncover patterns and associations**.

6️⃣ **Business Question 1**

**Does Inflation Increase Sovereign Default Risk?**

Correlation Results:

| Dataset Segment       | Correlation (Inflation vs Default) |
| --------------------- | ---------------------------------- |
| Full Dataset          | **0.0726** (Very Weak Positive)    |
| Normal Inflation Only | **-0.0053** (No Relationship)      |
| Inflation Outliers    | **0.1240** (Moderate Positive)     |


Results on full dataset:

<img src="images/screenshot.png" width="600">
<img width="1158" height="740" alt="Sovereign Default Rate" src="https://github.com/user-attachments/assets/ef5e4bd6-a735-4aa7-9415-1bcbb1d1df7a" />

Results on outliers: 
<img width="1086" height="740" alt="Default Rate Among Inflation Outliers" src="https://github.com/user-attachments/assets/ff21ea9a-2725-4441-88f8-8008d5312c48" />

Results without outliers: 
<img width="1122" height="742" alt="Default Rate (Normal Inflation Only" src="https://github.com/user-attachments/assets/e6af479e-11c5-44f5-85f9-74b63e5878b4" />

Correlation overview: 
<img width="1334" height="936" alt="Correlation Between Inflation and Sovereign Default" src="https://github.com/user-attachments/assets/7d9aabcb-5af6-4e8a-ad0f-de3fac655ecc" />

**Interpretation**

    - Inflation overall shows a very weak positive association with default risk.
    
    - Normal inflation levels show no meaningful relationship.
    
    - Extreme inflation years show a stronger positive association with sovereign default events.

**Key Insight**

Sovereign defaults are more closely associated with macroeconomic extremes rather than normal inflation fluctuations.

7️⃣ **Business Question 2**

**Which Historical Period Was Most Economically Unstable?**

**Descriptive Findings:**

Inflation by Decade:

<img width="1190" height="738" alt="Inflation by Decade" src="https://github.com/user-attachments/assets/4dd1abbb-2ab9-4edf-9c89-93b818216613" />

Banking Crisis Probability by Decade: 

<img width="888" height="628" alt="Banking Crisis Probability by Decade" src="https://github.com/user-attachments/assets/1dcfa54c-3b13-4c81-8b15-94d383968e7d" />

Sovereign External Debt Default Probability by Decade:
<img width="974" height="630" alt="Sovereign External Debt Default Probability by Decade" src="https://github.com/user-attachments/assets/5650df31-86d3-4bf1-9e54-bfde68c48474" />

Country's economic instability in different decades: 
<img width="1534" height="948" alt="Economic Instability by Country and Decade" src="https://github.com/user-attachments/assets/0cc4fca7-7192-4794-8243-90c29fcececa" />

Summary of findings: 

    - Inflation spiked significantly during the 1980s–1990s
    
    - Banking crisis probability peaked in the 1990s
    
    - Default probability also peaked in the 1990s

Instability occurred across multiple indicators simultaneously

**Interpretation**

- The 1990s represent the most economically unstable period in the dataset.

- This period exhibited:

- Elevated inflation volatility

- Increased banking crisis frequency

- Higher sovereign default probability
  

Instability was broad-based rather than isolated.


8️⃣ **Overall Conclusion**

Descriptive statistical evidence suggests:

    - Regular inflation does not meaningfully increase sovereign default risk.
    
    - Extreme inflation periods are more strongly associated with defaults.
    
    - The 1990s represent the peak of macro-financial instability.
    

**Final Takeaway**

Sovereign default risk appears to rise during periods of extreme macroeconomic stress, not during normal economic conditions.


9️⃣ **Limitations**

- Descriptive analysis only

- Correlation does not imply causation

- Results limited to African country sample

- No econometric modeling performed
  

🔟 **Technical Summary**


    Python (Pandas) used for data handling
    
    IQR method used for outlier detection
    
    Correlation coefficients computed
    
    Group means used to calculate crisis probabilities
    
    Visualizations generated using Matplotlib / Seaborn
    

1️⃣1️⃣**Project Structure**

<img width="1202" height="636" alt="read" src="https://github.com/user-attachments/assets/2941f641-18c8-4dc5-a5b4-6b7e2f8deaf9" />



    
