# Clinical Trial SQL Analysis Pipeline

This repository showcases a SQL-based project that simulates the design, population, and analysis of a clinical trial dataset. It focuses on evaluating treatment efficacy, demographic trends, and medical condition impacts using structured queries.

## Project Overview
This SQL pipeline performs:
- Creation of a patient clinical trial table
- Insertion of synthetic trial data
- Data cleaning and transformation
- Exploratory queries to identify patterns across treatment outcomes, comorbidities, and patient attributes

## Table Schema: `Trial_1_Data`
| Column Name       | Data Type      | Description                             |
|-------------------|----------------|-----------------------------------------|
| PatientID         | INT            | Unique patient ID                       |
| Age               | INT            | Age of the participant                  |
| Sex               | VARCHAR(6)     | Biological sex                          |
| Treatment         | VARCHAR(11)    | Treatment group (A/B)                   |
| EfficacyScore     | DECIMAL(4,2)   | Treatment response score (0–10 scale)   |
| SideEffect        | VARCHAR(3)     | 'Yes' or 'No'                           |
| BloodPressure     | VARCHAR(10)    | e.g., '120/80'                          |
| DateVisited       | DATE           | Date of clinical visit                  |
| BMI               | DECIMAL(5,2)   | Body Mass Index                         |
| Cholesterol       | INT            | Blood cholesterol level (mg/dL)         |
| SmokingStatus     | VARCHAR(10)    | Smoker / Non-smoker                     |
| DiabetesStatus    | VARCHAR(3)     | 'Yes' or 'No'                           |
| FamilyHistory     | VARCHAR(3)     | Family history of disease               |
| Ethnicity         | VARCHAR(20)    | Reported ethnicity                      |
| EducationLevel    | VARCHAR(20)    | e.g., 'Graduate', 'High School'         |
| Occupation        | VARCHAR(20)    | Profession                              |

## SQL Workflow Steps

### Create and Populate Table
- Create the `Trial_1_Data` table
- Insert 10+ patient records with diverse attributes

### Data Cleaning & Updating
- Rename column `Gender` to `Sex`
- Update cholesterol and side effect status conditionally using `CASE` and `WHERE`

### Exploratory Data Analysis (EDA)

#### Q1: Treatment Efficacy
```sql
SELECT Treatment, AVG(EfficacyScore), COUNT(*) FROM Trial_1_Data GROUP BY Treatment;
```

#### Q2: Education Distribution by Treatment
```sql
SELECT Treatment, EducationLevel, COUNT(*) FROM Trial_1_Data GROUP BY Treatment, EducationLevel;
```

#### Q3: Smoking vs Efficacy
```sql
SELECT SmokingStatus, AVG(EfficacyScore) FROM Trial_1_Data GROUP BY SmokingStatus;
```

#### Q4: Sex-based Outcomes
```sql
SELECT Sex, AVG(EfficacyScore) FROM Trial_1_Data GROUP BY Sex;
```

#### Q5: Diabetes Status Impact
```sql
SELECT DiabetesStatus, AVG(EfficacyScore) FROM Trial_1_Data GROUP BY DiabetesStatus;
```

#### Q6: Ethnicity and Treatment Outcomes
```sql
SELECT Ethnicity, Treatment, AVG(EfficacyScore) FROM Trial_1_Data GROUP BY Ethnicity, Treatment;
```

#### Q7: Age-wise Treatment Preference
```sql
SELECT Age, Treatment, COUNT(*) FROM Trial_1_Data GROUP BY Age, Treatment;
```

## Example Results
| Treatment   | Avg Efficacy | Sample Size |
|-------------|--------------|-------------|
| Treatment A | 8.1          | 5           |
| Treatment B | 6.3          | 6           |

## Applications
- Simulated trial reporting
- Healthcare analytics training
- Interview-ready SQL case
- Foundation for data dashboarding

## Tools Used
- SQL Server / PostgreSQL / MySQL
- SQL IDEs (DBeaver, Azure Data Studio, pgAdmin)
- Sample generation via static `INSERT` scripts

## License
MIT License – free for academic, personal, and professional use.
