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



## Key Findings and Insights
- Sales Trends:
- Sales are seasonal, with peaks during holiday periods. This suggests that marketing efforts should be intensified during November and December.
- Weekday patterns show Tuesday–Thursday as the busiest days, while weekends are quieter.

- Geographical Insights:
- The UK is the largest market, but significant sales also come from Germany, France, and the Netherlands. This indicates potential for targeted marketing campaigns in these countries.

- Business Performance:
- We have noted in block 306 of the ETL notebook some of the more expensive costs to the business are not for items sold but for business expenses. This is something the business may want to look into further.
- Furture analysis should be done to identify the most returned products and understand the reasons behind returns to improve customer satisfaction and reduce costs. This can be views in block 301 in the ETL notebook.

## Project Review and Conclusion

## Credits
- Abhishek Ranjan - Original Dataset Creator
- Code Institute Tutor Vasi for providing assistance and guidance throughout the project.   
- The use of ChatGPT to help with transforming the original dataset .csv file to a .zip file to reduce file size.
- To the team who worked on this project for their collaboration and contributions:
- Fanxiang
- Lee
- Benjamin
- Jasneil