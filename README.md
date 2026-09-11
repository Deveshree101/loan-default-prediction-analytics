# **Project Overview**

### **Objective**

The goal of this project is to predict whether a low-income borrower is likely to repay a loan or not. By studying patterns in income, expenditure, and past repayments, the project aims to help lenders make fair and confident loan decisions.

### **Context**

Predicting loan repayment is challenging when borrowers lack formal credit histories ,the project analyzes borrower data to uncover patterns that can guide smarter lending decisions. This project simulates a fintech startup lending scenario . It focuses on understanding the factors that influence a borrower’s repayment behaviour. The goal of the project is to generate insights from data and help companies become aware of the defaulters well in advance. [Read Detailed Context](Detailed_Context.md)

### Problem Statement

Lenders struggle to predict loan repayment among low-income borrowers due to irregular incomes and limited credit histories, leading to higher default risk and restricted access to credit for this segment.

### **Tools**

I employed Python Libraries for this project , as they allow for powerful and reproducible analysis. I used random for data generation,  pandas for data manipulation and matplotlib or seaborn for creating charts.

### **Methodologies**

Generated data for this project using python code .The data was loaded into the code, further it was cleaned and analyzed using EDA( Exploratory Data Analysis) and in the end the data was visualized.

# **The Approach and Process**

Since the detailed credit histories or prior loan data was unavailable, it was important to deeply understand the available information about borrowers- their income levels, job types, and loan behavior. To tackle the problem, I first generated a realistic dataset representing GramBond’s borrowers. Then, I cleaned the data to handle missing or inconsistent values, followed by exploring and visualizing it through EDA to uncover patterns that can not be seen at first glance. Each step helped move closer to understanding which borrower segments are most at risk.

