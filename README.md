# Global-Bank_-Churn-Analysis
   ##The Business Problem 
   
   The bank is experiencing a substantial customer attrition rate. Out of 10,000 active accounts, 
2,670 customers have left the bank, resulting in a churn rate of 26.7%. With an overall 
portfolio valuation of $25 Million in Total Charges, this high churn rate represents millions of 
dollars in lost or at-risk revenue. Management lacked clear visibility into why customers 
were leaving, which segments posed the highest financial risk, and what operational 
adjustments could prevent future losses. 

Dataset used:
- <a href="https://github.com/abhinagendramangalapally-oss/Global-Bank_-Churn-Analysis/blob/main/Bank_Churn.xlsx">GlobalBank ChurnAnalysis Dataset</a>

 GlobalBank ChurnAnalysis Dashboard:
  - <a href="https://github.com/abhinagendramangalapally-oss/Global-Bank_-Churn-Analysis/blob/main/churn%20analysis.pbit">GlobalBank Interactive Dashboard</a>

##Key Findings 

-> Contract Vulnerability: Customers on short-term Monthly Contracts are the 
dominant drivers of churn. 
-> The Critical First Year: Customer attrition peaks heavily within the New Customer 
bracket (0–12 months of tenure). 
-> Payment Friction: Customers utilizing manual or less integrated payment methods 
exhibit disproportionately higher churn rates than those on automated billing. 
->Financial Risk Exposure: A substantial portion of the bank’s $25M portfolio sits in 
high-risk categories, requiring immediate, targeted proactive marketing 
interventions. 
Dashboard Image View:
-<a href=" https://github.com/abhinagendramangalapally-oss/Global-Bank_-Churn-Analysis/blob/main/Global%20bank%20churn%20analysis.png.png">>GlobalBank Dashboard ImageView</a>

##2. Business Objective 

##Why Customer Churn Matters

Every customer who closes their account takes away recurring monthly fees, loan potentials, 
and transaction volumes. Furthermore, replacing a customer costs up to 5 times more in 
marketing and onboarding expenses than keeping an existing one happy. 

##Business Value of this Analysis 

This project transforms raw transactional and demographic data into a strategic asset. By 
identifying exactly where the bank is losing customers, leadership can: 
1. Shift from reactive firefighting to proactive retention. 
2. Optimize marketing budgets by targeting only the high-risk, high-value segments. 
3. Design tailored product adjustments (e.g., promotional long-term contracts) that 
address customer pain points before they exit.

##3. Data Preparation & Engineering 
To ensure data integrity, the raw dataset underwent comprehensive cleaning and feature 
engineering using Power Query within Excel and Power BI. 
• Data Cleaning & Profiling: Handled missing data points, eliminated duplicate rows, 
and verified data types (e.g., ensuring financial charges were explicitly formatted as 
currency). 
• Feature Engineering (Calculated Columns): * Tenure Grouping: Segmented raw 
tenure numbers into clean, actionable business groups: New customer (0–12 
months), Regular customer (13–36 months), and Loyal customer (37+ months). 
o Charges Grouping: Categorized Monthly Charges into Low, Med, and High 
brackets to assess if pricing structures were forcing customers away. 
• DAX Measures Implementation: Built a robust metrics layer to power the dashboard 
visuals dynamically: 
o Total Customers = COUNT (Bank_Churn [CustomerID]) 
o Total Churn = CALCULATE (COUNT (Bank_Churn [CustomerID]), Bank_Churn 
[Churn] = 1) 
o Churn Rate =DIVIDE ([Total Churn], [Total Customers], 0)

##5. Dashboard Overview
   
The final product is a single-page executive-level analytical dashboard built in Power BI, 
optimized for intuitive navigation. 
• Executive KPI Cards: Placed prominently at the top left to instantly give stakeholders 
the high-level health metrics: Total Customers (10,000), Churned Customers (2,670), 
Churn Rate (26.7%), and Total Portfolio Value ($25M). 
• Interactive Global Filters (Slicers): Enabled filtering by Gender, Senior Citizen Status, 
Contract Type, and Risk Segment, allowing regional managers to slice the data to 
match their specific operating parameters. 
• Visual Layout Strategy: * Left side focuses on demographics and contract 
breakdowns (Who is leaving?). 
o Center focus tracks tenure and risk segments (When and how severely are 
they leaving?). 
o Right side focuses on financial values and payment structures (What is the 
revenue cost?). 

