# Excel_Salary_Dashboard  

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/553ac7bb-f0c3-4db2-8b56-df6b9fe63674)  

## Introduction  
The data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequetly compensated.  

The data is from @lukebarousse's Excel course that I used in my project, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.  
### Dashboard File  
My final dashboard is in [My 1st Project (Salary-Dashboard).xlsx](https://github.com/WraithIsLive/Excel_Project-Data_Analytics/blob/main/Project%201%20Salary%20Dashboard/My%201st%20Project%20(Salary-Dashboard).xlsx).  

### Excel Skills Used  
The following Excel skills were utilized for analysis:  
- 📉 **Charts**
- 🧮 **Formulas and Functions**
- ❎ **Data Validation**

### Data Jobs Dataset  
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via @lukebarousse's Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:  
- 👨‍💼 **Job titles**  
- 💰 **Salaries**
- 📍 **Locations**
- 🛠️ **Skills**

## Dashboard Build  

### 📉 Charts  

#### 📊 Data Science Job Salaries - Bar Chart  

<img width="850" height="550" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/c39d2fe6-dd0f-41df-a021-bd0e9fe249fb" />    

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.    
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.  
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readibility.  
- 💡 **Insightes Gained:** This enables quick identification of salary trends, nothing that Senior roles and Engineers are higher-paying than Analyst roles.    

#### 🗺️ Country Median Salaries - Map Chart  
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/9c280392-380b-489c-a608-7b787f1bc578)  
- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.  
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions  

#### 💰 Median Salary by Job Titles  
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```
- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, region, and schedule types.
- 🔢 **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

#### 🍽️ Background Table  
![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/b3a884e9-42e1-4e20-97d6-a32551e8f256)  

#### 📉 Dashboard Implementation  
<img width="400" height="500" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/641d41d5-d60d-4e42-b08b-5f0fc55fda60" />  

#### ⏰ Count of Job Schedule Type  
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 **Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

#### 🍽️ Background Table  
<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/3cb452c0-5a74-4cd5-ba3b-62c58bcf3c45" />  

#### 📉 Dashboard Implementation:  
<img width="350" height="500" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/cd710185-9c34-4bef-b396-0753f4f54d80" />  

### ❎ Data Validation  
#### 🔍 Filtered List  
- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:  
  ◦ 🎯 User input is restricted to predefined, validated schedule types  
  ◦ 🚫 Incorrect or inconsistent entries are prevented  
  ◦ 👥 Overall usability of the dashboard is enhanced
  
<img height="400" alt="1_Salary_Dashboard_Data_Validation" src="https://github.com/user-attachments/assets/5a1f835f-b9f1-4e34-bb91-fa35130ef79c" />  

## Conclusion  
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from @lukebarousse's Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
