# Visualization---Credit-Card-Spend-Report---PowerBI

Analyzing customer spending for credit card company using PowerBI Desktop, DAX Queries, Power Query

Dataset : https://www.kaggle.com/datasets/thedevastator/analyzing-credit-card-spending-habits-in-india

Published PowerBI report : https://app.powerbi.com/view?r=eyJrIjoiMDZiMTM5NDgtYmQwOC00MGU5LTgxZDctYWEyZmI3YjBmNGExIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

Tools : PowerQuery, PowerBI Desktop, DAX Queries, PowerBI Service

Tasks : 
- Data cleaning
- Data Transformation
- Data Modelling 
- Data Analysis
- Visualizing the output

-> Challenges associated with the dataset and how they were tackled.

  - With the intital format of the dataset, there was only an amount (transaction) column was present.
  - Created additional Credit Points column calculated according to the card type. 
    . Silver: 0.5% of transaction
    . Gold: 1% of transaction
    . Platinum: 1.5% of transaction
    . Signature: 3% of transaction
    
   - Created addition Cashbacks column calculated according to the expense type
     . Bills: 0.1% of transaction
     . Entertainment: 0.3% of transaction
     . Food: 0.2% of transaction
     . Fuel: 0.2% of transaction
     . Grocery: 0.1% of transaction
     . Travel: 0.5% of transaction
     
   - With only the date column present, had to create another "Calender/Date" table to get a more detailed analysis. 
    . Extracted Year, Month, Month_number, Day, Day_number. 
    . Month_number column was used to identify quaters of the year
    . Day_number column was used to identify Weekend/Weekday
   
-> Used a star schema for the data model. 
  - Primary key "Date" from Dates table connected to "Date" column from CC_Transactions table.
  - Additional Measures table created to segregate measures from Calculated columns for better understanding 
  
-> DAX/ M-Query functions used : 
- M Query : IF-ELSE
- DAX Logical operators : IF, nested-IF
- DAX Aggregate fucntions : AVERAGE, MIN, MAX, MAXX, MINXX, SUMX
- DAX Text Function : Format()
- Date and Time Function : Month, Day, Year

-> Visuals : 
  - Animated bar chart to display increment of transaction over monthly period
  - Dynamic text box with values changing over selection
  - Slicers to filter data over Year, Expense_type, Card_Type, Weekday/Weekend.
  - Single Row Cards to display aggregates, total spending, total credit points awarded, total cashbacks
  - Stacked Bar chart to display cashbacks and total spending over month
  - Donut charts to display total spending by Gender, total credit points by card_type, total Cashbacks by card_type, High_ticket and General ticket items over total 
    spend. 
  - Navigator buttons to switch to KPIs page.
  - Line and clustered column chart to display total spending, cashbacks, credit points with slicers in the KPIs page. 


    
