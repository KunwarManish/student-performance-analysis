# Analysis of a Student Performance Dataset

## 1. Data Understanding

The dataset includes information from the student.csv file. The dataset comes from two

Portuguese schools &quot;Gabriel Pereira&quot; and &quot;Mousinho da Silveira&quot; contains student grades, demographic, social, and school-related characteristics. It contains information about students, their grades, and their families.

#### Data Characteristics as a Tabular Representation

| S.N. | Dataset | Description | Data Type | Variable Type |
| --- | --- | --- | --- | --- |
| 1. | school | school refers to the school that students of GP and MS attend. GP stands for Gabriel Pereira and MS stands for Mousinho da Silveira. The students are supposed to attend one of the two school. | object | categorical |
| 2. | sex | sex contains information about the student&#39;s gender, such as M for Male and F for Female. | object | categorical |
| 3. | age | age refers to a student&#39;s age, which ranges from 15 to 22 years old. | int64 | categorical |
| 4. | address | address includes the address of the student&#39;s house. In this case, &quot;U&quot; stands for urban, and &quot;R&quot; stands for rural. | object | categorical |
| 5. | famsize | famsize contains information on a student&#39;s family size. Here. &quot;LE3&quot; indicates less than 3 and &quot;GT3&quot; indicates more than 3. | object | categorical |
| 6. | Pstatus | cohabitation status of the parents is included in Pstatus, with &quot;T&quot; indicating living together and &quot;A&quot; indicating living apart. | object | categorical |
| 7. | Medu | Medu refers to a student&#39;s mother&#39;s educational level, which has 4 values: primary education (4th grade), 5th to 9th grade, secondary education, or higher education. | object | categorical |
| 8. | Fedu | Fedu refers to a student&#39;s father&#39;s educational level, which has 4 values: primary education (4th grade), 5th to 9th grade, secondary education, or higher education. | object | categorical |
| 9. | Mjob | Mjob stands for a student&#39;s job mother. &quot;Teacher,&quot; &quot;health&quot; care related, civil &quot;services&quot; (e.g., administrative or police), &quot;at home,&quot; or &quot;other&quot; are the five values for this column. | object | categorical |
| 10. | Fjob | Fjob stands for a student&#39;s job father. &quot;Teacher,&quot; &quot;health&quot; care related, civil &quot;services&quot; (e.g., administrative or police), &quot;at home,&quot; or &quot;other&quot; are the five values for this column. | object | categorical |
| 11. | reason | reason includes the reason for selecting the school. It consists of one of five variables: close to &quot;home,&quot; school &quot;reputation,&quot; &quot;course&quot; preference, and &quot;other.&quot; | object | categorical |
| 12. | guardian | The student&#39;s guardian is referred to as the guardian. It has one of three variables, &quot;mother,&quot; &quot;father,&quot; or &quot;other.&quot; | object | categorical |
| 13. | traveltime | The amount of time it takes a student to get from home to school is referred to as traveltime. It can be one of the following values: 1- \&lt;15 minutes, 2- 15 to 30 minutes, 3- 30 minutes to 1 hour, or 4-\&gt; 1 hour. | object | categorical |
| 14. | studytime | Students weekly study time is referred to as studytime. It is made up of one of four variables, each with a different value. i.e., 1– \&lt;2 hours, 2–2–5 hours, 3–5–10 hours, or 4– \&gt;10 hours. | object | categorical |
| 15. | failures | failures represent the total number of previous class failures. The failure column holds one of four values, namely 0, 1, 2, and 3. | int64 | discrete |
| 16. | schoolsup | schoolsup refers to the additional educational help offered by the specific school to needy students. It has two variables: &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 17. | famsup | famsup refers to the family assistance offered to students in order to help them with their education. It has two possible outcomes: &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 18. | paid | paid refers to whether or not the student had extra paid classes inside the course; the value is either &quot;yes&quot; or &quot;no&quot;. | object | categorical |

