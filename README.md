# School_District_Challenge
Module 4 challenge - School District Analysis
## Project Overview
This project was completed for a school district to analyze student test scores on a certain metrics.

## Methods
### Phase 1 : Data cleaning
The data was inspected and found to have issues in the Student Names column. 
Names where cleaned by removing prefixes using the following procedure:
 - Create a list of prefixes to be removed
prefixes_suffixes = ["Dr. ", "Mr. ","Ms. ", "Mrs. ", "Miss ", " MD", " DDS", " DVM", " PhD"]
 - Replace with empty space
for word in prefixes_suffixes:
    student_data_df["student_name"] = student_data_df["student_name"].str.replace(word,"")

### Phase 2: Student test score analysis
Student reading and math test scores where analysed, see image below for the full distric summary
<img width="703" alt="DistrictSummary" src="https://user-images.githubusercontent.com/95047485/149645658-e047d49c-ab34-40f8-b816-8bd76b4fea5c.PNG">

 Average test scores and passing percentages where calculated for:
1. School size
2. School Type
3. Budget per student
4. Scores per grade
5. High and low performing schools were isolated

### Phase 3
It was found that there was academic dishonesty at Thomas High School in the 9th grade class
Those scores for that grade and class were removed from analysis.

## Results
These analyses will give the school district insights on attributes of schools with high and low test scores. 
The most insightful data tables are the top 5 and bottom 5 performing schools. 
The top 5 schools are all charter schools, and despite spending less per student than the lowest performing distric schools the students still have better test scores.
Another insight that the district will surely be happy about is that there appears to be negative corelation between budget per student and test scores. 
<img width="652" alt="SpendPerStudent" src="https://user-images.githubusercontent.com/95047485/149646264-478cc7bd-095a-4081-834f-851209f21b2c.PNG">

Removing the 9th grade scores from Thomas high school had a small impact on overall scores as seen below
 
Thomas High School all students:
 
<img width="357" alt="ThomasHighSchool-all" src="https://user-images.githubusercontent.com/95047485/149646286-d8bc8b32-4f93-413f-8154-03e61319f8d7.PNG">

Thomas High School ninth graders removed:
 
<img width="392" alt="ThomasHighSchool-no9th" src="https://user-images.githubusercontent.com/95047485/149646279-8b0721dd-547f-4ce1-ad4f-ce1dfe24497d.PNG">

Other changes in the school distric analysis challenge is general re-factoring and making the code easier to read. Using conditional statements with '&' operator allows the analyst to define a variable and input all the criteria on one line instead of re-writing on multiple lines.


