# UCB-Project-One

## Title: Insurance Policy Marketing Team Analysis

+ Group Members: Darley Chen, Nelson Lin, Anusha Balasubramanian, Cynthia Street, Tico Brown

## Topic: Customer Segmentation Data

+ The marketing team is tasked with analyzing a customer segmentation dataset provided by an insurance company aims to maximize profit, enhance customer service, and improve key performance indicators (KPIs). The dataset encompasses various dimensions of customer information, including demographic details, socio-economic factors, behavioral insights, and individual preferences.
+ By analyzing these diverse dimensions of customer data, the marketing team can identify distinct customer segments, tailor insurance offerings to meet specific needs, optimize pricing strategies, enhance customer satisfaction, and ultimately improve KPI performance. The insights derived from the dataset will inform targeting marking campaigns, product development initiatives, and customer service enhancements, ensuring the insurance company remains competitive and responsive to evolving customer preferences.
+ Tools: Several tools are applied to enhance the analysis of the customer segmentation dataset provided by the insurance company.
  + Jupyter Notebook: The platform for executing codes and viewing outputs immediately, fostering an interactive and exploratory workflow.
  + Pandas: Python library for data manipulation and analysis.
  + Matplotlib: Python library for visualization and customization.
  + Statistics: Conclusion includes valuable insights into the underlying patterns and relationships in the data. The team applied descriptive statistics, hypothesis testing, and correlation and regression analysis.

## Data Introduction

+ The customer segmentation dataset presents a multifaceted business challenge ripe for analysis and optimization. It encapsulates a rich tapestry of customer attributes essential for delineating market segments and tailoring strategies. Comprising vital columns such as customer ID, age, gender, marital status, education level, geographic details, occupation, and income level, it provides a comprehensive portrait of clientele demographics. Furthermore, it delves into nuanced customer behavior, including interactions with customer service, insurance products owned, insurance coverage and premium amounts, policy types, preferred communication channels, etc. Each data point serves as a cornerstone in the intricate mosaic of customer segmentation, offering insights crucial for deciding targeted marketing campaigns, refining product offerings, and enhancing customer satisfaction.

## Data Processing Pipeline

+ The raw dataset contains 21 columns, some of which lack clear self-explanation, prompting the marketing team to formulate assumptions during preprocessing. For instance, concerning policy choices, we encountered ambiguity between two columns: "behavioral data" and "insurance products owned". Opting for clarity, we utilized "insurance product owned" exclusively for subsequent analysis. Additionally, upon detecting approximately 20% duplicates (based on Customer IDs), we elected to treat each entry as a distinct customer to ensure comprehensive dataset analysis. Introducing an auxiliary column labeled "Customer Number" facilitated this approach. Furthermore, while the "segment" column's significance eluded our comprehension, its potential relevance in analysis remains acknowledged, warranting further exploration.
+ After stating the assumptions and completing the data cleaning and preprocessing steps, the team concentrated the analysis on specific inquires and seeks out discernible trends within the dataset.
  + Relationship Comparison: Income Level vs. Insurance Coverage Amount
  + Relationship Comparison: Occupation vs. Communication Channel
  + Relationship Comparison: Age vs. Premium Coverage Amount
  + Relationship Comparison: Marital Status vs. Policy Type
  + Relationship Comparison: Age vs. Coverage Amount

## Complete Analysis & Demo & Findings Summary

+ Relationship Comparison: Income Level vs. Insurance Coverage Amount:
  + The team aimed to explore the correlation between coverage amount and income levels, initially presuming that individuals with higher incomes would opt for greater coverage. However, our analysis revealed a negligible correlation of -0.018 between insurance coverage and income level, indicating a low association. Across various income brackets, we observed minimal discrepancies in coverage amounts among individuals with comparable education levels. Interestingly, regardless of income level, customers tended to select lower coverage amounts. This suggests a common preference for lower coverage ranges among individuals across different income brackets.
    
  + ![Alt text](Project%201%20Images/Income%20Level%20vs.%20Coverage%20Amount.png)
 
  + ![Alt text](Project%201%20Images/Counts%20of%20Education%20Level%20by%20Income%20Level.png)
 
  + ![Alt text](Project%201%20Images/Counts%20of%20Coverage%20Range%20by%20Income%20Level.png)


