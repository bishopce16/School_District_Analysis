# School_District_Analysis
## Overview of the school district analysis: 
The school board requested an analysis on the various performance metrics for the school district. For example, school budget, school size, school type, and student grades. The focus on the average scores for the state-testing standards in both reading and math. As well as the percent passing for reading, math and overall passing percentage. The data sources and software used to conduct this analysis are listed below in resources section, the CSV files are also located in the resources folder along with images used in this report. The analysis was performed a second time after the school board reviewed the original data analysis, which pointed to academic dishonesty by the ninth-grade class at Thomas High School (THS). Because of the potential academic dishonesty by the ninth-grade students at Thomas High School, the school board requested the analysis to be conducted second analysis excluding the ninth-grade students scores from THS and replaced the scores with a null value (NaN).
#
## Resource:
Data Sources:
schools_complete.csv,
students_complete.csv
#
Software:
Anaconda 4.13.0,
Jupyter Notebook 6.4.11,
Python 3.8.9
#
Libraries:
Pandas,
Numpy
#
## Results: 
Because of the potential dishonesty by the ninth-grade students at Thomas High School (THS), the school board requested the analysis to be conducted a second time. With the first analysis including the full set of student data, and the second analysis excluding the ninth-grade students scores from Thomas High School and replacing the scores with NaN.
Below is District Summary DataFrame created after replacing the Thomas High School ninth-grade students scores with NaN.
#
* How is the district summary affected?
    -	The total count of students was not affected as “student_name” column was used to run the count and only the reading and math scores were replaced with NaN. Comparing the two DataFrames shows that the removal of less than 500 student had a nominal impact on the percentage overall passing. 
    #
    
    Below is the Original District Summary DataFrame using the full set of student data.

    ![Original District Summary DataFrame](School_District_Analysis/resources/original_district_summary_df.png)
    #
    Below is District Summary DataFrame created after replacing the Thomas High School ninth-grade students scores with NaN.
    #
    ![ District Summary DataFrame](School_District_Analysis/resources/district_summary_df.png)
#

* How is the school summary affected?
    - Replacing the ninth graders’ math and reading scores had a nominal effect on Thomas High School’s performance relative to the other schools. With less than a one percent difference in the Original District Summary DataFrame and the second District Summary DataFrame created after replacing the Thomas High School 9th grader scores with NaN, Thomas High School was in the top five schools in the original analysis and remained in the top five schools. 
    
        Original Analysis Top Five Schools:	 
        ![Original Analysis Top Five Schools](School_District_Analysis/resources/original_top_schools.png)

        Second Analysis Top Five Schools:
        ![Second Analysis Top Five Schools](School_District_Analysis/resources/top_five_schools.png)

#
* How does replacing the ninth-grade scores affect the following:

    * Math and reading scores by grade:
        
        - The reading and math scores by grade only changed the “Scores by Grade DataFrames” by replacing the scores for Thomas High School ninth-grade students with null values instead of a grade, which show up as NaN. As shown in the following images below.

        Original Analysis Reading Scores by Grade:
        ![Original Analysis Reading Scores by Grade](School_District_Analysis/resources/original_reading_scores_by_grade.png)

        Original Analysis Math Scores by Grade:
        ![Original Analysis Math Scores by Grade](School_District_Analysis/resources/original_math_scores_by_grade.png)

        Second Analysis Reading Scores by Grade:
        ![Second Analysis Reading Scores by Grade](School_District_Analysis/resources/reading_scores_by_grade.png)

        Second Analysis Math Scores by Grade:
        ![Second Analysis Math Scores by Grade](School_District_Analysis/resources/math_scores_by_grade.png)

    * Scores by school spending
        - The findings indicate the increase of spending per student does not increase the average scores and passing percentages. This shows that there might be more significant aspects than funding that decide average scores and percent passing.
        
        ![Spending Summary DataFrame](School_District_Analysis/resources/spending_summary_df.png)

    * Scores by school size
        - The “small” and “medium” schools (Under 2,000 student)  have a negligible difference in performance, in average reading and math scores and percent overall passing. The “large” schools that have 2,000 student or more have the lowest average scores and passing percentage. The school sizes seem to suggest a direct impact on students’ performance in smaller learning environments in this district. 

        ![Size Summary DataFrame](School_District_Analysis/resources/size_summary_df.png)

    * Scores by school type
        - District school are outproformed by Charter schools, in reading scores, math scores and percentage overall passing. The district schools overall percentage passing is being pulled down by the percentage passing math.
        ![Type Summary DataFrame](School_District_Analysis/resources/type_summary_df.png)

#
## Summary: 
Because of the potential academic dishonesty by the ninth-grade students at Thomas High School, the school board requested the analysis to be conducted second time, with the second analysis excluding the ninth-grade students scores from Thomas High School and replaced the scores with a null value (NaN). This did not alter the total student count, as the column that was used to run the count was “student_name” and only the reading and math scores were replaced with NaN. So, the removal of the ninth-grade students from Thomas High School had a nominal impact on the percentage overall passing in the District Summary DataFrame. The only changes in both the Reading Score by Grade DataFrame and Math Score by Grade DataFrame were null values instead of grades for Thomas High School ninth-grade students. The one percent difference in the Original District Summary DataFrame and the second District Summary DataFrame created after replacing the Thomas High School ninth-grader scores with a null value had a nominal effect on Thomas High School’s performance relative to the other schools, as was seen by Thomas High School being in the top five schools in both analyses.