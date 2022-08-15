# Industry-Grade-Project
# Customer Engagement Enhancementin BFSI Industry
Background ParTechis an emerging subscription-based financial technology start-up that offers a range of services  to  its  customers,  including  bank  accounts,  debit  cards,  currency  exchange,  stock trading,  cryptocurrency  exchange,  and  peer-to-peer  payments.  As  with  many  subscription-based  businesses (especially in the FinTech domain), one of the main areas of concern for the company  has  been  customer  engagement  and  increasing  churn  rate.  They  need  assistance from  a team  of Data Scientists in quantifying successand driving their business teams towards an effective customer retention strategy.As Data Scientists,our objectiveis to build a data-driven, actionable, and effective solution for ParTech to help improve customer engagement and mitigate churn.

# Key-skill:
## Business understanding
## Data pre-processing
## Exploratory data analysis
## Feature engineering
    Defining target
    Designing predictive features
## Visualization
## Statistical/Machine Learning techniques including:
    Model tuning
    Model evaluation metrics
    Model validation
    Hypothesis testing 
    Experimentation 
## Process Flow
    Exploratory Data Analysisand Feature Engineering
    Find relevant insights  about the  company’s business to  build  a  clear  understanding  of  each feature  in  the datasets.  
    For  this,you  need  to  performExploratory  Data  Analysisand  Feature Engineering
    
    
## Differentiate between users through Visualizations<br><br>
     Establish a clear definition of customerengagementbased on a company’s business requirements. This willhelp youdifferentiate between engaged and unengaged users.      For this, you require relevantbusiness justification, visualizations, and/or modeling techniques.
## Predictive Model Building<br><br>
    Designengagement metric that show if customers are likely to be unengaged in the futureand the  early  warnings/drivers   of   unengagement.  Forthis, you need  to     predict  and  classify engaged/unengaged customers using machine learning techniques.
## Model Validation and Experimentation<br><br>
     Use  themodel  to  identify  the  most  unengaged  users.  For this, you need  to  help  set  up  an experiment to prove that the model works.
     
## Dataset Description<br><br>
    Three key datasets are provided by ParTech in the enterprise_datafolder for Data Scientists to explore. These tables consist of information on ~19.3k customers         collected over 17 months, at different levels of granularity, depending on the table under consideration. The details of each dataset are as provided below:


## Dataset 1: marketing_monthly_data.csv
    This table is maintained by ParTech’s in-house  business  team  to  keep  track  of  CRMactivities and  customer  profiles.  It  comprises  monthly  aggregated         data  on  customer  demographics, account details, devices, outbound notifications, etc.
## Business advice:
    ParTech’s internal analytics team often leverages this information to decide the monthly plan of customer outreach or any other form of modeling activities 
     
## Dataset 2: transaction_monthly_data.csv
     ParTech’s in-house  analytics  team  usesthe  table  to  comprehend  high-level  transactional patterns  of  customers.  It  comprises  of  summarized  monthly        view  of  customer  transactions, including details on value, direction, currency, type, state, etc. 
## Business advice:
    ParTech’s internal analytics teams often use this information to create monthly financial reports for senior business stakeholders or any other form of modelling       activities.
 ## Dataset 3: transaction_details_data.csv
    This table is owned and analyzed by ParTech’s in-house analytics team to understand granular transactional patterns of customers. It encompasses information on         each transaction for every customer in terms of datetime, value, state, and type.
 ## Business advice:
    ParTech’s internal analytics team uses this information to understand the low-level dynamicsof customer transaction behavior and in any other form of modeling         activities•ParTech’s internal analytics team advises that this table is likely to have some overlap of information with transaction_monthly_data.csvand needs to be     used judiciously•ParTech’s business team would prefer a bottom-up approach and advice on leveraging the granular information for deciding:othe definition of the       target metric which needs to be easy-to-understand, capture data intelligence as well as business value and actionabilityothe optimal window over which the target     metric needs to be measured at any point in time (e.g., 3-month future window)
 
 
 ## Tasks to be performed
 ### Task 1:
    It  is  crucial  for  you  as  a  Data  Scientist  to  gain  the  confidence  of  business  stakeholders  at  the very  outset  of  the  project  through  some         quick  wins  in  the  form  of  exciting  findings,  in-depth data understandings, and great visualizations. As  a  Data  Scientist,  you  need  to  dive  deep         into  the  datasets  (refer  to  the  set  of  the  following sub-tasks)  to  unlock  interesting  insights  about  customers,  their  transactional  behaviours,       ParTech’s business trends, etc. Also, you need to build a clear understanding of each feature in the datasets through a quick and efficient data quality report.
### Sub-tasks -Part A -[Exploratory Data Analysis using Tableau Public]
    1.What can be inferred from  the distribution of the total amount_usdtransactions across different transactions_state? (Hint: Use transaction_details_data)
    2.Which transactions_typehas  been  most  beneficial  to ParTechmonetarily?(Hint:  Only COMPLETED transactions directly add value to ParTech)
    3.Which type of transactions has the highest amount_usd of non-COMPLETED transactions?
    4.How does the count of new joiners and the total number of transactions by the new joiners vary across time (day-level)? 
    (Hint: Use user_created_date to identify new joiners) 
    5.What does the overall distribution of distinct users across different countries look like on the world map?
    6.What does the average birth_yearof users across different countries look like on the world map?
    7.Which plan_type is most popular among the users?
    8.How does the average distribution of each plan_typevary across yearmonth?
    9.What is the total number of SENT and FAILED notificationsacross yearmonth?
    10.What does the box-plot distribution of amount_usdand tx_countacross yearmonth tell us about the outliers?
    11.What inferences can be drawn based on average distributions of each transaction directionand transactions_typeacross ‘yearmonth’s?
