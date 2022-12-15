# What makes a great candidate to land a job in stem?
#### Gilberto Arellano | CPSC 392 Final Project
Im attempting to create predictive models to figure out what makes a succesful candidate to land a job in tech. 
I will be using data from the 2017 Kaggle survey, in which collected responses in regards to people's salary, education, programming language recommendations, etc.

### Questions to Answer
---
#### 1) Who is the most ideal candidate to land a job in tech?
What are the characteristics needed to land a job in this field? Are employers targeting people with a college education? Did an internship in undergrad? A couple of portfolios under their belt? Or is having a solid reference enough? We will use a logistic regression model since the output we are predicting is what are the variables needed to land a job. Doing so we can analyze the coefficients and decide which factors has the most impact

#### 2) Are employers targeting people through job boards or referals?
We are going to use both the logistic regression and regularatization methods to see where employers are mostly looking for candidates through.

#### 3) Is there a relation between age and wage?
After plotting the relationship between 'Age' and 'SalaryCompensation', I determined to use Gaussian Mixture as the clustering method since there is no clear seperation in which other models such as DBSCAN would struggle to differentiate. 

### Results
---
Despite our logistic regression model having a high accuracy rate, it is skewed since the majority of the responses are from people who are employed. We do not have sufficient data to characterize what could possible be an unemployed person.
[Number of Employed/Un-Employed](raw.githubusercontent.com/arell110/CPSC_392_Final_Project/tree/master/graphs_images/employment_status.png)

Our Logistic and Lasso model performed similar with a MAE at around 0.19. Although we are going to use the Ridge Model as reference since the MAE was slightly better at 0.14. Per our results we can infer that having a higher education (bachelors, masters, PhD) has the most impact along with looking for a job online through a job board (indeed, glassdoor, linkedin, etc.) The factors that played the least were gender and age

[Ridge Model's Coefficients](raw.githubusercontent.com/arell110/CPSC_392_Final_Project/tree/main/graphs_images/ridge_coef.png)

Our clustering model, GM, was not able to differentiate the cluster well with the data that was given. It has a low sillhouette score of 0.35, meaning there is not a lot of seperation nor density between the 3 clusters. Thus it would not be best to use this model to infer the different type of jobs using someones age and annual salary.

[GM Cluster](raw.githubusercontent.com/arell110/CPSC_392_Final_Project/tree/main/graphs_images/gm_cluster.png)

### Sources
---
- [Kaggle Submission](https://www.kaggle.com/code/smcnish71/what-should-job-seekers-do-to-get-a-job/report) by Shannon: For the dataset and a reference on how to have a similar theme
- [plotnine documentation](https://plotnine.readthedocs.io/en/stable/): On how to manipulate and enhance ggplot