| 19. | activities | activities show whether or not the student participates in extracurricular activities at school. The value can only be &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| --- | --- | --- | --- | --- |
| 20. | nursery | nursery indicates whether or not the student has attended nursery school. It has two variables: &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 21. | higher | higher reflects whether or not students want to attain higher education in the future. It has two values: &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 22. | internet | internet indicates whether or not the student has access to the internet at home. The value is either &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 23. | romantic | romantic indicates if the student is in a romantic relationship. The value is either &quot;yes&quot; or &quot;no&quot;. | object | categorical |
| 24. | famrel | famrel indicates the quality of students&#39; family relationships. It has one of the five variables, namely &quot;very bad,&quot; &quot;bad,&quot; &quot;good,&quot; &quot;very good,&quot; and &quot;excellent&quot;. | object | categorical |
| 25. | freetime | After school, each student&#39;s spare time is referred to as freetime. It contains five variables: &quot;very low,&quot; &quot;low,&quot; &quot;medium,&quot; &quot;high,&quot; and &quot;very high&quot;. | object | categorical |
| 26. | goout | The frequency of outings with friends is referred to as goout. It has one of the five provided values: &quot;very low,&quot; &quot;low,&quot; &quot;medium,&quot; &quot;high,&quot; and &quot;very high&quot;. | object | categorical |
| 27. | Dalc | Dalc represents a student&#39;s weekday alcohol consumption. It has one of the five provided values: &quot;very low,&quot; &quot;low,&quot; &quot;medium,&quot; &quot;high,&quot; and &quot;very high&quot;. | object | categorical |
| 28. | Walc | Walc indicates weekend alcohol intake. It has one of the five possible values: &quot;very low,&quot; &quot;low,&quot; &quot;medium,&quot; &quot;high,&quot; or &quot;very high&quot;. | object | categorical |
| 29. | health | health refers to the student&#39;s current health situation. It has one of the five variables, namely &quot;very bad,&quot; &quot;bad,&quot; &quot;good,&quot; &quot;very good,&quot; or &quot;excellent.&quot; | object | categorical |

| 30. | absences | absences refer to a student&#39;s total number of absences from school. In the absence&#39;s column, the value ranges from 0 to 75. | int64 | discrete |
| --- | --- | --- | --- | --- |
| 31. | G1 | G1 refers to a student&#39;s grade in the first period of school, which ranges from 0 to 20. | int64 | discrete |
| 32. | G2 | G2 refers to students in their second period grade, where their grade ranges from 0 to 20. | int64 | discrete |
| 33. | G4 | G3 refers to the grade of students in which the student&#39;s grade ranges from 0 to 20. | int64 | discrete |

_Table 1: Data attributes are represented in a table._

## 2. Data Transformation

All of the processes involved in the conversion are the same. The unique () function returns an array of the input array&#39;s unique elements. A binary value of 0 or 1 was assigned to an empty dictionary. The concat () function applies a function to all the elements of a given object. The first five values are returned by the head () method.


### 2.1 school, sex, address, famsize, Pstatus, schoolsup, famsup, paid, activities, nursery, higher, internet and romantic into binary: 0 or 1 (create new columns without overwriting the existing ones)

### 2.2 Medu, Fedu, Mjob, reason, guardian, traveltime, studytime, famrel, freetime, gout, Dalc, Walc and health into ordinal numbers based on number of cases in the data set (create new columns without overwriting the existing ones)

### 2.3 create a new column named age\_category whose values should be based on the values in the age column, divide the values into 3 ordinal numbers: 1-15 to 17, 2-18 to 20, 3-21 and over

## 3. Initial Data Analysis

### 3.1 The summary statistics (sum, mean, median, standard deviation, max and min) of the variables age, absences, G1, G2 and G3.

### 3.2 The correlation between the variables absences, failures, G1, G2 and G3. Present the result using a heatmap and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178655041-86abab26-d784-4b76-b341-e29658de6282.png)

_Figure 36: corr () function being used to compute correlation of columns._

The above screenshot demonstrates the implementation of corr function in which the correlation of absences, failures, G1, G2 and G3 is presented.

![image](https://user-images.githubusercontent.com/31987649/178655106-f3f810db-69ce-4860-a7b1-3d78893184e7.png)

_Figure 37: Heatmap presenting the correlation between variables._

The color codes used in the heatmap above show the strength of each variable, namely absences, failures, G1, G2, and G3. In the above heatmap, the correlation between the variables is strong if the color is dark, but the connection between the variables is weak if the color is light.

## 4. Data Exploration and Visualization

### 4.1 Histogram plots and boxplots to visualize the distribution of the variables age, absences and G3. Interpret the results and comment about the distribution of each variable.

**a) Histogram: Age**

