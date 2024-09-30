# Bank Loan Analysis and Visualization with Power BI & SQL

Welcome to Bank Loan Data Insights, a powerful demonstration of my ability to leverage Power BI and SQL to solve critical financial challenges. This project delivers an in-depth, data-driven analysis of bank loan performance, encompassing **over 38,000 customers** and covering key aspects such as **loan approval rates, customer demographics, and financial metrics.**

The dashboards unveil vital **Key Performance Indicators, including an analysis of good vs. bad loans, detailed state-by-state trends, and comprehensive monthly performance insights.** Every result has been meticulously validated using SQL queries, ensuring the highest level of data accuracy and reliability. By transforming raw data into actionable intelligence, these insights empower informed decision-making, enabling strategic improvements that drive efficiency and optimize loan management across the financial spectrum.

**Tools:** Power Query | Dax Studio | Power BI

**RDMBS:** Microsoft SQL Server

**Approach:** ETL | Data Modeling | Data Visualization | Data Exploration  

# Problem Statement

In order to thoroughly monitor and elevate our bank’s lending performance to unprecedented levels, we are undertaking the development of a **Bank Loan Report** that meticulously analyzes **over 20 critical loan-related metrics** using **Power Query** for robust data extraction , **SQL** for data validation coupled with **Power BI** for dynamic data visualization. This innovative report will harness advanced visualization techniques, utilizing **dynamic cards for key performance indicators**, **interactive slicers for real-time filtering**, and a diverse array of chart types—including **bar charts**, **donut charts**, and **line graphs**—to facilitate agile, data-driven decision-making. By visually representing data from an extensive dataset of over **38,000 customers**, we will gain the capability to track intricate trends in **state-wise** and **month-wise loan performance**, providing an unparalleled, granular understanding of our loan portfolio and its key metrics over time.

Our ambitious goal is to create **multiple interactive dashboards** within Power BI that capture essential loan metrics, such as loan amounts, interest rates, defaults, and repayment patterns, thereby delivering a crystal-clear snapshot of the overall health of our loan book. Furthermore, these dashboards will showcase **state-specific lending trends** and monitor **monthly changes** in loan issuance and repayments, ensuring we remain responsive to market dynamics and customer needs.

The report will serve as a consolidated hub for **all critical loan parameters, integrating advanced metrics and graphical tools** to empower our team to effectively monitor lending operations. Utilizing **SQL for complex queries and data aggregation, combined with Power BI’s powerful visualization capabilities,** will enable us to identify emerging trends, optimize our portfolio performance, mitigate risks, and make strategic adjustments to enhance our lending strategies. By tapping into the full potential of our loan data, we aim to revolutionize our approach to lending, drive profitability, and achieve excellence in customer retention and satisfaction, positioning our bank as a leader in the financial services industry.

# Database Schema

Here are details of the columns from your CSV file:

**id:** A unique identifier for each loan application or customer.

**address_state:** The state where the applicant resides.

**application_type:** Specifies whether the loan is individual or joint.

**emp_length:** Length of employment of the applicant (e.g., 10+ years, 2 years, etc.).

**emp_title:** The job title of the applicant.

**grade:** Loan grade (typically represents the risk level of the loan).

**home_ownership:** Homeownership status of the applicant (e.g., rent, own, mortgage).

**issue_date:** The date the loan was issued.

**last_credit_pull_date:** The date of the most recent credit check for the applicant.

**last_payment_date:** The date the applicant last made a payment on the loan.

**loan_status:** The current status of the loan (e.g., current, default, fully paid, etc.).

**next_payment_date:** The date when the next loan payment is due.

**member_id:** A unique identifier for the applicant.

**purpose:** The reason or purpose for taking out the loan (e.g., debt consolidation, home improvement).

**sub_grade:** A more specific loan risk category within the main grade.

**term:** Loan term in months (e.g., 36 months, 60 months).

**verification_status:** Indicates whether the applicant's information has been verified.

**annual_income:** The annual income of the applicant.

**dti:** Debt-to-income ratio of the applicant, used to assess loan risk.

**installment:** The monthly payment amount for the loan.

**int_rate:** The interest rate on the loan.

**loan_amount:** The total loan amount requested or granted.

**total_acc:** Total number of credit accounts held by the applicant.

total_payment: The total amount of payments made toward the loan.
