Online Retail Transactions Analysis Project


This project involves the analysis of online retail transactions data to extract meaningful insights and trends. The dataset used contains various attributes related to online retail sales, including invoice numbers, stock codes, descriptions, quantities, invoice dates, prices, customer IDs, and countries.



# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)



## Dataset Content
The dataset we used was provided by Abhishek Ranjan on Kaggle and can be found here: https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset/data

The dataset contains the following columns:
- StockCode: A code used to identify the product that was purchased
- Description: A brief description of the product that was purchased
- Quantity: The quantity of the product that was purchased
- InvoiceDate: The date and time that the purchase was made
- UnitPrice: The price of one unit of the product that was purchased
- CustomerID: The unique identifier for the customer who made the purchase
- Country: The country where the customer who made the purchase is located
- We also created an additional field called TotalPrice, which is calculated by multiplying the Quantity by the UnitPrice.


## Business Requirements
The company wants to improve profitability by understanding customer behaviour, identifying best-selling products, reducing returns, and targeting the right customer segments.
- Improve customer retention through segmentation and targeted strategies.
- Optimise inventory management by reducing returns and tracking product demand.
- Understand seasonal trends to align marketing campaigns with peak demand.

## Ethical considerations
All data was handled in accordance with relevant data protection regulations and ethical guidelines. This included anonymising personal information and ensuring that the data was used solely for the purposes of this analysis with no personal identifiable information being exposed. 

## Analysis techniques used
We used a variety of analysis techniques including:
- ETL (Extract, Transform, Load) processes to clean and prepare the data for analysis using Python and Pandas within Jupyter notebooks.
- Data visualization using Matplotlib and Seaborn to create charts and graphs that illustrate key findings.
- Additional Visualisation using Power BI to create interactive dashboards for deeper insights and storytelling.
- Exploratory Data Analysis (EDA) to identify patterns, trends, and anomalies in the data.
- Grouping and aggregation to summarise data by various dimensions such as product categories, customer segments, and time periods.
- Hypothesis testing to validate assumptions and draw conclusions from the data.


## Best Practices & Notes
Coding & ETL:
- Followed modular coding practices kept ETL steps (Extract → Transform → Load) clear and well-documented within Jupyter notebooks.
- Used consistent naming conventions for variables, files, and folders.
- Stored raw data in `DataSet/Raw/` and cleaned outputs in `DataSet/Cleaned/` to separate original vs processed data.
- Added inline comments and Markdown cells in Jupyter to explain each step.

Data Quality:
- Documented data cleaning decisions (handling missing values, removing duplicates, filtering invalid transactions).
- Preserved cancelled orders in a separate flag to allow for return analysis.
- Validated transformations by checking row counts, duplicates, and descriptive statistics after cleaning.

Version Control:
- Used Git & GitHub for collaboration and version tracking.
- Committed changes regularly with descriptive messages.
- Shared cleaned datasets as compressed `.zip` files to meet GitHub’s size limits.

Dashboard Design:
- Ensured clarity and interactivity: slicers for country, time, and product categories.
- Applied visual storytelling principles: KPIs at the top, trends in the middle, details at the bottom.
- Kept dashboards consistent in colour scheme and layout for readability.

Team Collaboration:
- Defined clear tasks between team members.
- Used GitHub Projects - Kanban board to track tasks, milestones, and deliverables.
- Held daily stand-ups to track progress and resolve issues and kept a constant line of communication open via Discord.

## Bugs and Fixes
- Initial issues with saving large cleaned datasets on GitHub were resolved by compressing the files into `.zip` format.
- Encountered missing values in the CustomerID column; decided to drop these rows as they were essential for customer analysis.
- Handled duplicate entries by removing exact duplicates and flagging potential return transactions for separate analysis.

## Hypothesis and how to validate?
- Hypothesis 1: Certain products are more likely to be returned than others. To validate this, we can analyse the return rates by product category and identify any patterns or trends.

- Hypothesis 2: Customers with higher RFM (Recency, Frequency, Monetary) scores are more likely to make repeat purchases. We can validate this by segmenting customers based on their RFM scores and analysing their purchase behaviour over time.
How to validate:
1. Calculated recency, frequency, and monetary value per customer.
2. Divided customers into quartiles to find RFM "Champions" (top scores).
3. Computed revenue contribution of Champions.
4. Found that Champions (customers with a score of 4), while fewer in number, contributed significantly more (over 80%) to overall revenue compared to other segments.
- Insight: prioritise retention and rewards for high-value customers.

- Hypothesis 3: Sales are seasonal, with peaks during holiday periods. We can validate this by analysing sales data over time and identifying any seasonal patterns or trends.
- Our recommendation would be to increase marketing efforts during November and December to capitalise on the holiday shopping season and increase inventory levels for popular products.

- Hypothesis 4: Customers from certain countries are more likely to make purchases than others. We can validate this by analysing sales data by country and identifying any patterns or trends represented in Data Visualisation.