### Process
- [Data Generation](#Data-Generation)

- [Data Loading](#Data-Loading)
- [Data Exploration](#Data-Exploration)
- [Data Cleaning](Data-Cleaning)
- [Exploratory Data Analysis](#EDA)
    - [Univariate Analysis](#Univariate-Analysis)
    - [Bivariate Analysis](#Bivariate-Analysis)
    - [Multivariate Analysis](#Multivariate-Analysis)
- Final Conclusion and Recommendations

### **Data Generation**

The initial step involved generating synthetic data using Python libraries like random, pandas, NumPy to simulate real-world dataset. The dataset has the following columns-

- **Age**: The age of the borrower **(in years)**
- **Loan_Amount**: The total loan amount sanctioned to the borrower **( in INR)**
- **Income_Level:** Categorized income range of the borrower as **Low, Medium or High**
- **Income_Source**: The primary source of income such as **Daily Wage, Salary, Small Business, Pension, or Commission**, showing the nature of earnings.
- **Default_Status**: The repayment status, whether the borrower **paid** the loan or **defaulted**



### Data Exploration

In order to understand what the dataset actually contains, data exploration can be really helpful. It can help in identifying the missing or inconsistent information early. The data exploration phase ensures that further cleaning and analysis are based on a clear understanding of what’s actually inside the dataset.

image

From the summary statistics, the average age of borrowers is around 41 years, indicating that the dataset mainly represents an active working population. The average loan amount is approximately ₹29779 which is consistent with micro-loans typically offered to blue-collar workers. These averages validate that the generated data aligns with realistic lending patterns for this segment.

### **Data Cleaning**

I cleaned the data by handling missing values, removing duplicates, and ensuring consistent data types. Logical checks were also applied to verify that all records represented valid borrower profiles (e.g., age above 18, positive loan amounts). This ensured that further analysis and insights were based on accurate, realistic data. 

### **Exploratory Data Analysis (EDA)**

Exploratory Data Analysis (EDA) helps us find patterns and insights in the data. It’s done by looking at the data in three ways , **univariate** **analysis** (examining one variable at a time), **bivariate analysis** (comparing two variables), and **multivariate analysis** (examining many variables together). The purpose of this analysis is to understand who our customers are and how they repay their loans. By looking at details like their age, income level, and main source of income, we want to find patterns that show why some people are more likely to default than others.

### **1. Univariate Analysis**

 In this step, I looked at each variable one by one to understand how the data is spread and if there are any unusual values. This helps to spot outliers, see basic patterns like borrower income or age range, and get a first idea of the data before comparing different variables with each other. 

- **Age Distribution:**



!image.png

**Interpretation-** The age distribution of borrowers appears relatively uniform across all age ranges between 18 and 65, suggesting that lending activity is spread evenly across generations. There are mild peaks around the early 20s and early 60s, which may indicate that both younger individuals beginning their financial journey and older borrowers approaching retirement are actively seeking loans. Overall, the dataset reflects a well-balanced mix of borrowers across different age groups.

- **Loan Amount Distribution**


!image.png

**Interpretation**: Borrowers are fairly evenly distributed across loan amounts, with minor fluctuations. There is no strong skew or concentration at a particular loan amount, indicating a fairly uniform loan distribution.

- **Income Source Distribution**



!image.png

**Interpretation**: The plot suggests that the number of people that take loans are in this order ,salaried followed by daily wage earners followed by small business who are then followed by commission and least borrowers are from pension group.

- **Income Level Distribution**



!image.png

**Interpretation**: Around 40% of the borrowers belong to the low-income category, another 40% to the medium group, and around 20% to the high-income group. The percentage mentioned here is an approximate estimate not the exact numbers.

- **Default Status Distribution**



!image.png

**Interpretation:** The above plot shows that out of the whole dataset nearly 3600 people have paid back there loans and around 1250 people have defaulted over there loans. Above mentioned numbers are just an approximation from what can be interpreted from the graph.

---

### **2. Bivariate Analysis**

Bivariate Analysis helps explore how two variables relate to each other. For example, how income level affects loan default rate, or how age connects with loan amount. This step adds context to the findings and helps uncover meaningful patterns that univariate analysis might have missed.

- **Income_Level vs Default_Status**



!image.png

**Interpretation:** The chart shows that low-income borrowers have a visibly higher number of defaults compared to medium and high-income groups. This indicates a clear negative relationship between income level and repayment reliability.

- **Income_Source vs Default_Status**
    
   
    

!image.png

**Interpretation:** The chart shows how different income sources affects the default status when loan is taken. We can conclude from the above chart that -

low-income borrowers have a visibly higher number of defaults compared to medium and high-income groups. This indicates a clear negative relationship between income level and repayment reliability.

1. Borrowers with stable income sources ( salary, pension) have lower default rates.
2. Daily wage earners, due to unstable source of income, have highest default rates.
3. Small business have moderate risk while commission based earners( although a small group) shows some defaults.

- **Age vs Default_Status**
   

!image.png

**Interpretation:** The chart shows the number of borrowers in each age group (18–25, 26–35, etc.) and their loan repayment status (Paid vs Defaulted). We can conclude from the above chart that-

1. Middle-aged borrowers (36–55) are more likely to repay loans. 
2. Younger borrowers (18–35) have a higher proportion of defaults compared to their total loans. 
3. Age seems to influence repayment behavior, with repayment improving as borrowers get older.

---

### **3. Multivariate Analysis**

In this step, I explored how multiple factors together affect loan repayment. This helps identify deeper patterns like which combination of income level and source makes someone more likely to default.

- **Income Source vs Income Level vs Default Status**


!image.png

**Interpretation:** The above multivariate analysis charts show that-

1. People with **regular jobs or pensions** mostly **pay back their loans on time**. 
2. Those with **daily wages or small businesses** **miss payments more often**, especially when their income is low or medium. 
3.  Borrowers with **higher income** are **less likely to default**. Simply put, **steady and higher income means fewer chances of defaulting**. 

- **Income Level vs Loan Amount vs Default Status**



!image.png

**Interpretation:** The above chart shows loan amounts for different income groups: High, Medium, and Low. Each group is split into people who paid back their loan and people who defaulted. People who **defaulted** usually took slightly **higher loans**. Higher loans in low and medium incomes are more likely to default.

---

# Final Conclusions and Recommendations

### Key Findings

1. **Income level is the biggest risk factor**
- Low-income borrowers default 40% of the time
- Medium-income borrowers default around 20% of the time
- High-income borrowers default the least with 10% of the time only.
1. **Income source matters a lot**
- Daily-wage earners have the highest default rates followed by pension holders.
- Salary and small business owners repay better.
1. **Loan amounts don’t tell the full story**
- Defaulters and loan payers both borrow the similar amount.
- But low-income people taking larger loans are riskier.

### Strategic Recommendations

**1. Intelligent Group Composition** 

- Avoid clustering all high-risk borrowers together
- Integrate various income levels and sources within each JLG group
- Exercise heightened caution with pension and commission earners

**2. Group Risk Assessment** 

- Assess the collective risk for the entire group rather than individual members
- Disallow groups with an excessive number of high-risk individuals
- Formula: Income Level (45%) + Income Source (30%) + Loan/Income Ratio (25%)

 3**. Utilize Social Pressure Early On** 

- Dispatch payment reminders to the entire group instead of just individuals
- Facilitate group communication via the app
- Notify the group prior to any defaults occurring so they can take action

 4**. Progressive Lending Framework** 

- Groups that perform well gain access to larger amounts and improved rates
- This fosters trust and encourages responsible repayment behavior

### **Conclusion**

**Income level** along with **income source** serve as GramBond's most reliable indicators in the absence of credit history. Leverage this information to create well-balanced JLG groups, establish prudent loan limits, and promote group accountability from the outset. This strategy is expected to decrease defaults by 30-40% while continuing to support blue-collar workers and preserving robust NBFC partnerships for sustainable growth.
