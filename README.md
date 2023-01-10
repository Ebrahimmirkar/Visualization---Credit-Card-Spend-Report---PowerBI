# Visualization---Credit-Card-Spend-Report---PowerBI

Analyzing customer spending for credit card company using PowerBI Desktop, DAX Queries, Power Query

Dataset : https://www.kaggle.com/datasets/thedevastator/analyzing-credit-card-spending-habits-in-india

Published PowerBI report : https://app.powerbi.com/view?r=eyJrIjoiOGNmMWZiOTItNDdiOS00ZTk4LWI1ZmUtYjIyODg4Y2EyYmNjIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

Tasks : 
- Data cleaning
- Data Transformation
- Data Modelling 
- Data Analysis
- Visualizing the output

- Challenges associated with the dataset and how to tackled it.
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
   
   - Created a High Ticket column to identify transactions that were significantly larger compared to rest.
     . A transaction was high-ticket when the amount was greater than AVERAGE of all transactions
    