- Hypothesis 5: Revenue differs by time of day. Sales peak during hours 10 - 15. We can validate this by analysing sales data by hour and identifying any patterns or trends.

- Hypothesis 6: Average order value varies by country. UK has smaller average order values but more frequently leading to higher overall revenue. We can validate this by analysing average order values by country and identifying any patterns or trends.

- Hypothesis 7: Certain customers act like resellers. As represented in the data we have gathered, 77 customers act like resellers. These customers place a high number of orders, with a low recency meaning they place orders often and should not be classes as an average customer. We can validate this by analysing customer purchase patterns and identifying any customers who exhibit reseller-like behaviour.

## Key Findings and Insights
- Sales Trends:
- Sales are seasonal, with peaks during holiday periods. This suggests that marketing efforts should be intensified during November and December.
- Weekday patterns show Tuesday–Thursday as the busiest days, while weekends are quieter.

- Geographical Insights:
- The UK is the largest market, but significant sales also come from Germany, France, and the Netherlands. This indicates potential for targeted marketing campaigns in these countries.

- Business Performance:
- We have noted in block 306 of the ETL notebook some of the more expensive costs to the business are not for items sold but for business expenses. This is something the business may want to look into further.
- Furture analysis should be done to identify the most returned products and understand the reasons behind returns to improve customer satisfaction and reduce costs. This can be views in block 301 in the ETL notebook.

- Recommended Actions:
- Customer ID 15287 Seems to be the companies own account which includes spending on business expenses. This is represented in the DataVisualisation section. We suggest the business keeps this account separate from other customer accounts to ensure accurate analysis of customer behaviour and spending patterns.

## Dashboard & Visualisations

We built interactive dashboards in Power BI featuring:

- Sales Overview
- Product Analysis
- Customer Insights
- Geographic Trends
 [Download Power BI Dashboard (.pbix)](https://drive.google.com/file/d/1y-aa6Pv6j8LqKfCZdpJPKb8Ksijl7UV0/view?usp=sharing)



## Project Review and Conclusion
This project successfully delivered on the main business requirements:  
- We improved understanding of customer behaviour by segmenting customers using RFM analysis.  
- We identified best-selling products, seasonal sales peaks, and countries with the highest sales activity.  
- We highlighted patterns in product returns and flagged areas where the business may reduce costs.  
- We built Data Visualisations and interactive Power BI dashboard to visualise these insights clearly and enable data-driven decision-making.  

Key Achievements:
- ETL Pipeline: Built a robust process to clean, transform, and prepare the dataset, ensuring data quality and consistency while also reducing file size for GitHub storage. 
- Customer Insights: Confirmed that high-value "Champion" customers contribute the majority of revenue, reinforcing the importance of retention strategies.  
- Seasonality: Identified strong seasonal patterns, with sales peaking in November and December.  
- Geography: Found that the UK dominates revenue, with Germany, France, and the Netherlands offering strong opportunities for growth.  
- Returns: Flagged certain products with higher return rates that could benefit from further investigation.  

Limitations:
- The dataset covers only one year of transactions, which limits our ability to confirm long-term seasonal patterns.  
- Product categorisation was based on descriptions, which may contain inconsistencies.  
- Customer demographics (age, gender, income) were not available, so customer segmentation relied only on transaction history.  

Recommendations for Future Work:
- Perform deeper analysis on the reasons for product returns to reduce costs and improve customer satisfaction.  
- Explore basket analysis (products frequently bought together) to identify cross-selling opportunities.  
- Extend the analysis with multiple years of data to confirm seasonal trends and detect long-term growth opportunities.  
- Build predictive models to forecast sales and identify customers at risk of churn.  
- Exclude business expenses from customer data to ensure accurate analysis of customer behaviour.

Conclusion:
This project set out to analyse online retail transaction data to uncover actionable insights that could improve profitability, reduce inefficiencies, and guide business strategy. By following a structured ETL pipeline, performing exploratory data analysis, and visualising results through interactive dashboards, we were able to address the original business requirements and extract meaningful conclusions.

The Online Retail Transactions Analysis project demonstrates the value of data driven decision-making in ecommerce. By cleaning and transforming raw transactional data into structured insights, we provided evidence that customer segmentation, seasonal marketing strategies, and return management are key levers for improving profitability. The Power BI dashboard serves as an interactive tool for stakeholders to explore sales, customers, products, and markets dynamically.

Ultimately, the project illustrates that even with limited transactional data, meaningful and actionable business strategies can be derived. With further data integration and predictive analytics, the business could evolve from reactive reporting to proactive and strategic decision making.


## Credits
- Abhishek Ranjan - Original Dataset Creator
- Code Institute Tutor Vasi & Niel for providing assistance and guidance throughout the project.   
- The use of ChatGPT to help with transforming the original dataset .csv file to a .zip file to reduce file size and helping with parts of the code.
- To the team who worked on this project for their collaboration and contributions:
- Fanxiang
- Lee
- Benjamin
- Jasneil