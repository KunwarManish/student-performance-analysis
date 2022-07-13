# Analysis of a Student Performance Dataset

## 1. Data Understanding

The dataset includes information from the student.csv file. The dataset comes from two Portuguese schools &quot;Gabriel Pereira&quot; and &quot;Mousinho da Silveira&quot; contains student grades, demographic, social, and school-related characteristics. It contains information about students, their grades, and their families.

## 2. Data Transformation

All of the processes involved in the conversion are the same. The unique () function returns an array of the input array&#39;s unique elements. A binary value of 0 or 1 was assigned to an empty dictionary. The concat () function applies a function to all the elements of a given object. The first five values are returned by the head () method.

### 2.1 school, sex, address, famsize, Pstatus, schoolsup, famsup, paid, activities, nursery, higher, internet and romantic into binary: 0 or 1 (create new columns without overwriting the existing ones)

### 2.2 Medu, Fedu, Mjob, reason, guardian, traveltime, studytime, famrel, freetime, gout, Dalc, Walc and health into ordinal numbers based on number of cases in the data set (create new columns without overwriting the existing ones)

### 2.3 create a new column named age\_category whose values should be based on the values in the age column, divide the values into 3 ordinal numbers: 1-15 to 17, 2-18 to 20, 3-21 and over

## 3. Initial Data Analysis

### 3.1 The summary statistics (sum, mean, median, standard deviation, max and min) of the variables age, absences, G1, G2 and G3.

### 3.2 The correlation between the variables absences, failures, G1, G2 and G3. Present the result using a heatmap and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178658617-09a936f7-ea10-4c33-ae3b-fd7f41b56ce6.png)

_Figure 1: corr () function being used to compute correlation of columns._

The above screenshot demonstrates the implementation of corr function in which the correlation of absences, failures, G1, G2 and G3 is presented.

![image](https://user-images.githubusercontent.com/31987649/178658584-77a12d80-e65d-4d21-a270-a69c5f662a4a.png)

_Figure 2: Heatmap presenting the correlation between variables._

The color codes used in the heatmap above show the strength of each variable, namely absences, failures, G1, G2, and G3. In the above heatmap, the correlation between the variables is strong if the color is dark, but the connection between the variables is weak if the color is light.

## 4. Data Exploration and Visualization

### 4.1 Histogram plots and boxplots to visualize the distribution of the variables age, absences and G3. Interpret the results and comment about the distribution of each variable.

**a) Histogram: Age**

