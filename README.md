# EXCEL-TELECOM-CHURN-ANALYSIS
## Overview

This project focuses on analyzing customer behavior within a telecommunications company to understand the drivers of customer churn, identify at risk customers and develop a structured risk segmentation model to support retention strategies.
The analysis was carried out using Microsoft Excel and combines descriptive, diagnostic and predictive analytics to uncover behavioral patterns that influence churn decisions

## Core Objective

The primary goal of this project is to:

Analyze customer behavior and service usage patterns to identify drivers of churn, predict customers at risk of leaving and recommend actionable strategies to improve customer retention.

## Analytical Structure/ Analysis Questions

The analysis follows a 3 layer framework:

### A.) Descriptive Analysis (What happened?)
`This focuses on understanding churn distribution and customer behavior patterns.

Analysis Questions
  
1. What is the churn rate?  
2. How does churn vary across states, area codes, and plans?  
3. What usage patterns exist between churned and retained customers?  
4. How do customer service interactions vary?
  
### B.) Diagnostic Analysis (Why it happened?)

This focuses on Identifying root causes and behavioral drivers of churn.

Analysis Questions

1. Does customer service interaction affect churn?  
2. Is churn linked to high charges or usage?  
3. Are plan mismatches driving churn?  
4. What behavioral patterns are common among churned customers?

  ### C.) Predictive Analysis (Who will churn?)

This focuses on Building risk segmentation to identify at-risk customers.

Analysis Questions  

1. Which variables best predict churn?
2. Can customers be grouped into risk segments?  
3. What early indicators signal churn risk?

  ## Data Preparation

Before analysis, the dataset was validated for quality:

- Cleaning Checks  
- Missing values check  
- Duplicate detection  
- Blank row validation  
- Data type consistency  
- Categorical value verification  
  
### Outcome

The dataset was confirmed clean and analysis-ready.

## Derived Metrics

New analytical columns were created from the raw dataset to support churn analysis.

### A.) Total Usage

Combined:
- Day Minutes
- Evening Minutes  
- Night Minutes  
- International Minutes

### B.) Total Charges

Combined:
- Day Charges  
- Evening Charges  
- Night Charges  
- International Charges

### C.) Total Calls

Combined:
- Day Calls
- Evening Calls
- Night Calls
- International Calls

  ### D.) Customer Service Risk Level

Based on number of support calls:
- 0–1 → Low Risk  
- 2–3 → Medium Risk  
- 4+ → High Risk

### D.) Usage Risk Level

Based on dynamic thresholds:
- Above 110% of average → High  
- Below 90% of average → Low  
- Otherwise → Medium

  ### E.) Charges Risk Level

Same dynamic average-based logic used for usage risk level.

### F.) International Usage Behavior

Categories:
- Paying & Using  
- Paying but Not Using  
- Unplanned Usage    
- Inactive

### G.) Voicemail Usage Behavior

Categories:
- Active User
- Unused
- Unsubscribed Usage
- Inactive

### H.) Risk Segmentation
- High Risk  
- Medium Risk  
- Low Risk  

### Classification Logic
- High Risk: High customer service complaints AND
Unplanned international usage  
- Medium Risk:Medium service risk OR
High charges risk    
- Low Risk: Stable behavior across all indicators

  ## Conditional Formatting 

To improve interpretability, conditional formatting was applied across all risk segmentation outputs in Excel.
Implementation:
- High Risk → Red highlight  
- Medium Risk → Yellow/Amber highlight  
- Low Risk → Green highlightators
  
<img width="1579" height="710" alt="Screenshot (50)" src="https://github.com/user-attachments/assets/b5be8f00-9cc6-4320-bc0d-659c87e7ee8c" />

 ## Dynamic Analysis Layer
### A.) Unique States List
Used for geographic segmentation

### B.) High-Risk Customers List
Used for retention targeting

### C.) Churned Customers List
Used for churn behavior analysis

### D.) High-Risk & Churned Customers
Used to validate predictive accuracy of risk model  
<img width="705" height="703" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/a55f0962-9dac-4698-be8b-927a83fb17fd" />

## Excel Functions Used
 The project intentionally incorporated advanced Excel functions to demonstrate analytical and modeling capability.  
 Functions Used:
 - Logical & Conditional Functions: * IFS * IF * AND * OR  
   Used for: * churn risk classification * behavioral segmentation * conditional grouping
- Error Handling: * IFERROR   
   Used to: * prevent broken calculations * improve formula robustness
- Aggregation Functions * AVERAGE  
   Used for: * dynamic threshold calculations * usage and charges segmentation  
- Dynamic Array Functions : * UNIQUE * SORT * FILTER    
   Used for: * automated lists * customer segmentation * dynamic filtering 

## Pivot Table Analysis

Pivot tables were heavily used throughout the project to support dashboard creation, trend analysis, and model validation.

Pivot tables were used to:
- Summarize customer churn patterns
- Compare churn across categories
- Analyze behavioral trends
- Generate dashboard-ready summaries
- Validate predictive segmentation

<img width="1526" height="719" alt="Screenshot (51)" src="https://github.com/user-attachments/assets/7484b79c-37ce-469f-8b09-432fa4b37b9b" />

## Dashboard Structure

### Layer 1: Churn Overview (Descriptive)

- Churn distribution  
- Churn by area code  
- Churn by plan type  
- Customer service distribution  

### Layer 2: Churn Drivers (Diagnostic)  

- Service calls vs churn  
- Charges vs churn  
- Usage patterns vs churn  
- Plan behavior interaction  
  
### Layer 3: Risk & Retention (Predictive)

- Risk segmentation  
- High-risk distribution  
- Key churn drivers  
- Retention opportunity analysis 

 ### Key Performance Indicators (KPIs)  
 
- Total Customers
- Total Churned Customers
- Churn Rate
- Avg Customer Service Calls
- Avg Total Charges
- High Risk Customers

<img width="902" height="680" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/ffb0a20c-f9de-4009-8079-a5f8180bfbad" />

## Key Insights

### 1. Descriptive Analysis — What Happened?  

#### A.) What is the overall churn rate?
   The dashboard shows:  
- 667 total customers
- 95 churned customers
- 14.24% churn rate    
   Insight: The company is losing roughly 1 out of every 7 customers, which indicates a moderate churn problem that requires attention.

 #### B. How does churn vary by area code?  
 The churn overview shows differences across area codes:   
 -  Area code 415 recorded the highest churn volume followed by 408 while 510 showed relatively lower churn.    
   Insight: Certain geographic/customer clusters appear more vulnerable to churn than others, suggesting differences in customer experience or service behavior across regions.

  #### C. What is the churn rate by plan type?  
  The dashboard indicates:   
  -  customers with unplanned international usage experienced noticeably higher churn while customers properly aligned with plans were more stable.
  -  For voicemail behavior: inactive voicemail users formed the largest group, active voicemail users showed lower churn tendencies.  
   Insight: Customers whose usage behavior does not match their subscribed plans are more likely to leave.

  #### D . How do usage patterns differ between churned and retained customers? 
  The Usage Pattern vs Churn chart shows:   
- churned customers are concentrated more heavily within the high usage risk group,  retained customers dominate the low-risk usage segment.    
  Insight: Heavy usage customers appear more sensitive to service quality and pricing pressure.  
  
  #### E. What is the distribution of customer service calls?    
  The customer service call distribution shows:  
-  most customers made between 1–3 service calls, churn increases significantly among customers with higher complaint frequency.  
   Insight: Frequent customer service interaction may reflect unresolved issues and dissatisfaction.

  ### 2. Diagnostic Analysis — Why Did Churn Happen?   
  This stage identified the major drivers contributing to churn.  
  
 #### A. Does high customer service interaction increase churn likelihood?   
 Yes. The Customer Service Calls vs Churn chart shows:   
 - churn rates rise significantly within the high customer service risk category.  
 Insight: Customers who repeatedly contact support are more likely to leave suggesting unresolved complaints or poor customer experience.

####  B. Is churn associated with higher charges?   
Yes. The Charges Risk Level chart shows: 
-  customers in the high charges risk segment recorded the highest churn proportion.    
  Insight: Higher spending customers may feel they are not receiving sufficient value relative to cost.  
 
#### C. Is churn associated with high usage intensity?    
Yes. The usage risk analysis indicates:
-  customers with high usage levels experienced increased churn likelihood.     
 Insight: High usage customers are likely more sensitive to: network quality, billing concerns,  service reliability.

#### D. Do customers without suitable plans churn more?   
Yes. The International Usage Behavior analysis shows:  
- customers with unplanned international usage displayed elevated churn behavior.  
  Insight: Poor alignment between customer needs and plan subscriptions contributes strongly to dissatisfaction.

  #### E. Are there common behavioral patterns among churned customers?
  Yes. Most churned customers tend to show: high service complaints, high charges, high usage intensity and inconsistent plan behavior.  
  Insight:  Churn is rarely driven by a single factor. Instead, it is usually a combination of dissatisfaction, pricing pressurE and poor service-plan alignment.

  ### 3. Predictive Analysis — Who Is Likely to Churn?
  This stage focused on identifying high-risk customers before churn occurs.

  #### A. Which variables are strongest predictors of churn?
   The strongest churn indicators identified were:
-  Customer Service Calls
-  International Usage Behavior
-  Customer Usage Level
-  Charges Risk Level  
   Insight: Complaint frequency emerged as the most influential churn driver.
   
#### B. Which customer profile represents the highest churn risk?   
 High-risk customers typically exhibit:   
 - frequent customer service interaction,high charges, high usage intensity and unplanned international usage behavior.
 
 #### C. Can customers be segmented into risk categories?  
 Yes. Customers were successfully grouped into:   
 - High Risk    
 - Medium Risk    
 - Low Risk  
   The risk validation chart confirms:  
-  High-risk customers recorded the highest churn rate while low-risk customers showed significantly lower churn levels.    
  Insight: The segmentation model effectively identifies vulnerable customer groups.

 #### D. What simple rules can identify at-risk customers early?   
 Customers are likely to become high risk when they:   
 -  make repeated customer service calls, show unusually high charges, display excessive usage behavior or use services without suitable plans
  

## Recommendations 

1. Improve Customer Support Response Customers with repeated service complaints showed the highest churn tendency. Faster issue resolution and proactive follow-up can reduce dissatisfaction before customers decide to leave. 
2. Review Pricing & Billing Experience High-charge customers displayed elevated churn behavior. Introducing clearer billing structures, usage notifications, and better-value bundles may reduce pricing frustration.
3. Promote Better Plan Matching Customers using international services without suitable plans were more likely to churn. Personalized plan recommendations can improve customer satisfaction and reduce avoidable costs.
4. Prioritize High-Risk Customer Retention The risk segmentation model provides an opportunity to identify vulnerable customers early. These customers can be targeted with:  loyalty incentives, retention campaigns, personalized support or service upgrades.
5. Monitor Heavy Usage Customers More Closely High usage customers contribute significant value but also showed higher churn likelihood. Maintaining service reliability and network quality for these customers is important.

## What I learned 



### Final Conclusion

The analysis shows that churn is primarily influenced by: customer dissatisfaction, high service interaction, pricing pressure and poor service-plan alignment. By using behavioral segmentation and risk monitoring, the telecom company can proactively identify vulnerable customers and implement targeted retention strategies before churn occurs.
