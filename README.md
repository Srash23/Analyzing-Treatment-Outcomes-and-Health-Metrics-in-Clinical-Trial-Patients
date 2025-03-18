# Clinical Trial Data Analysis Using SQL

### Introduction

This study explores the differences in treatment outcomes and side effects among patients receiving different treatments. By analyzing demographic and health-related factors such as age, sex, smoking status, diabetes status, cholesterol levels, BMI, and education level, we aim to identify significant correlations and disparities. The study involves creating a structured database, inserting patient data, and performing a series of SQL queries to extract meaningful insights.
![_- visual selection](https://github.com/user-attachments/assets/9d81f400-eb65-4e33-9ea3-d4eb3fa6b59d)

### Why is This Analysis Important?

1. Improves Clinical Decision-Making: Identifies patterns in treatment efficacy based on demographic and health factors.
2. Personalized Medicine: Helps tailor treatments based on patient profiles to maximize efficacy and minimize side effects.
3. Public Health Insights: Provides data-driven evidence to address healthcare disparities and optimize treatment strategies.

### Installation and Usage (For End-Users)

1. Install MySQL or any other SQL-compatible database.

2. Open your SQL client and create a new database.

3. Run the provided SQL script to create the Trial_1_Data table and insert patient records.

4. Execute the analysis queries to gain insights into treatment outcomes.

### Installation and Usage

Clone the repository:

1. git clone https://github.com/Srash23/SQL-Clinical-Trial-Analysis.git

2. Open the SQL script in an SQL editor (e.g., MySQL Workbench, PostgreSQL, SQLite, etc.).

3. Modify or extend the queries to explore additional insights.

4. Submit pull requests for any improvements or additional analyses.

### Methodology

#### Step 1: Creating the Database Table

Defines Trial_1_Data table with attributes like PatientID, Age, Sex, Treatment, EfficacyScore, SideEffect, and other health-related factors.

#### Step 2: Inserting Data

Populates the table with sample patient records reflecting diverse demographic and clinical profiles.

#### Step 3: Data Processing

Modifies table structure (e.g., renaming columns, updating values based on conditions).

#### Step 4: Exploratory Data Analysis

We investigate multiple research questions using SQL queries:
1. **Comparing Treatment Efficacy:** Determines if there is a significant difference between Treatment A and Treatment B efficacy scores.
2. **Education Levels and Treatment Distribution:** Examine if education level influences treatment selection.
3. **Smoking Status and Treatment Efficacy:** Analyzes whether smoking impacts treatment outcomes.
4. **Sex-Based Differences in Outcomes:** Evaluates if treatment efficacy varies based on sex.
5. **Diabetes and Treatment Outcomes:** Identifies if diabetes affects treatment efficacy.
6. **Ethnic Disparities in Treatment Response:** Determines whether different ethnic groups respond differently to treatments.
7. **Age and Treatment Preferences:** Explores how age influences treatment choices.

### Results and Discussion
#### Treatment A vs. Treatment B:
Aggregated results indicate whether one treatment is more effective than the other.

#### Demographic Influence on Treatment Outcomes:
Identifies any disparities in treatment efficacy across different age groups, ethnicities, and health conditions.

#### Predictive Indicators:
Highlights potential factors influencing treatment success or failure.

### Conclusion

This SQL-based clinical trial analysis demonstrates how structured data management and querying can reveal crucial insights into treatment efficacy and patient demographics. These findings can help optimize medical treatment plans and support data-driven healthcare decisions.
