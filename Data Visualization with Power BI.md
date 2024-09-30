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

![Screenshot 2024-09-30 152904](https://github.com/user-attachments/assets/967dad66-5000-4d07-8460-2ca8acdb27cf)

**Good Loan v Bad Loan KPI’s:**
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

# Bank Loan Dashboard | Overview

![Screenshot 2024-09-30 211916](https://github.com/user-attachments/assets/6072b07c-9a04-4f03-bbfc-d0d966f149b8)

In our Bank Loan Report project, we aim to visually represent critical loan-related metrics and trends using a variety of chart types. These charts will provide a clear and insightful view of our lending operations, facilitating data-driven decision-making and enabling us to gain valuable insights into various loan parameters. The diverse chart types will enhance our ability to visualize and communicate loan-related insights effectively, supporting data-driven decisions and strategic planning within our lending operations. Below are the specific chart requirements:

**Monthly Trends by Issue Date (Line Chart):** This line chart will showcase how 'Total Loan Applications,' 'Total Funded Amount,' and 'Total Amount Received' vary over time, allowing us to identify seasonality and long-term trends in lending activities.

**Regional Analysis by State (Filled Map):** This filled map will visually represent lending metrics categorized by state, enabling us to identify regions with significant lending activity and assess regional disparities.

**Loan Term Analysis (Donut Chart):** This donut chart will depict loan statistics based on different loan terms, allowing us to understand the distribution of loans across various term lengths.

**Employee Length Analysis (Bar Chart):** This bar chart will illustrate how lending metrics are distributed among borrowers with different employment lengths, helping us assess the impact of employment history on loan applications.

**Loan Purpose Breakdown (Bar Chart):** This bar chart will provide a visual breakdown of loan metrics based on the stated purposes of loans, aiding in the understanding of the primary reasons borrowers seek financing.

**Home Ownership Analysis (Tree Map):** This tree map will display loan metrics categorized by different home ownership statuses, allowing for a hierarchical view of how home ownership impacts loan applications and disbursements.

# Bank Loan Dashboard | Details

![image](https://github.com/user-attachments/assets/b311ce29-ebbb-4d43-a9e0-2cff25660832)

The primary objective of the Details Dashboard using the **table visual** is to provide a comprehensive and user-friendly interface for accessing vital loan data. It will serve as a one-stop solution for users seeking detailed insights into our loan portfolio, borrower profiles, and loan performance.
 