###A. Churn by Contract Type 
• Insight: Over 75% of all churned customers belong to the Monthly Contract 
segment. Customers locked into One-Year or Two-Year contracts show remarkably 
stable retention rates. 
• Management Takeaway: Short-term flexibility is hurting our bottom line. Customers 
without a long-term commitment view our services as transactional rather than 
relational. 
##B. Churn by Tenure Group (The First-Year Drop-Off) 
• Insight: Attrition is heavily concentrated among New Customers (those with less 
than 12 months with the bank). Once a customer crosses the 3-year (Loyal) mark, 
their propensity to churn drops to single digits. 
• Management Takeaway: Our onboarding experience or initial expectations are 
failing. The first 90 to 180 days are critical; if we don't engage them deeply there, we 
lose them entirely. 
##C. Churn by Risk Segment 
• Insight: The data engine classified a significant pool of customers under the High Risk 
segment, showing an overlap where high monthly charges correspond with declining 
transaction frequencies. 
• Management Takeaway: High-paying customers are highly sensitive to fee increases 
or perceived poor service quality. 
##D. Churn by Payment Method 
• Insight: Customers paying via manual methods (like Mailed Checks) churn at a 
significantly higher rate compared to those who set up automated billing options like 
Bank Transfers or Credit Cards. 
• Management Takeaway: Manual payment options introduce a monthly "decision 
point" where the customer consciously reflects on whether they want to keep 
spending money with us. Automated billing removes this friction. 

##9. Strategic Recommendations 
Based on the insights derived from the dashboard, the following data-informed initiatives 
are recommended to executive management: 
1. Introduce an Automated Billing Incentive Program: Launch a targeted campaign 
offering a one-time statement credit (e.g., $10) or small interest-rate perk to any 
monthly customer who switches from check/manual payments to automatic bank 
transfers or credit cards. 
2. Optimize the Onboarding Journey: Task the customer experience team with building 
a "First 100 Days" Nurture Track. Introduce proactive check-in calls at Month 3 and 
Month 6 for all new accounts to solve friction points early. 
3. Incentivize Long-Term Contracts: Transition existing Monthly Contract users to 
Annual Agreements by offering a bundled discount on monthly account maintenance 
fees. The upfront discount is heavily outweighed by the guaranteed retention value. 
4. Proactive Attrition Alerts for High-Risk Groups: Establish a process where account 
managers receive a flag when a customer falls into the "High Risk" segment, 
triggering immediate outreach with personalized relationship-retention offers.

##7. Realized Business Impact
   
By deploying this BI framework across operations, leadership gains immediate business 
advantages: 
• Speed to Decision: Removes guesswork. Executives can immediately see which 
segments are failing month-over-month without waiting for delayed manual 
spreadsheets. 
• Revenue Protection: Safekeeping even 5% of the currently churned high-value 
segment translates directly into hundreds of thousands of dollars saved in pure top
line revenue. 
• Targeted Resource Allocation: Instead of wasting marketing funds running blanket 
retention campaigns for all 10,000 customers, the bank can precisely direct its 
spending toward the vulnerable 2,670 group. 

##9. Core Technical Skills Demonstrated 
• Data Preparation (Excel/Power Query): Applied robust data profiling, addressed 
missing values, removed system anomalies, and engineered clean business 
dimensions. 
• Data Modeling & DAX Engine: Developed an efficient relational schema and wrote 
clean, well-commented DAX formulas to build dynamic business metrics. 
• Data Visualization & Storytelling (Power BI): Designed an intuitive, high-contrast, 
uncluttered dashboard interface following corporate UI design principles. 
• Business Translation: The ability to look at complex, segmented transactional data 
rows and extract clear, actionable initiatives that non-technical CEOs can confidently 
fund.

##11. Project Conclusion & Next Steps 

This project successfully bridges the gap between raw data and corporate execution. By 
illuminating the vulnerabilities in monthly contracts, manual payment structures, and early 
tenure lifecycle stages, the analysis hands the business a literal playbook for protecting its 
revenue portfolio. 
Future Enhancements 
• Predictive Machine Learning Integration: Integrate a Python or Azure ML model to 
generate a real-time probability score directly inside the dashboard, predicting 
exactly which individual customer is likely to leave next. 
• Customer Sentiment Integration: Layer in CSAT/NPS feedback data to see how 
customer complaints correlate with sudden churn spikes.
