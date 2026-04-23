# Excel _Project-Data Analytics
Project 1 Excel Salary Dashboard  

<img width="1292" height="1020" alt="Recording 2026-04-22 at 16 45 53" src="https://github.com/user-attachments/assets/61c4c869-9944-44fc-afa4-4a252d906100" />  

## Introduction  

I created this data jobs salary dashboard to help me investigate salaries and markets for my desired jobs and enusre that I have a true picture of adequate compensation. 

This data sourced from various job platforms provided a foundation in analyzing data using this powerful tool. The data contains information on job titles, salaries, locations, and essential skills.  

## Dashboard File  
My Final dashboard is in [Project_One_Excel.xlsx](Project_One_Excel.xlsx)

Excel Skills Used  

I used the following Excel Skills for analysis:  

* 📉 Charts
* 🧮 Formulas and Functions
* ❎ Data Validation

## Data Jobs Dataset  

The dataset I used in this project containsreal-world data science job information from 2024. It contains detailed information on:   
* Job Titles
* Salaries
* Locations
* Skills

Dashboard Build  

Charts  
Data Science Job Salaries -Bar Chart  
<img width="462" height="272" alt="Data Science Job-Bar Chart" src="https://github.com/user-attachments/assets/5b9d749d-ae52-46f7-b582-4864a4632c89" />  
*Excel Features: Utilised bar chart feature (with formatted salary values) and optimised layout for clarity.  
* Design Choice: Horizontal bar chart for visual comparison of median salaries.
* Data Organization: Sorted job titles by descending salary for improved readability.
* Insight Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

  Country Median Salaries- Map Chart
  
  <img width="486" height="273" alt="Country Median Salaries-Maps" src="https://github.com/user-attachments/assets/eb64875e-2c1d-4762-a31a-f36da1c62de6" />
  *Excel Features: Utilised Excel's map chart features to plot median salaries globally.
  * Design Choice: Color-coded map to visually differentiate salary levels across regions.
  * Data Representation: Plotted median slary for each country with available data.
  * Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
  * Insights Gained: Enbale quick grasp of global slary disparitiesan highlights high/low salary regions.
 
    Formulas and Functions

    Median Slary by Job Titles

   $$=MEDIAN(
     IF(
       (jobs[job_title_short]=A2)*
       (jobs[salary_year_avg]<>0)*
       (jobs[job_country]=country)*
       (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
        jobs[salary_year_avg]
        )
 
 )$$  
 * Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
 * Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
 * Tailore Insights: Provides specific salary information for job titles, regions, andschedule types.
 * Formula Purpose: This formula populates the table below, returning the median salary based on job title, country and type.

   Background Table
   <img width="342" height="280" alt="Med-Sal" src="https://github.com/user-attachments/assets/de848e70-7a54-49b5-97ee-726fdebb1487" />
   
 Dashboard Implementation  
<img width="443" height="493" alt="MED SAL" src="https://github.com/user-attachments/assets/1512c52b-d5b1-4067-af63-04a48e31b948" />  

Count of Job Schedule Type  
$=FILTER(I2#,NOT(ISNUMBER(SEARCH("and",I2#)))*(I2#<>0))$  

🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.  

Background Table  

<img width="421" height="172" alt="Job-schedule" src="https://github.com/user-attachments/assets/ce7ad8c7-b555-4363-9a8c-96185244104f" />

 Dashboard Implementation:   
 <img width="512" height="472" alt="Type" src="https://github.com/user-attachments/assets/81778d3d-38e4-4ebf-8025-1bd0408f737e" />  

 Data Validation   
🔍 Filtered List
🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
🎯 User input is restricted to predefined, validated schedule types
🚫 Incorrect or inconsistent entries are prevented
👥 Overall usability of the dashboard is enhanced  


Conclusion: 
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel skills, this dashboard allows me to make informed decisions about my career paths. Exploring the functionalities to understand how location and job type influence salaries.



 



 



  








