# Analysing Diabetic Patient Data for Predictive Healthcare


## Table of Contents
- [Introduction](#introduction)
  
- [Project Goals](#project-goals)
  
- [Database Design and Tools](#database-design-and-tools)
  
- [Data Collection](#data-collection)
  
- [ER Diagram and Database Schema](#er-diagram-and-database-schema)
  
- [Data Analysis Tools](#data-analysis-tools)
  
- [Data Cleaning](#data-cleaning)
  
- [Model Results](#model-results)
  
- [Visualizations](#visualizations)
  
- [Findings and Discussion](#findings-and-discussion)

- [Appendix](#appendix)

## Introduction
This project leverages two large Kaggle datasets to analyze data from diabetic patients. The aim is to develop predictive models that reduce hospital readmissions, lower healthcare costs, and enhance treatment quality for individuals with diabetes. This analysis focuses on key factors such as patient demographics, laboratory test results, medications, and risk factors, paving the way for personalized treatment recommendations.

## Project Goals
The main objectives of this project are as follows:
- **Prioritizing hospital readmissions:** Focus on diabetes patients as a key healthcare quality metric to reduce overall costs.
- **Data Analysis:** Analyze data from two datasets—"diabetes-dataset-2019" and a 10-year "diabetes" dataset.
- **Predictive Modeling:** Develop models to identify patients who could benefit from targeted interventions and reduction policies.
- **Cost Reduction and Quality Enhancement:** Use insights from the indicators to minimize healthcare expenditure, reduce readmission rates, and enhance treatment quality.
- **Data-Driven Visualizations:** Create interactive visualizations to effectively communicate advanced insights.

## Database Design and Tools
- **Database Design:**  
  I utilized MySQL, a robust and widely established relational database management system, to store and retrieve our diabetic patient datasets. phpMyAdmin is employed for efficient management. Our database schema is designed in accordance with the Third Normal Form (3NF), ensuring data integrity and minimal redundancy.

  ![Database](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/ca314bbe9e42b99a165a1815af24c32452438955/Database_project/Images/phpdatabase.jpg)

- **Data Analysis:**  
  Python is used for data analysis within a Jupyter Notebook environment, allowing for efficient data manipulation, statistical analysis, and model building.
  
- **Data Visualization:**  
  Tableau is used to develop interactive visualizations that aid in the communication and interpretation of our key findings.

## Data Collection
Two datasets have been collected from Kaggle:
- **DATASET 1: "10-YEARS-DIABETES-DATASET"**  
  Contains information about patient admissions, medications, and laboratory tests.  
  Dataset Link: [10-Years Diabetes Dataset](https://www.kaggle.com/datasets/jimschacko/10-years-diabetes-dataset?resource=download)
  
- **DATASET 2: "DIABETES-DATASET-2019"**  
  Contains information about patient risk factors.  
  Dataset Link: [Diabetes Dataset 2019](https://www.kaggle.com/datasets/tigganeha4/diabetes-dataset-2019)

## EntityRelation Diagram and Database Schema
- **Entities:**  
  The ER diagram for this project includes four major entities:
  - **Patient Details**
  - **Admission Records**
  - **Laboratory Tests**
  - **Risk Factors & Key Medications**
- **Relationships:**  
  The diagram illustrates one-to-many and one-to-one relationships. For example, one patient admission record may be linked to multiple medication entries or risk factor assessments.
- **Attributes:**  
  Each entity is depicted using rectangles, while attributes are represented as ovals.
<img src="https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/ca314bbe9e42b99a165a1815af24c32452438955/Database_project/Images/DBSchema.jpg" width=50% height=50%> <img src="https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/ca314bbe9e42b99a165a1815af24c32452438955/Database_project/Images/ERD.jpg" width=40% height=40%>

## Data Analysis Tools
- **Platform:**  
  Jupyter Notebook is used as the primary platform for coding and analysis in Python.
- **Workflow:**  
  - Load CSV files and inspect for null values.
  - Drop columns with significant missing data.
  - Differentiate between numeric and categorical variables.
  - Generate subplots for numeric variables to observe their distributions.
  - Apply log transformations to variables that are not normally distributed.
 
    

## Data Cleaning
- **Missing Data Imputation:**  
  The primary strategy for data cleaning involves using the `fill` function to impute NaN values where possible.
- **Quality Check:**  
  After cleaning, we verify data integrity by ensuring that the sum of null values is minimal before proceeding to further analysis.

![data cleaning process here](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/ca314bbe9e42b99a165a1815af24c32452438955/Database_project/Images/Datacleaning.png)

## Model Results
For complete code files, please refer to the [GitHub repository](https://github.com/yourusername/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare).

- **Key Findings:**  
  - Models have been developed to predict which patients are at high risk of poorly controlled diabetes and subsequent hospital readmissions.
  - The predictive models demonstrate strong performance, highlighting critical factors that influence readmission risks.

## Visualizations
![Tableau visualization](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/db1a48e578b7028e6a603b541d2562e5d56c891e/Database_project/Tableau%20Visualizations%20at%20glance.jpg)

- **Visualization Insights:**  
  Key findings include:
- Predictive models that identify high-risk patients for hospital readmission.
- Significant predictors include patient age, prior admissions, laboratory test results, and medication usage.
- Logistic regression analysis revealed that patients on insulin therapy were 2.41 times more likely to experience 30-day readmission, after controlling for other factors.

Interactive visualizations summarize the core insights:
- **Admission Types:**  
  A bar chart visualizes the frequency distribution of different admission types, providing insight into patient visit patterns.

  ![Admission Types Chart](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/a80bd4341a7070a37d32061a103033d5f295f3fa/Distribution%20of%20Admission%20Types.png)

- **Readmission Status:**  
  A pie chart displays the proportion of patients readmitted, not readmitted, or readmitted after 30 days.

  ![Readmission Status Pie Chart](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/a80bd4341a7070a37d32061a103033d5f295f3fa/Readmission%20Status.png)

- **Health Metrics:**  
  Histograms depicting the distributions of Body Mass Index (BMI) and number of pregnancies provide additional context for risk assessment.

  ![BMI and Pregnancies Histogram](https://github.com/asmatahasin/Analysing-Diabetic-Patient-Data-for-Predictive-Healthcare/blob/55e2bbba617470efc48012a987cf551edfdc4b95/BMIPregnencies.png)

## Findings and Discussion
- **Insights:**  
  - Older patients and those with a history of frequent admissions are at a higher risk of readmission.
  - The data indicates that patients on insulin therapy have significantly higher odds of 30-day readmission.
  - Visualizations support these findings and offer clear, actionable insights for personalized patient care.
  
- **Healthcare Implications:**  
  - An optimized database and predictive model can lead to better management of diabetes care.
  - Proactive interventions based on these insights could lower readmission rates and improve overall patient outcomes.
  - Ongoing refinement of the predictive models and visualizations will further enhance decision-making processes in clinical settings.



## Appendix: SQL Query Optimization and Data Integration
Key elements from the project report include:

- **Attributes Used for Analytics:**  
  Critical attributes include patient demographics (age, gender), admission details, BMI, blood pressure, medication types, laboratory results, diagnoses, comorbidities, HbA1c levels, and prior outpatient/ER visits.

- **Query Optimization Techniques:**  
  - **Indexing:** Added indexes on `patientID` across all tables to improve JOIN performance.
  - **Selective Columns:** Modified queries to select only the necessary columns.
  - **Filtering:** Early application of `WHERE` clauses to reduce the dataset size during query execution.

- **Data Integration:**  
  An ETL process standardized data formats, resolved inconsistencies, and ensured referential integrity across integrated datasets. This approach facilitated robust analytics and seamless visualization updates.

These methods collectively enhanced the performance of our data retrieval and analysis pipelines, ensuring reliable and timely insights.

---

