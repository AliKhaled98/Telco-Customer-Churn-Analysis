#  Telco Customer Churn Analysis  

I recently completed a full end-to-end business analysis project where I explored customer churn behavior for a telecom company. The main goal was to simulate a **real business analytics workflow**, starting from **SQL data extraction**, moving through **Python-based analysis**, and ending with a **Power BI dashboard** for executive storytelling.  

---

##  Project Overview  

This project aimed to uncover what drives customers to leave and which customer groups are most likely to churn.  

I started by connecting directly to **Microsoft SQL Server** using Python (`pyodbc`) to extract the data — simulating how analysts work with live company databases instead of static CSVs.  

After cleaning and preparing the data, I explored patterns, validated findings statistically, and built customer segments to identify retention opportunities.  

---

##  Key Steps  

###  Data Extraction & Cleaning  
- Pulled customer data from **SQL Server** using `pyodbc`.  
- Handled 11 missing values in `TotalCharges` by replacing them with 0 (representing new customers who hadn’t been billed yet).  
- Detected outliers using IQR but kept valid extreme values as they reflected meaningful customer behavior.  

###  Exploratory Data Analysis (EDA)  
- Found most customers pay **$20–$80/month**.  
- Total charges distribution was **positively skewed**, showing that many leave early while smaller loyal groups stay long-term.  
- About **26% of customers churned**, a high but realistic rate in telecom.  

###  Statistical Validation  
To move beyond intuition, I ran statistical tests to **confirm insights with evidence**:  
- **Mann–Whitney U Test** → tenure distribution differs significantly between churned and stayed customers.  
- **Welch’s T-Test** → higher monthly charges significantly correlate with churn.  
- **Chi-Square Test** → churn varies strongly across contract types.  

**Key findings:**  
- Short-tenure customers churn more.  
- High monthly charges link to higher churn.  
- Month-to-month contracts have the highest churn rates.  

###  Customer Segmentation  
Segmented customers to identify patterns and retention opportunities:  
- **Tenure Segmentation:**  
  - 1–3 months churn ~57% → onboarding issues.  
  - 30+ months churn ~18% → strong loyalty.  
- **Monthly Charges Segmentation:**  
  - Premium users ($81–$100) churn ~37%, indicating price sensitivity.  
- **Internet Service:**  
  - Fiber optic users churn ~42% — potential dissatisfaction or pricing issue.  

###  Dashboard Creation (Power BI)  
Designed a **Power BI dashboard** for storytelling:  
- KPIs: Churn Rate, Total Customers, Monthly Revenue.  
- Slicers: Contract Type, Payment Method, Internet Service.  
- Visuals: Churn by Tenure, Monthly Charges, Contract Type, Add-on Engagement.  

---

##  Key Insights  
- Customers in their first 3 months have the **highest churn (~57%)**.  
- **Auto-payment methods** have the lowest churn.  
- **Month-to-month contracts** are the biggest churn risk.  
- **Fiber optic** users churn more — possible pricing dissatisfaction.  
- **Premium-paying** customers are more sensitive to perceived value.  

---

##  Tools & Technologies  
| Category | Tools Used |
|-----------|-------------|
| Database | Microsoft SQL Server |
| Data Extraction | Python (`pyodbc`) |
| Analysis & Stats | Pandas, Seaborn, SciPy |
| Visualization | Power BI |
| Documentation | Markdown, Jupyter Notebook |

---



