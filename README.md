# Employee_Performance_Analysis_Project
I have built the trained model where we can predict the Employees performance rating based on the given input. This model will help the company to take right decision based on the  employees  work parameters..
# Domain Analysis
Age: The age of the employee.
Gender: The gender of the employee (e.g., Male, Female, Other).
EducationBackground: The educational background of the employee (e.g., Engineering, Marketing, Science).
MaritalStatus: The marital status of the employee (e.g., Single, Married, Divorced).
EmpDepartment: The department in which the employee works (e.g., Sales, HR, Research & Development).
EmpJobRole: The role or position of the employee within the company (e.g., Manager, Analyst, Technician).
BusinessTravelFrequency: The frequency of business travel undertaken by the employee (e.g., Rarely, Frequently, Never).
DistanceFromHome: The distance of the employee's home from the workplace.
EmpEducationLevel: The education level of the employee (e.g., High School, Bachelor's Degree, Master's Degree).
EmpEnvironmentSatisfaction: Employee's satisfaction with the work environment.
EmpHourlyRate: The hourly wage rate of the employee.
EmpJobInvolvement: Employee's level of involvement in their job.
EmpJobLevel: The job level or hierarchy within the company.
EmpJobSatisfaction: Employee's satisfaction with their job.
NumCompaniesWorked: The number of companies the employee has worked for previously.
OverTime: Whether the employee works overtime (Yes or No).
EmpLastSalaryHikePercent: The percentage increase in the employee's last salary hike.
EmpRelationshipSatisfaction: Employee's satisfaction with their relationships at work.
TotalWorkExperienceInYears: Total work experience of the employee in years.
TrainingTimesLastYear: The number of times the employee was trained last year.
EmpWorkLifeBalance: Employee's perceived work-life balance.
ExperienceYearsAtThisCompany: The number of years the employee has worked at the current company.
ExperienceYearsInCurrentRole: The number of years the employee has been in the current role.
YearsSinceLastPromotion: The number of years since the employee's last promotion.
YearsWithCurrManager: The number of years the employee has been with the current manager.
Attrition: Whether the employee has left the company (Yes or No).
PerformanceRating: The performance rating of the employee.

# Final Conclusion of EDA
* Gender: After analysing the graph , we got male and female are giving the same performance in company.

* EducationBackground: Most of the bad performing employees belong to life science, Medical and marketing.

* MaritalStatus: Most of the employees performing bad are married.

* EmpDepartment: Most of employees performing bad are working in Sales or Research & development department.

* EmpjobRole : Most of the employees performing bad have Job role as sales executive,sales representative,HR,laboratory technician and research scientist,manager R&D and finance manager.

* BusinessTravelFrequency : Travel doesn't make much of a difference in the percentage of bad performing people. Bad performers in each category are 1/5 of the average performers and a little higher than the great performers in that category.

* EmpEnvironmentsatisafaction : Employees who are not satisfied with the office environment perform poorly than their peers.

* Empjoblevel: Employees at job level 1 have fewer bad performers on average compared to other job level. The bad to average performers ratio is 1:6 compared to 1:3 or 1:4 for other job levels.

* Empjobsatisfaction : The highest number of bad performers by volumne are with category 3 and 4. 

* EmpWorkLifeBalance:  Employees having 3 level work life balance have maximum bad performers by volume, however the ratio of bad performers to all employees looks similar in 2,3 and 4.

* EmphourlyRate :In EmphourlyRate, Employees having hourlyRate 85 has maximum bad performers on average and by volume.

* EmpLastSalaryHikePercent :In EmpLastSalaryHikePercent, employees who got less than 20 % last salary hike are          performing bad.

* ExperienceYearsAtThisCompany : In ExperienceYearsAtThisCompany,employees who have maximum experience approx 10 to 23yrs in     this company they are performing bad.

* ExperienceYearsInCurrentRole:Employees who have between 6 to 12 years experience in current role are performing bad.

* YearsSinceLastPromotion : Employees who did not get promotion in last 2yrs are performing bad.   

# Conclusion of Model Comparison Report
We applied various algorithms to predict employees performance using historical data. Initially, we used six different algorithms such as SVM Classification,Logistic regression, Decision tree classification, ANN MLP_classifier,Random forest classification and XGB classifier and assessed their accuracy scores. Among them, random forest classification and xgb classifier showed highest score performance, achieving an accuracy of 0.9333% with hyperparameter tuning. This level of accuracy stands out when compared to the performance of other models.but random forest classification giving testing accuracy score 93% and training accuracy score 100% , indicated that model is overfitting.

Considering the remarkable performance for prediction of employess performance and xgb classifier algorithms could be considered the best choice for prediction. It models exhibit a 0.9333% accuracy rate, as shown in the model DataFrame.

