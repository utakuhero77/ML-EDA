# ML-EDA
 Dataset Description
This dataset contains information about users' app usage, demographics, preferences, and challenges in using dating applications. It includes details on primary and secondary app choices, usage frequency, satisfaction levels, and desired features.

| Column Name                   | Data Type | Description |
|--------------------------------|----------|-------------|
| User_ID                        | int      | Unique identifier for each user |
| Age                            | int      | Age of the user |
| Gender                         | category   | Gender identity of the user |
| Location                       | category   | City where the user is based |
| Education                      | category   | Highest level of education completed |
| Occupation                     | category   | Employment status or job role of the user |
| Primary_App                    | category   | The main dating app the user prefers |
| Secondary_Apps                 | category   | Other dating apps the user uses |
| Usage_Frequency                | category   | How often the user engages with dating apps (e.g., daily, weekly, monthly) |
| Daily_Usage_Time               | category   | Time spent on the apps in hours/minutes format |
| Reason_for_Using               | category   | The user's motivation for using dating apps (e.g., finding a partner, casual dating) |
| Satisfaction                   | category      | Satisfaction rating on a scale (e.g., 1-5) |
| Challenges                     | category   | Issues faced while using dating apps (e.g., safety concerns, time-wasting) |
| Desired_Features               | category   | Features users wish to have in dating apps |
| Preferred_Communication        | category   | The most preferred mode of communication (e.g., text, voice notes, video calls) |
| Partner_Priorities             | category   | The order of priority for selecting a partner (e.g., values > personality > appearance) |
| Daily_Usage_Time_in_Minutes    | category      | Numeric representation of daily usage time in minutes |



Data Cleaning Steps 

1. Checked for Missing Values:  
    Found missing values in `Primary_App`, `Secondary_App`, and `Challenges`.  
    Used the mode to fill values  to handle them sincethe value counts in each column were evenly distributed. using mode prevents over-representation of rare values

2. Data Type Consistency: 
   Converted object-type columns to **category data type**.  
    Converted `Satisfaction` column to **category data type** for better efficiency.  

3. Ensured Gender Categorization:  
    Standardized categorical labels (e.g., ensuring "Male" and "male" are the same) to remove inconsistencies.  

4. Outlier Detection:
    Performed an analysis using box plots and the IQR method to detect outliers.
     No significant outliers were found, indicating that the dataset values were within an acceptable range
