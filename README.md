# Lead Scoring Case Study

## Problem Statement
An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses. 

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%. 

Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone. A typical lead conversion process can be represented using the following funnel:

![image](https://github.com/user-attachments/assets/02e1b7c1-0dae-437a-bb46-b3f64caa07ce)

As you can see, there are a lot of leads generated in the initial stage (top) but only a few of them come out as paying customers from the bottom. In the middle stage, you need to nurture the potential leads well (i.e. educating the leads about the product, constantly communicating etc. ) in order to get a higher lead conversion.

X Education has appointed you to help them select the most promising leads, i.e. the leads that are most likely to convert into paying customers. The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with a higher lead score have a higher conversion chance and the customers with a lower lead score have a lower conversion chance. The CEO, in particular, has given a ballpark of the target lead conversion rate to be around 80%.

 
## Data
You have been provided with a leads dataset from the past with around 9000 data points. This dataset consists of various attributes such as Lead Source, Total Time Spent on Website, Total Visits, Last Activity, etc. which may or may not be useful in ultimately deciding whether a lead will be converted or not. The target variable, in this case, is the column ‘Converted’ which tells whether a past lead was converted or not wherein 1 means it was converted and 0 means it wasn’t converted. You can learn more about the dataset from the data dictionary provided in the zip folder at the end of the page. Another thing that you also need to check out are the levels present in the categorical variables. Many of the categorical variables have a level called 'Select' which needs to be handled because it is as good as a null value (think why?).

### Key Steps:

1. **Data Preprocessing**:
   - The dataset contains around 9000 leads with various attributes like Lead Source, Last Activity, and Total Time Spent on the Website.
   - Several irrelevant features were dropped (e.g., `Magazine`, `Prospect ID`, `Receive More Updates About Our Courses`) to streamline the analysis.
   
2. **Exploratory Data Analysis**:
   - Insights were gathered from various features:
     - **Lead Origin**: Approximately 52% of leads came from "Landing Page Submissions," with a 36% lead conversion rate.
     - **Current Occupation**: 90% of the leads were unemployed, but "Working Professionals" had a 92% conversion rate despite being only 7.6% of total leads.
     - **Lead Source**: Google had a lead conversion rate (LCR) of 40%, while references had the highest conversion rate at 91%.
     - **Last Activity**: "SMS Sent" had the highest conversion rate of 63%.
     - **Specialization**: Courses like Marketing Management and HR Management contributed significantly to conversions.

3. **Model Development**:
   - A logistic regression model was built to assign a lead score between 0 and 100 for each lead. The model uses features such as lead source, last activity, and current occupation to predict the likelihood of conversion.

4. **Evaluation**:
   - The model achieved:
     - **Train Data**:
       - Accuracy: 81.11%
       - Sensitivity: 80.74%
       - Specificity: 81.33%
     - **Test Data**:
       - Accuracy: 80.77%
       - Sensitivity: 80.27%
       - Specificity: 81.10%

### Goals of the Case Study

- Build a logistic regression model to assign a lead score between 0 and 100 to each of the leads.
- Identify the most promising leads for the sales team to focus on.
- Evaluate model performance using metrics like accuracy, sensitivity, and specificity.

### Results

  - The logistic regression model successfully assigned lead scores to potential customers, with high   conversion probabilities identified.
  - The model’s sensitivity and accuracy were in line with the company’s goal of achieving a lead conversion rate of around 80%.