# Data Analysis Report
## About dataset
In this project we saw there is a company INX future Inc,(referred as INX),one of the leading data analytics and automation
solution provider with over 15 years of global business presence.INX is consistently rated as top 20 best employers for past 5 years. INX human resource policies are considered as employee friendly and widely perceived as best practices in the industry. But in recent years, the employee performance indexes are not healthy and this is becoming a growing concern among the top management. There has been increased escalations on service delivery and client satisfaction levels came down.
## Goal of the project
So based on the problem statement, we have to understand all the given features which are very important and we will understand the employees behavior.
We have to analyze the problem of company as well as employees perspective, where the company can grow while employees also be  satisfied with their job.
So we have to build the model predictor using the machine learing algorithms,where our model can predict the employees performance based on the input features. 
##  Basic check
Initially,I did the domain analysis which is very crucial for every project. After doing the analysis ,I understood the dataset and what modifications will be required during the project.
Saw there are 1200 rows and 28 columns. I have done the basic check in dataset where we checked head,shape,tail,info and describe etc. We got there are no null values present in features and some features are present in catogorical. We have to convert that in numerical using the encoding techniques.We saw the target variable is imbalanced. We have to balance the data using the smote techniques.
This dataset have some unnessceries feature so we need to drop that features which are irrelavent.

## Exploratory data analysis(EDA):
I have Seperated the dataset in three parts based on the datatype and gave the variables name such as categorical data, descrite data and continues data. After that i have done the univariate analysis and bivariate analysis of each variables and extract the insight which i have explained after analysis.

## Data Preprocessing: 
In preprocessing I have checked the null values and this dataset do not have null values. after that I have replaced the categorical features into numerical using the manual encoding techniques and showed the target variables value which are in not order like (2,3,4) so i used the  manual encoding with target variable and made them in orders like(0,1,2) because some model does not work with this values.

## Feature selection: 
In feature selection , I have dropped the unwanted features because these unwanted features can negatively impact model performance, lead to overfitting,increase computational costs and fits noise in the data.
Checked the correlation between the variables ,got there are no high correlation between each other.After that We have done the model creation x and y and splitted the data into training and testing for model build up.
I have balanced the target variable using the smote technique. 

## Model selection:
I have used the various algorithms such as SVC,logistic regression, Decision tree classification,ANN MLP clssifier,random forest classification and XGb classifier.I have used the hyperparameter tuning with few algorithms .Where i got some success in model performance using the hyperparameter tuning techniques.
We saw xgb classifier gave us the best accuracy score which is 93.33%. It suggests that your model is performing quite well in terms of making correct predictions for the employees performance rating.
(NOTE:The test accuracy score is 93% and train accuracy score is 97% after hyperparameter tuning we got this scores and before hyperameter tuning model was overfiting where test accuracy 92% and train accuracy is 100% such as having a training accuracy of 100% (1.0) and a test accuracy of 92%, is a strong indicator of overfitting.But Now The 4% difference between training and test accuracy (97% vs. 93%) is relatively small, suggesting that the model is not severely overfitting.It is showing improved generalization performance.)

## Model Dataframe:
I have created the model comparison dataframe ,where we can see all the used algorithms accuracy score ,f1 score and hyperparameter tuning accuracy scores.
# Report on Challenges faced
I have faced some issues while i was doing the EDA to understand the graph. I can extract some valuable insight which would be required to make better decision against the employees ,who are not performing good in company. Therefore, I have extracted the insight and explained each feature well. In model selection,few models performance were not good and gave less accuarcy score so here i used the Hyperparameter tuning technique and got good accuracy score and our model is showing generalized performance.

# The following insights are expected from this project.
## 1. Department wise performances
I have done the EDA, got the insight in Sales and Research & development most of employees are performing bad and In development employees are performing good as compared to other.

In job role sales executive,sales representative,HR,laboratory technician and research scientist,manager R&D and finance manager are performing bad and developer,technical architect,business analyst ,delivery mangager and technical lead are prforming average and good

## 2. Top 3 Important Factors effecting employee performance
There are several factors effecting employee performance and i will explain few factors:

Empsalaryhikepercent: We saw that employees who have got more than 20% hike are performing good. Most of the employees have average performance, but those who got less than 20% have bad performance.

Empcurrentjobrole: We saw that employees having less than 2 years of experience in their current role have very good performance. While the employees have more than 6 years experience in current role are not doing well performance.

EmpEnvironmentsatisafaction:We analysed the graph and got that employees who have 1 and 2 environment satisafaction level are performing bad as compared to other.

## 3. A trained model which can predict the employee performance based on factors as inputs. This will be used to hire employees.
In this project I have used various algorithms to build the model. As I have mentioned in dataframe and The model xgb classifer gave the accuracy score 93%, which indicates that our model is quite well in term of making correct predictions for employees performances based on the factors as input.

## 4. Recommendations to improve the employee performance based on insights from analysis.
After Analysis i will recommend to improve the environment statistfaction where employee feel motivated and have friendly culture.
If employees are working last few year on some project so they will feel bored and fatigued ,so give them some new challenging work. If employees are performing well, company should appreciate them and compensate accordingly.
The employees who are working for more than ten years need to be re-evaluated per their experience and their contribution to the organization. They should be asked to up skill and perform better or should be asked to leave if they don't add enough value according to their roll.
The employees who got lesser getting hikes should be coached that hikes are performance driven and if they focus on adding value, their efforts will be rewarded. Also, some revaluation and corrections can be done for some deserving people if any.
A proper coaching and training infrastructure should be developed for employees at the bottom level to be able to understand their role and contribute better with the right mentorship. Timely evaluations should happen to push them to learn faster.
Organisation needs to dig deeper within particular departments which are not doing well like sales and R&D. Possible reasons could be not having an attractive incentive policy in sales, or not having enough tools to be able to deliver results faster in R&D departments. Take anonymous feedbacks to collect the pain points and take actions to fix them.
                                            ____DONE______