![image](https://user-images.githubusercontent.com/31987649/178658513-cd64ef78-fd89-4d31-b722-3e66ad5236ab.png)

_Figure 3: Histogram plots to represent the number of students according to their age._

According to the above histogram plots, the number of students between the ages of 16 and 17 is high, while the number of students between the ages of 21 and 22 is low.

#### b) Histogram: Absences

![image](https://user-images.githubusercontent.com/31987649/178658474-fd6147fd-8198-49a4-8093-29b87a5b4b9a.png)

_Figure 4: Histogram plots to represent the number of students according to their absence._

According to the above histogram plots, the number of absences of students ranging from

0 to 10 is high, whereas the number of absences of students ranging from 60 to 70 is low.

#### c) Histogram: G3

![image](https://user-images.githubusercontent.com/31987649/178658443-9b26a42f-956a-4f8b-b310-4c4070fb8f49.png)

_Figure 5: Histogram plots to represent the number of students according to G3_

According to the above histogram plots, the number of students with first period grades ranging from 10 to 11 is high, while the number of students with first period grades ranging from 3 to 4 and 4 to 5 is low.

#### e) Box Plots: Age

![image](https://user-images.githubusercontent.com/31987649/178658405-2fb8acef-f6a9-4b27-a401-6dab367169e9.png)

_Figure 6: Box plots to represent the number of students according to their age._

According to the above box plots, the students age 17 is median, age 16 is lower quartile, age 18 is upper quartile, while the number of students the age of 15 is min and 22 is max.

#### f) Box Plots: Absences

![image](https://user-images.githubusercontent.com/31987649/178658355-c75bcb47-13f7-46d2-bd1e-24a68ae0a2fd.png)

_Figure 7: Box plots to represent the number of students according to their absence._

According to the box plots above, the number of absences of students ranging from 0 (lower quartile) to 10 (upper quartile) is the median, while the number of absences of students ranging from 60 to 70 is the maximum.

#### g) Box Plots: G3

![image](https://user-images.githubusercontent.com/31987649/178658320-f1bc1bff-847c-4bfa-941f-1edbc88d7f3b.png)

_Figure 8: Box plots to represent the number of students according to G3_

According to the above box plots, the grade ranges from 10 to 12.5 is median, grade range from 7.5 to 10 is lower quartile, grade from 12.5 to 15 is upper quartile, while the number of grade 0 is min and 20 is max.

### 4.2 Bar graph of the total number of students who passed the final term grouped according to the school that they belong to. Use proper labels in the graph and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178658280-33dbc355-4970-4bf5-ba12-b9baa0f12729.png)

_Figure 9: Bar graph of total number of passed students in final term grouped according to school._

The bar graph represents that the rate of total number of passed students is higher in GP, i.e., Gabriel Pereira school, than in MS, i.e., Mousinho da Silveira school.

### 4.3 Bar graph of the total number students who failed the final exam grouped according to their weekly study time. Use proper labels in the graph and interpret the results.

![image](https://user-images.githubusercontent.com/31987649/178658222-2e1d2b2d-bc19-49a0-aeab-c35f8c0eca85.png)

_Figure 10: Bar graph of total number of failed students in final term grouped according to their weekly study time._

According to the bar graphs, students who study 2 to 5 hours per week have a high failure rate in their final term, whereas those who study more than 10 hours per week have a low failure rate in their final exam.

## 5. Further Analysis

#### Student Data as per the school

![image](https://user-images.githubusercontent.com/31987649/178658057-d20734af-1554-454b-bad4-f2670f6f5b3e.png)

_Figure 11: Pie-Chart representing number of students according to School._

According to the pie chart above, 88.35 percent of students attend GP i.e., School Gabriel Pereira, and 11.65 percent attend MS i.e., School on Mousinho da Silveira. According to the above chart, the number of students enrolled in GP school is more than the number of students enrolled in MS school.

#### Grade as Per the Gender

![image](https://user-images.githubusercontent.com/31987649/178658009-4128b489-3f1d-4e1f-9712-f4e05596d134.png)

_Figure 12: Pie-Chart representing total number of male and female_

In the pie chart screenshot above, &#39;F&#39; stands for Female and &#39;M&#39; stands for Male. According to the pie chart above, 52.66 percent of people are female, and 47.34 percent are male. As a result, female students outnumber male students at GP and MS schools.

#### Student Pass and Fail Rate as Per School

![image](https://user-images.githubusercontent.com/31987649/178657887-0252b076-09fa-4fc2-88a3-9960ff01ee6b.png)

_Figure 13: Bar graph of total number of pass and fail rate as per the school._

The bar graph above illustrates that the pass rate and failure rate of students are higher in GP school than in MS school. The student who passed the exam in the bar diagram above are represented by red color, and the student who failed the exam are represented by blue color. According to the bar graph above, the rate of pass for GP students is higher than the rate of failure. In the case of MS, the failure rate is larger than the pass rate.

**Student&#39;s Family Background affect his/her grades.**

#### Grade of Student as per the Father&#39;s job

![image](https://user-images.githubusercontent.com/31987649/178657749-a5a40933-e7bb-4695-bcf3-500d5e3be139.png)

_Figure 14: Bar Graph of student pass rate as per father&#39;s occupation._

Students who passed their exams are shown in dark green, while those who failed are shown in light green in the bar graph above. According to the bar graph above, the father of the student who has been active in various occupation other than teacher, services, health and at home has a low pass rate and failure rate. Furthermore, according to the graph above, the failure rate of students whose father works in the health field is low and high pass rate in other.

#### Grade of Student as per the Mother&#39;s Job

![image](https://user-images.githubusercontent.com/31987649/178657715-6f5b5450-45c6-4ef4-961e-8417946b4edf.png)

_Figure 15: Bar Graph of student pass rate as per Mother&#39;s occupation_

The students who passed their exam are shown in light green, while those who failed are shown in dark green in the bar graph above. According to the bar graph above, the mother of the student who was involved in various professions other than teacher, services, health, and at home has a low pass rate as well as failure rate. Furthermore, according to the graph above, the failure rate of students whose mother works in the health field is low and high rate in other.

#### Parent&#39;s Education Background &amp; Student&#39;s Pass Rate

![image](https://user-images.githubusercontent.com/31987649/178657671-318fd36b-99c1-492a-89f9-9ae8ec48c7bb.png)

_Figure 16: Horizontal Bar graph indicates parent&#39;s education background with student&#39;s pass rate._

The pass rate according to final grade is represented by orange in the bar graph above, while the fail rate according to final grade is represented by green. The students whose mothers do not have a background in education, such as higher education, primary education (4th grade), and secondary education, appear to have a high pass rate and the lowest failure rate in their final grade, as shown by the horizontal bar above. The bar graph represents the same for the father&#39;s educational background. Students whose mother&#39;s occupation is higher education tend to fail more in their final grade, whereas students whose father&#39;s occupation is primary education (4th grade) have a high failure rate in their last grade, according to the graph above.

**Family Relationship of Students and their pass rate.**

![image](https://user-images.githubusercontent.com/31987649/178657528-319fe932-417a-4dfe-8b63-c772fcee6962.png)

_Figure 17: Bar graph of student&#39;s family relationship and their pass rate._

The orange color bar in the bar graph above represents students who did not pass, while the green color bar represents students who did. The bar graphs show the students&#39; family relationships as well as their pass/fail rates. As seen in the graph above, students with very good family relationships have a high pass rate, but they also have a high failure rate when compared to other family relationships. Students with very bad family relationships had the lowest pass and failure rates. According to the graph above, students who have a strong family relationship tend to do well on their exams.

#### Student Performance in Final as per their Study Time

![image](https://user-images.githubusercontent.com/31987649/178657471-c1430983-c3c3-4fda-a691-89bd83b899f6.png)

_Figure 18: Bar graph of final result of student as per the study time._

The vertical bar graph above displays students&#39; final grades with pass and fail rates based on their study time. According to the following bar graph, students who have a very good reading time plan performed well in their final test and passed the exam, whereas students who have a terrible reading timetable had the lowest pass percentage based on their final grade. Similarly, students with a good reading time plan had the lowest failure percentage based on their final grade.

#### Number of Student&#39;s Study Time affect the Final Grade

![image](https://user-images.githubusercontent.com/31987649/178657417-442e13df-dda6-4b7e-bcb2-21a52762b3d1.png)

_Figure 19: Bar graph of the study time and number of pass rate students._

The dark green color in the screenshot above represents the pass student rate, while the light green color represents the fail student rate. The graph above demonstrates that students with study time between 2 and 5 hours have a high pass percentage, whereas those with study time between 2 and 5 hours have a significant failing rate. According to the bar graph above, students who study for more than 10 hours had the lowest failure rate.

**Internet Role in a Student&#39;s Studies.**

![image](https://user-images.githubusercontent.com/31987649/178657374-276f937e-9db5-4146-aa6d-3ebe6e2a6049.png)

_Figure 20: Box plot of internet usage of student for the final exam._

The blue color box in the above box plot diagram indicates students who do not have access to the internet, while the orange color box shows students who have. Students that have access to the internet appear to fare better in their final grades, as seen in the box plot above. Also, the above graph shows that students who perform exceptionally well in their exams have access to the internet, as the box plot of students with access to the internet has a greater maximum value than the box plot of students without access. Similarly, as seen in the accompanying box map, pupils who do not have access to the internet have a lower median value than those who do.

**Attendance as per Age with their Pass Rate.**

![image](https://user-images.githubusercontent.com/31987649/178657324-cc9a23e5-6732-44a7-a5c5-7b9af583155b.png)

_Figure 21: Violin plot of attendance as per age with their pass rate._

The orange color in the above Violin plot represents the rate of pass students with their absence rate as per age, whereas the blue color represents the rate of failed students with their absence rate as per age. The median value is shown by the white dot in the violin plot above. The violin plot shows that there are the most value points in the range of 0 to 20. Similarly, in the age group of 18 to 19 data who had passed and had absent days, there is a large range of numbers. From the violin plot above, it can be deduced that students in the age bracket of 18 to 19 who have a lot of absence days may still do well in exams.

#### Alcohol Consumption Weekly and Daily with the Pass Rate

![image](https://user-images.githubusercontent.com/31987649/178657271-f2b6bbbd-315a-475d-b976-4cc6c340fa98.png)

_Figure 22: Bar graph of Alcohol consumption daily and weekly of students with the pass rate_

The green color bar in the above bar graph represents students who have not passed, while the grey color bar represents students who have passed. The bar graphs show the student&#39;s daily and weekly alcohol intake, as well as their pass and fail rate as determined by their final grade. Students that use very little alcohol on a daily and weekly basis have a high final grade pass percentage, as seen in the above bar diagram. Similarly, students who use a lot of alcohol on a regular and weekly basis are more likely to fail their final exams. It may be concluded from the graph above that student who consume very little alcohol have a high final grade pass rate.

#### Extracurricular activities of students as per their gender and pass rate

![image](https://user-images.githubusercontent.com/31987649/178657237-488fbc6b-b867-4a82-8c61-64986e67cd57.png)

_Figure 23: Swarm plot of students participate in extracurricular activities categorized according to their gender with pass rate._

The failed students are represented by the red filled circle in the swarm plot above, while the graduates are represented by the blue full circle. The graph on the left depicts students who do not participate in extracurricular activities and receive a final grade based on their gender, whereas the graph on the right depicts students who do participate in extracurricular activities and receive a final grade based on their gender. According to the graph above, men students participate in more extracurricular activities than female students. Male students who participate in extracurricular activities had a lower failing percentage in the final grade than female students who participate in extracurricular activities. According to the graph above, women who do not participate in any extracurricular activities have a high pass rate in their final grade.
  