+ Relationship Comparison: Occupation vs. Communication Channel
  + Null Hypothesis - A direct correlation exists between customers' occupations and their preferred contact methods.
    + Utilizing the provided DataFrame, we employed the groupby() function to filter occupations and count the occurrences of preferred communication channels.
    + Subsequently, a bar chart was generated using matplotlib to visualize the comparison.
    + To validate the relationship, correlation analysis was conducted, employing the Chi-square test for this categorical data. Additionally, we determined the p-value to ascertain the strength of evidence.
    + Furthermore, an additional visualization was crafted for the marketing team, illustrating the preferred contact times according to customers' occupations.
  + The null hypothesis posits a direct correlation between customers' occupations and their preferred contact methods. This assertion was substantiated by employing the Chi-square test, yielding a result of 366.17. Notably, the data revealed an exceedingly low p-value, affirming the unlikelihood of this occurrence being random. Across all occupations, in-person visits followed by phone calls emerged as the optimal contact methods for customers. To provide supplementary insights for the marketing team, we also presented the preferred contact times, demonstrating a preference among all occupations for weekend mornings.
 
  + ![Alt text](Project%201%20Images/Preferred%20Communication%20Channels%20by%20Occupation.png)
 
  + ![Alt text](Project%201%20Images/Preferred%20Contact%20Time%20by%20Occupation.png)


+ Relationship Comparison: Age vs. Premium Coverage Amount
  + Initially, the team categorized age and put them in bins and utilized the mean function to compute averages for various policy types present in the dataset, including family, business, group, and individual. The team constructed a dataframe and consolidated my findings into a unified table and generated a line chart illustrating the relationship between premium amounts and age groups to visually interpret the results across different policy types.
  + Conclusion:
    + Family policies tend to have lower premium coverage compared to that of other policy types.
    + Age group between 40 - 55 has lower premium coverage amount on average compared to that of other age groups.
    + Customers, in the age group of 55 - 70, have higher premium coverage amount across policy types due to age associated risks.

    + ![Alt text](Project%201%20Images/Average%20Premium%20Amount%20by%20Age%20Group.png)
      
+ Relationship Comparison: Marital Status vs. Policy Type
  + The team conducts an analysis on the relationship between Marital Status and Policy Type within a customer segmentation dataset.
    + We start by calculating the totals representing the count of observations for each combination of Marital Status and Policy Type.
    + Subsequently, we create a pivot table to organize the data, dividing the counts by policy type to generate percentages for marital status within each policy type. This information is then visualized through pie charts, with each chart representing the distribution of marital status for a specific policy type.
    + A pie chart depicting the overall totals by marital status across all policy types is generated. This analysis aims to uncover any potential correlations or patterns between marital status and policy type within the dataset, providing valuable insights for targeted marketing strategies or product offerings.
    + From the Totals by Marital Status analysis, it indicates that the two largest populations are Married (24.7%) and Divorced (24.6%)
   
    + ![Alt text](Project%201%20Images/Marital_Status_Distribution_for_Business.png)
      
    + ![Alt text](Project%201%20Images/Marital_Status_Distribution_for_Family.png)
      
    + ![Alt text](Project%201%20Images/Marital_Status_Distribution_for_Group.png)
      
    + ![Alt text](Project%201%20Images/Marital_Status_Distribution_for_Individual.png)
   
    + ![Alt text](Project%201%20Images/Totals%20by%20Marital%20Status.png)
    
+ Relationship Comparison: Age vs. Coverage Amount
  + The analysis conducted aimed to investigate the relationship between age and coverage amount among customers.
    + Initially, the dataset was prepared by extracting relevant columns, including customer number, age, and coverage amount. Age was categorized into four distinct brackets: "<20", "20-40", "40-60", and "60-80", facilitating the segmentation of customers based on age ranges.
    + The mean, median, variance, standard deviation, and standard error of the mean (SEM) were calculated for coverage amounts within each age bracket.
    + Subsequently, an analysis of variance (ANOVA) was performed to assess the differences in coverage amounts across the age groups.
    + The results revealed an F-statistic of 0.817 and a corresponding p-value of 0.484, indicating that age does not have a significant impact on average coverage amounts among the customer segments analyzed in this study.

## Challenges and Future Opportunities
  + The customer segmentation dataset presents both challenges and future opportunities for analysis.
    + Inspired by the Pareto principle, which suggests that roughly 80% of effects come from 20% of causes, we discerned that policies 1 and 2 within the "insurance product owned" column accounted for approximately 50% of sales and total insurance amounts. This revelation prompts the possibility of conducting a focused analysis solely on these two policies to uncover more prominent trends.
    + Certain columns, such as "segment," remained untapped due to a lack of understanding of their contents. However, reaching out to the data source for clarification could facilitate a more comprehensive analysis by leveraging potentially significant variables.
    + Time constraints hindered the exploration of geographic information through API key-related analysis, representing a promising avenue for future insights.
    + The absence of time for benchmarking against external sources limited the validation of findings. For instance, comparing our data against auto insurance rates by age revealed a correlation between premium coverage amount and age, echoing industry trends. Employing similar benchmarking techniques across other analyses could enhance the robustness of our findings and ensure the validity of the dataset's insights.
  + As the team navigates these challenges, addressing them presents opportunities to refine our analytical approach and glean deeper insights into customer segmentation dynamics.

## Please see the Jupyter Notebook file for detailed analysis and images