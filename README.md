This dashboard analyzes the current state of India’s job market using layoffs, unemployment, and competition data. Rising layoffs across sectors, increasing unemployment rates, and intense competition for limited job opportunities are creating a high-stress environment for job seekers. The combined effect of these factors is captured by the Stress Index, visually highlighting why the job market feels challenging and unstable. The analysis shows that the ‘crash’ perception is largely due to demand-supply imbalance rather than a shortage of talent, emphasizing the need for strategic career planning, upskilling, and mental resilience.
Dataset Overview – India Job Market Analysis
1️⃣ India_Unemployment.csv

Source: Kaggle / Government Open Data (Ministry of Labour & Employment / Periodic Labour Force Survey)

Rows / Columns: ~48 rows × 2 columns

Columns:

Month → Date (YYYY-MM)

Unemployment_Rate → Percentage of unemployed population

Sheets: Single sheet CSV

Data Notes: Monthly unemployment data for India (2022–2025)

Usage in Dashboard: Line chart (Unemployment Trend), Average Unemployment KPI

2️⃣ India_Layoffs.csv

Source: Kaggle / News aggregated company layoffs data

Rows / Columns: ~120 rows × 3 columns

Columns:

Company → Name of the company

Year → Year of layoffs

Layoffs_Count → Number of employees laid off

Sheets: Single sheet CSV

Data Notes: Year-wise layoffs for top companies

Usage in Dashboard: Line chart (Layoffs Trend), Total Layoffs KPI, Stress Index

3️⃣ India_JobCompetition.csv

Source: Kaggle / Job portals aggregated data

Rows / Columns: ~200 rows × 3 columns

Columns:

Job_Role → Name of job role

Month → Date of job posting

Competitors → Avg applicants per job

Sheets: Single sheet CSV

Data Notes: Shows average number of applicants competing per job role

Usage in Dashboard: Line chart (Competition Trend), Avg Competition KPI, Stress Index

Data Modeling / Relationships

Date Table: Central table created in Power BI (Date_Table)

Columns: Date, Year, MonthNumber, Month, Quarter

Relationships:

Main Table	Column	Date Table	Column	Type
India_Unemployment	Month	Date_Table	Date	Many-to-One
India_Layoffs	Year	Date_Table	Year	Many-to-One
India_JobCompetition	Month	Date_Table	Date	Many-to-One

Reasoning: Date Table acts as common “spine” to allow time-based trends across datasets.