### Sub-tasks -Part B -[Data Quality Report using Jupyter Notebook | Python3]
    1.Use  pandas-profiling  package  to  auto-create  summary  reports  within  the  notebook frame, for each of the three datasets Task 
    2:As highlighted in the problem statement, one of the critical areas of focus for ParTechis to understand customer engagement better. The first step towards           understanding engagement is to establish a clear and robust definition of the metric. The challenge is, there are no fixed definitions of engagement, and it often     needs to be customized based on a company’s business requirements.
    Through the following sub-tasks, Data Scientists need to build a metric that can help identify engaged users and differentiate between engaged and unengaged users.     The approach needs to be backed with necessary business justification, visualizations, rationale, and/or modeling techniques.
    
### Sub-tasks -Part A -[Data Handling using Jupyter Notebook | Python3]
    1.Convert the user_created_dateand created_datecolumns from marketing_monthly_data& transaction_details_datadatasets into usable datetime formats.  
    2.Considering2018, as the observation time-period, what are the steps needed to create a new data frame, such that it satisfies all of the following 
    criteria:
    Contains 1 record per customero
    Only COMPLETED transactions are considered
    Captures average 3-months behavior across the tenure of each customer along four engagement-specific dimensions, as stated below:
        1)Number of transactions (Use count of amount_usd)
        2)Total USD value of transactions (Use sum of amount_usd)
        3)Total distinct types of transactions (Use transactions_type)
        4)Total distinct days of transactions (Use created_date)
        
### Sub-tasks -Part B -[Unsupervised Learning using Jupyter Notebook | Python3]
    1.Use two popular clustering algorithms, K-means & Hierarchical, to combine the four engagement-specific dimensions into a single multi-class metric (Note:Outliers       may bias the clustering algorithms)
    2.Compare the centroid values of the two clustering algorithms across each dimension in each cluster
    3.Which of the two algorithms is a better choice for defining the engagement metric?
    4.How may the centroid values from the optimal algorithm be used to define a business rule for tagging engaged vs. unengaged users?
 ### Note:
    The above business-rule based engagement metric built on top of unsupervised modeling framework fits ParTech’s requirements (easy-to-understand, data intelligence,     business value, and actionability-driven engagement metric). However, beyond the scopeof this project, Data Scientists are encouraged to research further and           explore other robust approaches in designing an engagement metric as well.

### Task 3:
    To make the above design of the engagement metric useful to the business, ParTechneeds to know which customers are likely to be unengaged in the future. They also     need to understand the early warnings/drivers of unengagement so that action can be taken accordingly. To  achieve  this,  Data  Scientists  need  to  predict  and     classify  engaged/unengaged  customers using Statistical/Machine Learning techniques, based on the following sub-tasks.
    
### Sub-tasks -Part A -[Model Data Preparation using Jupyter Notebook | Python3]
    1.How  can  the  dataset(s)  be  joined  efficiently  to  create  a  single  dataframe,  containing  1 record per customer per yearmonth? (Note:avoid replication       of effort in case of overlap of information across any dataset(s))
    2.Assume  that  at  any  point  in  time, ParTechneeds  1-month  heads-up  to implement any action (i.e., the gap between feature window and target window needs to     be 1-month). Based  on  this  assumption,  create  a  binary  engagement  target  using  the  engagement metric definition from Task-2)
    3.What is the distribution of the target across each yearmonth? Is the target balanced?
    4.What   are   the   kinds   of   feature   engineering   that   can   be   done   using   the   available information? (Note:Input features directly correlated       with the target metric could lead to overfitting and misinterpretation)
 
 
 ### Sub-tasks -Part B -[Modelling Training and Validation using Jupyter Notebook | Python3]
 
    1.Split the data such that:
        Training data -80% till 201809
        Validation data 1 (out-of-sample) -20% till 201809
        Validation data 2 (out-of-time) -201812
        Scoring data -2019012.
    2.Train, tune and validate a Logistic Regression model
    3.Train, tune and validate an XGBoost classification model
    4.Based on the 2 models, what are the essential indicators of unengagement?
    5.Compare the performance of the 2 models. Which model should ParTechuse?
    6.What can cumulative gains plot tell us about the optimal sample size for testing?

### Task 4:
    Based  on Task-3, ParTechnow  wants  to  use  themodel  to  identify  the  most  unengaged  users and implement  some business actions to convert them  to engaged     users. To enable this, Data Scientists  need  to  help  set  up  an  experiment  to  prove  that  the  model  works  through  the following sub-tasks.
    
 ### Sub-tasks -Part A -[Model Scoring using Jupyter Notebook | Python3]
    1.Use the model developed in Task 3 to score on 201901 data
    
 ### Sub-tasks -Part B -[Experiment setup using Jupyter Notebook | Python3]
    1.Set up test and control groups (60%-40%) from the top 10% unengaged customers. Note: In real-life business scenarios, testing is not usually done on full base       but on a smaller set of customers for whom it will be most effective
    2.Perform an appropriate statistical test to test customer characteristics and check if control groups are similar
    
    
 ### Task 5:
    Detailed project report/synopsis.
    
    
