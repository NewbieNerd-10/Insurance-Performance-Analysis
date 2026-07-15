Insurance Analysis Dashboard
Dashboard Link:
https://app.powerbi.com/links/MeX-DTKKCv?ctid=a90703de-3b25-4520-a41b-56a6f50dff03&pbi_source=linkShare

Problem Statement

This dashboard helps insurance companies analyze policy performance, customer demographics, premium collections, and claim settlements. It enables insurers to monitor key business metrics, identify customer segments, evaluate claim trends, and improve decision-making through data-driven insights.
The dashboard provides an overview of policy distribution, premium income, claim amounts, customer demographics, and policy status. Using interactive visualizations, stakeholders can identify business opportunities, optimize insurance products, and improve customer satisfaction.

Steps Followed
Step 1: Loaded the Insurance dataset into Power BI Desktop.
Step 2: Opened Power Query Editor and enabled Column Quality, Column Distribution, and Column Profile to understand the dataset.
Step 3: Selected Column Profiling Based on Entire Dataset for complete data validation.
Step 4: Verified data types and handled missing or null values where required.
Step 5: Removed duplicate records and cleaned inconsistent data to improve data quality.
Step 6: Applied a suitable Power BI theme to enhance dashboard appearance.
Step 7: Added slicers for interactive filtering, including:
Insurance Type
Gender
Age Group
Policy Status
Claim Status
Region
Policy Year
Step 8: Created KPI Cards to display:
Total Policies
Total Premium Amount
Total Claim Amount
Total Customers
Average Premium
Claim Settlement Rate
Step 9: Created bar and column charts to analyze:
Premium by Insurance Type
Claims by Insurance Type
Policies by Region
Policies by Gender
Step 10: Created line charts to visualize premium collection and claim trends over time.
Step 11: Added pie and donut charts to represent:
Policy Status
Claim Status
Insurance Type Distribution
Step 12: Added report title, company logo, and dashboard branding using text boxes, images, and shapes.
Step 13: Created calculated columns where required.
Example DAX:
Age Group =
IF(Insurance[Age] <= 25, "18-25",
IF(Insurance[Age] <= 40, "26-40",
IF(Insurance[Age] <= 60, "41-60",
"60+")))
Step 14: Created measures for key performance indicators.
Example:
Total Policies =
COUNT(Insurance[Policy ID])
Total Premium =
SUM(Insurance[Premium Amount])
Total Claim Amount =
SUM(Insurance[Claim Amount])
Average Premium =
AVERAGE(Insurance[Premium Amount])
Claim Settlement Rate =
DIVIDE(
CALCULATE(
COUNT(Insurance[Policy ID]),
Insurance[Claim Status]="Settled"
),
COUNT(Insurance[Policy ID])
)*100
Step 15: Published the report to Power BI Service.
Snapshot of Dashboard (Power BI Service)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/db27915d-963d-4e5c-814a-1982b748227b" />

Report Snapshot (Power BI Desktop)

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/f46531f1-0f60-4fbd-beb3-9c44493136a3" />

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/f40232d4-dade-42ce-8522-447a81578a5b" />

Insights

A single-page interactive dashboard was created using Power BI Desktop and published to Power BI Service.

The following business insights can be derived from the dashboard.

[1] Policy Overview

The dashboard displays:

Total Number of Policies
Total Customers
Total Premium Collected
Total Claim Amount
Average Premium
Claim Settlement Rate

These KPIs provide an overall view of the insurance business performance.

[2] Premium Analysis

The dashboard analyzes:

Premium collected by insurance type
Premium collected across regions
Premium contribution by customer segments

This helps identify the most profitable insurance products.

[3] Claims Analysis

The dashboard provides insights into:

Total Claim Amount
Claim Status Distribution
Settled vs Pending Claims
Claims by Insurance Type

This helps evaluate claim management efficiency.

[4] Customer Demographics

Customer analysis includes:

Gender-wise policy distribution
Age Group distribution
Region-wise customer distribution

These insights help understand the target customer base.

[5] Insurance Type Analysis

The dashboard compares different insurance categories such as:

Health Insurance
Life Insurance
Vehicle Insurance
Home Insurance
Travel Insurance

This enables stakeholders to identify the most preferred insurance products.

[6] Regional Analysis

The dashboard highlights:

Policies by Region
Premium Collection by Region
Claim Amount by Region

This helps identify high-performing markets and regions requiring business improvement.

[7] Policy Status Analysis

The dashboard visualizes policy status such as:

Active Policies
Expired Policies
Renewed Policies
Cancelled Policies

These insights help monitor customer retention and renewal performance.

[8] Interactive Filtering

Users can dynamically analyze insurance data using filters such as:

Insurance Type
Gender
Age Group
Region
Policy Status
Claim Status
Policy Year

All dashboard visuals update automatically based on selected filters.

Business Benefits

Monitor overall insurance business performance.
Analyze premium collection and claim settlements.
Identify profitable insurance products.
Understand customer demographics and regional performance.
Improve claim management and policy renewal strategies.
Support strategic business decisions through interactive data visualization.

