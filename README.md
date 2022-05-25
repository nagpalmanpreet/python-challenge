# python-challenge

* initialize variables 
    * totalMonths - variable to hold value of total no. of months
    * totalAmount - variable to hold value of total amount of profit/loss
    * count - variable for loop iterator 
    * changeAggregator - variable to hold value of sum of changes between each month 
    * maxProfit - variable to hold value of maximum profit in a month
    * maxLoss - variable to hold value of maximum loss in a month
    * maxProfitMonth - variable to hold value for month with maximum profit
    * maxLossMonth - variable to hold value for month with maximum loss
    * changeList - List to hold differences of each month

* Set File Path to read budget_data.csv
* Loop through each row of the file
    * Increment totalMonths
    * Increment totalAmount
    * Set prevReading with value of Profit/Loss value
    * If difference between profit/loss of current month and previous month is greater than  maxProfit, set maxProfit to current value. Also set the maxProfitMonth as current month
    * If difference between profit/loss of current month and previous month is less than  maxLoss, set maxLoss to current value. Also set the maxLossMonth as current month
    * Append difference between profit/loss of current month and previous month to changeList List
* Calculate sum of all the elements of changeList array and assign it changeAggregator
* Calculate average change using changeAggregator divide by length of changeList
* Create a fString to generate below contents
    ```
    Financial Analysis
    ----------------------------
    Total Months: {totalMonths}
    Total: ${totalAmount}
    Average  Change: ${averageChange}
    Greatest Increase in Profits: {maxProfitMonth} ${maxProfit}
    Greatest Decrease in Profits: {maxLossMonth} ${maxLoss}
    ```
* Print previously created fString
* Set File Path for output file and write previously created fString to file