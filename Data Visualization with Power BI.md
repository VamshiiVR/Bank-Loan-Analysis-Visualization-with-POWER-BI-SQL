# Data Visualization with Power BI

Transformed the CSV file using **Power Query,** showcasing my proficiency in data manipulation and preparation. I performed extensive data cleaning to ensure the dataset was accurate and ready for analysis. Additionally, I demonstrated advanced skills by creating a **custom date table** using Power Query, integrating it seamlessly with the loan table through meticulous **data modeling,** thereby enhancing the overall relational structure of the data model. Leveraging my deep knowledge of **DAX formulas,** I crafted several critical measures that provide invaluable insights into loan metrics, ensuring the report delivers precise and actionable information.

**Key Performance Indicators (KPIs) using Card Visual:**

**1. Total Loan Applications:** We need to calculate the total number of loan applications received during a specified period. Additionally, it is essential to monitor the Month-to-Date (MTD) Loan Applications and track changes Month-over-Month (MoM).

**2. Total Funded Amount:** Understanding the total amount of funds disbursed as loans is crucial. We also want to keep an eye on the MTD Total Funded Amount and analyse the Month-over-Month (MoM) changes in this metric.

**3. Total Amount Received:** Tracking the total amount received from borrowers is essential for assessing the bank's cash flow and loan repayment. We should analyse the Month-to-Date (MTD) Total Amount Received and observe the Month-over-Month (MoM) changes.

**4. Average Interest Rate:** Calculating the average interest rate across all loans, MTD, and monitoring the Month-over-Month (MoM) variations in interest rates will provide insights into our lending portfolio's overall cost.

**5. Average Debt-to-Income Ratio (DTI):** Evaluating the average DTI for our borrowers helps us gauge their financial health. We need to compute the average DTI for all loans, MTD, and track Month-over-Month (MoM) fluctuations.

**A few DAX Measures:**

`Total Amt Recieved = SUM(financial_loan[total_payment])` 

`PMTD Loan Applications = CALCULATE([Total Loan Applications],DATESMTD(DATEADD(Date_Table[Date],-1,MONTH)))`

`MTD avg int rate = CALCULATE(TOTALMTD([Avg interest rate],Date_Table[Date]))`

`PMTD avg int rate = CALCULATE([Avg interest rate],DATESMTD(DATEADD(Date_Table[Date],-1,MONTH)))`

`MTD Amt Received = CALCULATE(TOTALMTD([Total Amt Recieved],Date_Table[Date]))`

`MoM Loan Applications = ([MTD Loan Applications]-[PMTD Loan Applications])/[PMTD Loan Applications]`

`MoM Amt Received = ([MTD Amt Received]-[PMTD Amt Recieved])/[PMTD Amt Recieved]`

`Good Loan Total Amount Recieved = CALCULATE([Total Amt Recieved],financial_loan[Good Loan vs Bad Loan]="Good Loan")`

`Bad Loan % = ((CALCULATE([Total Loan Applications],financial_loan[Good Loan vs Bad Loan]="Bad Loan"))/[Total Loan Applications]) `

# Bank Loan Dashboard | Summary

**Good Loan v Bad Loan KPI’s**
In order to evaluate the performance of our lending activities and assess the quality of our loan portfolio, we need to create a comprehensive report that distinguishes between 'Good Loans' and 'Bad Loans' based on specific loan status criteria

**Good Loan KPIs:**
Good Loan Application Percentage: We need to calculate the percentage of loan applications classified as 'Good Loans.' This category includes loans with a loan status of 'Fully Paid' and 'Current.'
Good Loan Applications: Identifying the total number of loan applications falling under the 'Good Loan' category, which consists of loans with a loan status of 'Fully Paid' and 'Current.'
Good Loan Funded Amount: Determining the total amount of funds disbursed as 'Good Loans.' This includes the principal amounts of loans with a loan status of 'Fully Paid' and 'Current.'
Good Loan Total Received Amount: Tracking the total amount received from borrowers for 'Good Loans,' which encompasses all payments made on loans with a loan status of 'Fully Paid' and 'Current.'

**Bad Loan KPIs:**
Bad Loan Application Percentage: Calculating the percentage of loan applications categorized as 'Bad Loans.' This category specifically includes loans with a loan status of 'Charged Off.'
Bad Loan Applications: Identifying the total number of loan applications categorized as 'Bad Loans,' which consists of loans with a loan status of 'Charged Off.'
Bad Loan Funded Amount: Determining the total amount of funds disbursed as 'Bad Loans.' This comprises the principal amounts of loans with a loan status of 'Charged Off.'
Bad Loan Total Received Amount: Tracking the total amount received from borrowers for 'Bad Loans,' which includes all payments made on loans with a loan status of 'Charged Off.'

**Loan Status Grid View**
In order to gain a comprehensive overview of our lending operations and monitor the performance of loans, we aim to create a grid view report categorized by 'Loan Status.' This report will serve as a valuable tool for analysing and understanding the key indicators associated with different loan statuses. By providing insights into metrics such as 'Total Loan Applications,' 'Total Funded Amount,' 'Total Amount Received,' 'Month-to-Date (MTD) Funded Amount,' 'MTD Amount Received,' 'Average Interest Rate,' and 'Average Debt-to-Income Ratio (DTI),' this grid view will empower us to make data-driven decisions and assess the health of our loan portfolio.



