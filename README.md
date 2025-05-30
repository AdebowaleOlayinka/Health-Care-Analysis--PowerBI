# Health Care Analysis 
![medical-banner-with-doctor-wearing-goggles_23-2149611193](https://github.com/user-attachments/assets/a8b2ce65-8ee4-406f-b793-1f17f67873cf)

 ## Table of Contents   
- [About Project](#about-project)
- [Dataset Overview](#dataset-overview)
- [Problem Statement](#problem-statement)
- [Technique Applied](#technique-applied)
- [Data Cleaning](#data-cleaning)
- [Dax Measures](#dax-measures)
- [Dashboard](#dashboard)
- [Insight](#insight)
- [Recommendations](#recommendations)

## About Project
The Health Care project contains a dataset of 55,500 record of patients from 10 major hospitals across the U.S. It captures a view of hospital admission, Medical conditions, medications, Insurance provider and treatment cost. The goal is to uncover insight that can drive better health care decisions, optimize cost and improve patient outcomes.

## Dataset Overview
- **Record**: 55,500 Patients
- **Column Field**: Age, Gender, Blood Type, Medical Conditions, Admission and Discharge Date, Hospital, Billing Amount, Test Results, Insurance Provider
- **Data Source**: Onyx Dataset

## Problem Statement 
1. What are the most common age group, gender and blood type among patient?
2. What medical conditions are diagnosed most frequenly?
3. How long do patient stay and what affect it?
4. How much does treament cost by condition and admission type?
5. How do hospital compare in terms of patient treated and outcomes?
6. What medications are commonly used?
7. How do admission type impact stay and cost?
8. Which insurance provider cover the most patient?

## Technique Applied 
- Data Cleaning and Transformation
- Dax calculations and kpi
- Visualization

## Data Cleaning 
The data set was cleaned in powerBI and dax calculations and kpi was generated

- Created a new Column for Age category and length of stay

## Dax Measures 
Dax was performed to generate the kpi for the following

- Total patient
```
Total patient= Distinct count('Health care data'[Patient ID])
```
- Billing Amount
```
Billing Amount= Sum('Health care data'[Billing Amount])
```
- Average Billing Amount
```
Average Billing Amount= Average('Health care data'[Billing Amount])
```
- Length of stay
```
Length of stay= DateDiff('Health care data'[Date of admission],'Health care data'[Discharge date],Day)
```
- Average Stay
```
Average stay= Average('Health care data'[Length of stay])
```

## Dashboard 
The power BI dashboard consist of two pages 
#### Page 1
- Patient Demographics (Age, Blood type and Gender)
- Patient Admission type
- Medical Test results by Hospital
- Most diagnosed condition

#### Page 2
- Most used medication
- Length of stay by admissions type
- Total patient by Insurance provider
- Average Billing amount by Medical condition


![Health Care Dashboard Page1](https://github.com/user-attachments/assets/68feec48-5be0-412b-b0c8-fd2b7ca908a9)

![Health Care Dashboard page 2](https://github.com/user-attachments/assets/7505a59d-f33b-4214-a14d-d9c48d4c7c67)

## Insight 
- **Patient Demographic**: Patient aged 66+ form the largest group of patients highlighting that Elderly are the most frequent users of the hospital services
- **Gender & Blood type distribution**: A+ blood type is most common among patients noticebly higher numbers of female patients(11,100) compared to male(6,660)
- **Hospital based on test outcomes**: Houston Methodist Hospital has the highest number of patients with highest test results
- **Most diagnosed condition**: The top 3 most diagnosed condition are Diabetes, Hypertension and Obesity affecting over 40,000 patients
- **Medication**: Ibuprofen is the most used medication by patients accounting for 20.05% usage
- **Insurance Provider**: Medicare insurance provider covers over 50% of patients
- **length of stay by treatment cost and admission type**: Elective admission lead to the highest treatment cost of $25,602 with the average stay of 15.5 days
- Emergency lead with the highest stay if 15.6 days and urgent admission with 15.4 days

### check the interactive dashboard [click Here](https://app.powerbi.com/view?r=eyJrIjoiYjVkYmNjOTAtYTMzYS00NWEwLTk0YmEtODBjMjA3ZjcxMmI1IiwidCI6IjUzYjJmMWM0LWNiNjItNDc2MC04OTgyLWU4NGJmMDMwNmM4MiJ9)

## Recommendations 
- Introduce Patients monitoring apps for remote tracking of vital sign of blood sugar and blood pressure
- Address common issues like diabetes through awareness and education
- Introduce preventative health care packages to create affordable check up plans targeting adults and elderly patients to detect issues early 