![image](https://user-images.githubusercontent.com/31987649/178655214-8cc7e698-850c-4771-858a-b468bf7b1ef7.png)

_Figure 38: Histogram plots to represent the number of students according to their age._

According to the above histogram plots, the number of students between the ages of 16 and 17 is high, while the number of students between the ages of 21 and 22 is low.

#### b) Histogram: Absences

![image](https://user-images.githubusercontent.com/31987649/178655248-d05747ad-b99d-4e29-a5e4-024c7bd58251.png)

_Figure 39: Histogram plots to represent the number of students according to their absence._

According to the above histogram plots, the number of absences of students ranging from

0 to 10 is high, whereas the number of absences of students ranging from 60 to 70 is low.

#### c) Histogram: G3

![image](https://user-images.githubusercontent.com/31987649/178655283-5d786a66-5af3-4154-b09b-b593af78e983.png)

_Figure 40: Histogram plots to represent the number of students according to G3_

According to the above histogram plots, the number of students with first period grades ranging from 10 to 11 is high, while the number of students with first period grades ranging from 3 to 4 and 4 to 5 is low.

#### e) Box Plots: Age

![image](https://user-images.githubusercontent.com/31987649/178655309-53083c6a-bdb1-47d8-874a-ecc1876439a9.png)

_Figure 41: Box plots to represent the number of students according to their age._

According to the above box plots, the students age 17 is median, age 16 is lower quartile, age 18 is upper quartile, while the number of students the age of 15 is min and 22 is max.

#### f) Box Plots: Absences

![image](https://user-images.githubusercontent.com/31987649/178655337-a4514416-b3e7-4410-89a5-813ec376acbb.png)

_Figure 42: Box plots to represent the number of students according to their absence._

According to the box plots above, the number of absences of students ranging from 0 (lower quartile) to 10 (upper quartile) is the median, while the number of absences of students ranging from 60 to 70 is the maximum.

#### g) Box Plots: G3

![image](https://user-images.githubusercontent.com/31987649/178655372-fa765beb-b8ac-4140-a300-6dd61a3f9e56.png)

_Figure 43: Box plots to represent the number of students according to G3_

According to the above box plots, the grade ranges from 10 to 12.5 is median, grade range from 7.5 to 10 is lower quartile, grade from 12.5 to 15 is upper quartile, while the number of grade 0 is min and 20 is max.

### 4.2 Bar graph of the total number of students who passed the final term grouped according to the school that they belong to. Use proper labels in the graph and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178655389-274bfebe-ceec-47bc-a193-242dc276bbf5.png)

_Figure 44: Bar graph of total number of passed students in final term grouped according to school._

The bar graph represents that the rate of total number of passed students is higher in GP, i.e., Gabriel Pereira school, than in MS, i.e., Mousinho da Silveira school.

### 4.3 Bar graph of the total number students who failed the final exam grouped according to their weekly study time. Use proper labels in the graph and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178655487-de829f76-fcf8-4990-92ed-bcf93cadd757.png)

_Figure 45: Bar graph of total number of failed students in final term grouped according to their weekly study time._

According to the bar graphs, students who study 2 to 5 hours per week have a high failure rate in their final term, whereas those who study more than 10 hours per week have a low failure rate in their final exam.

## 5. Further Analysis

#### Student Data as per the school

![image](https://user-images.githubusercontent.com/31987649/178655516-13480273-e932-417b-961c-802167040e35.png)

_Figure 46: Pie-Chart representing number of students according to School._

According to the pie chart above, 88.35 percent of students attend GP i.e., School Gabriel Pereira, and 11.65 percent attend MS i.e., School on Mousinho da Silveira. According to the above chart, the number of students enrolled in GP school is more than the number of students enrolled in MS school.

#### Grade as Per the Gender

![image](https://user-images.githubusercontent.com/31987649/178655530-f55767e4-94a1-435c-b384-7279ba3136b6.png)

_Figure 47: Pie-Chart representing total number of male and female_

In the pie chart screenshot above, &#39;F&#39; stands for Female and &#39;M&#39; stands for Male. According to the pie chart above, 52.66 percent of people are female, and 47.34 percent are male. As a result, female students outnumber male students at GP and MS schools.

#### Student Pass and Fail Rate as Per School

![image](https://user-images.githubusercontent.com/31987649/178655594-1ca00335-52ed-4700-b1f3-7207b96a809c.png)

_Figure 48: Extracting number of pass and fail students in a school._

The total number of passes for each student is calculated and saved in the dictionary dictPassedSchool, while the total number of failed students is computed and stored in the dictionary dictFailSchool, as seen in the code screenshot above. GP is denoted by 0 and MS is denoted by 1.

![image](https://user-images.githubusercontent.com/31987649/178655620-7dbadad0-babc-4459-97a9-5adcbaeb6b5b.png)

_Figure 49: Bar graph of total number of pass and fail rate as per the school._

The bar graph above illustrates that the pass rate and failure rate of students are higher in GP school than in MS school. The student who passed the exam in the bar diagram above are represented by red color, and the student who failed the exam are represented by blue color. According to the bar graph above, the rate of pass for GP students is higher than the rate of failure. In the case of MS, the failure rate is larger than the pass rate.

**Student&#39;s Family Background affect his/her grades.**

#### Grade of Student as per the Father&#39;s job

![image](https://user-images.githubusercontent.com/31987649/178655654-1f9f1f8f-a48d-41e6-a840-f57bfc41ab89.png)

_Figure 50: Bar Graph of student pass rate as per father&#39;s occupation._

Students who passed their exams are shown in dark green, while those who failed are shown in light green in the bar graph above. According to the bar graph above, the father of the student who has been active in various occupation other than teacher, services, health and at home has a low pass rate and failure rate. Furthermore, according to the graph above, the failure rate of students whose father works in the health field is low and high pass rate in other.

#### Grade of Student as per the Mother&#39;s Job

![image](https://user-images.githubusercontent.com/31987649/178655690-cf649f53-41e4-4f55-a0a3-9815d2030a28.png)

_Figure 51: Bar Graph of student pass rate as per Mother&#39;s occupation_

The students who passed their exam are shown in light green, while those who failed are shown in dark green in the bar graph above. According to the bar graph above, the mother of the student who was involved in various professions other than teacher, services, health, and at home has a low pass rate as well as failure rate. Furthermore, according to the graph above, the failure rate of students whose mother works in the health field is low and high rate in other.

#### Parent&#39;s Education Background &amp; Student&#39;s Pass Rate

![image](https://user-images.githubusercontent.com/31987649/178655716-72caa36e-04f7-4da5-9185-c7d9de4c20e6.png)

_Figure 52: Horizontal Bar graph indicates parent&#39;s education background with student&#39;s pass rate._

The pass rate according to final grade is represented by orange in the bar graph above, while the fail rate according to final grade is represented by green. The students whose mothers do not have a background in education, such as higher education, primary education (4th grade), and secondary education, appear to have a high pass rate and the lowest failure rate in their final grade, as shown by the horizontal bar above. The bar graph represents the same for the father&#39;s educational background. Students whose mother&#39;s occupation is higher education tend to fail more in their final grade, whereas students whose father&#39;s occupation is primary education (4th grade) have a high failure rate in their last grade, according to the graph above.

**Family Relationship of Students and their pass rate.**

![image](https://user-images.githubusercontent.com/31987649/178655740-a4df22b2-c33a-4d9d-a75f-54786521ccdb.png)

_Figure 53: Bar graph of student&#39;s family relationship and their pass rate._

The orange color bar in the bar graph above represents students who did not pass, while the green color bar represents students who did. The bar graphs show the students&#39; family relationships as well as their pass/fail rates. As seen in the graph above, students with very good family relationships have a high pass rate, but they also have a high failure rate when compared to other family relationships. Students with very bad family relationships had the lowest pass and failure rates. According to the graph above, students who have a strong family relationship tend to do well on their exams.

#### Student Performance in Final as per their Study Time

![image](https://user-images.githubusercontent.com/31987649/178655768-9ffafeba-d4d4-464c-9023-9318427c9592.png)

_Figure 54: Bar graph of final result of student as per the study time._

The vertical bar graph above displays students&#39; final grades with pass and fail rates based on their study time. According to the following bar graph, students who have a very good reading time plan performed well in their final test and passed the exam, whereas students who have a terrible reading timetable had the lowest pass percentage based on their final grade. Similarly, students with a good reading time plan had the lowest failure percentage based on their final grade.

#### Number of Student&#39;s Study Time affect the Final Grade

![image](https://user-images.githubusercontent.com/31987649/178655796-c816d7f8-be02-4371-bd39-d4752b6b9a48.png)

_Figure 55: Bar graph of the study time and number of pass rate students._

The dark green color in the screenshot above represents the pass student rate, while the light green color represents the fail student rate. The graph above demonstrates that students with study time between 2 and 5 hours have a high pass percentage, whereas those with study time between 2 and 5 hours have a significant failing rate. According to the bar graph above, students who study for more than 10 hours had the lowest failure rate.

**Internet Role in a Student&#39;s Studies.**

![image](https://user-images.githubusercontent.com/31987649/178655830-9f35009a-3cbb-44c4-a16b-5bc8f5c3bfb6.png)

_Figure 56: Box plot of internet usage of student for the final exam._

The blue color box in the above box plot diagram indicates students who do not have access to the internet, while the orange color box shows students who have. Students that have access to the internet appear to fare better in their final grades, as seen in the box plot above. Also, the above graph shows that students who perform exceptionally well in their exams have access to the internet, as the box plot of students with access to the internet has a greater maximum value than the box plot of students without access. Similarly, as seen in the accompanying box map, pupils who do not have access to the internet have a lower median value than those who do.

**Attendance as per Age with their Pass Rate.**

![image](https://user-images.githubusercontent.com/31987649/178655854-1611d4e6-04ec-46f7-acd8-49c7bcf2a1a5.png)

_Figure 57: Violin plot of attendance as per age with their pass rate._

The orange color in the above Violin plot represents the rate of pass students with their absence rate as per age, whereas the blue color represents the rate of failed students with their absence rate as per age. The median value is shown by the white dot in the violin plot above. The violin plot shows that there are the most value points in the range of 0 to 20. Similarly, in the age group of 18 to 19 data who had passed and had absent days, there is a large range of numbers. From the violin plot above, it can be deduced that students in the age bracket of 18 to 19 who have a lot of absence days may still do well in exams.

#### Alcohol Consumption Weekly and Daily with the Pass Rate

![image](https://user-images.githubusercontent.com/31987649/178655881-ec444257-e29a-4666-8352-732555cbbac1.png)

_Figure 58: Bar graph of Alcohol consumption daily and weekly of students with the pass rate_

The green color bar in the above bar graph represents students who have not passed, while the grey color bar represents students who have passed. The bar graphs show the student&#39;s daily and weekly alcohol intake, as well as their pass and fail rate as determined by their final grade. Students that use very little alcohol on a daily and weekly basis have a high final grade pass percentage, as seen in the above bar diagram. Similarly, students who use a lot of alcohol on a regular and weekly basis are more likely to fail their final exams. It may be concluded from the graph above that student who consume very little alcohol have a high final grade pass rate.

#### Extracurricular activities of students as per their gender and pass rate

![image](https://user-images.githubusercontent.com/31987649/178655891-302e32de-9d82-48a0-99ca-9bc99fca41f7.png)

_Figure 59: Swarm plot of students participate in extracurricular activities categorized according to their gender with pass rate._

The failed students are represented by the red filled circle in the swarm plot above, while the graduates are represented by the blue full circle. The graph on the left depicts students who do not participate in extracurricular activities and receive a final grade based on their gender, whereas the graph on the right depicts students who do participate in extracurricular activities and receive a final grade based on their gender. According to the graph above, men students participate in more extracurricular activities than female students. Male students who participate in extracurricular activities had a lower failing percentage in the final grade than female students who participate in extracurricular activities. According to the graph above, women who do not participate in any extracurricular activities have a high pass rate in their final grade.
  
