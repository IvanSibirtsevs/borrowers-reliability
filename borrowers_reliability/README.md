## Borrower reliability study

The customer is the credit department of the bank. It is necessary to find out whether the marital status and the number of children of the client affect the fact of repaying the loan on time. Input data from the bank - statistics on the solvency of customers.

The results of the study will be taken into account when building a **credit scoring** model - a special system that evaluates the ability of a potential borrower to repay a loan to a bank.


### Step 1. Open the data file and examine the general information.

### Conclusion

***Data type specified incorrectly in columns 'education_id', 'family_status_id', 'debt'***
- Different register in the education column
- Negative values in days_employed column
- Lemmas in the values in the purpose column***

### Step 2. Data preprocessing

### Pass processing

### Conclusion

***Missing values were found in columns 'total_income' and 'days_employed'***
- Perhaps people did not indicate their income and hours of work, although some of them wrote that they are currently working.
- There were negative values in the 'days_employed' column. Perhaps this error appeared when unloading data
- Gaps I filled in the first column using the median. Since the values differed greatly
- In the second using the average.

### Replacing the data type

### Conclusion

*** I chose the astype method because it fits best in this case. There is 1 more method to_numeric(),
but it converts strings to float.***

### Handling duplicates

### Conclusion

**There were not many duplicates in the table, but there were words with different case, and a few outliers.**
- Used the drop_duplicates() method
- Perhaps duplicates appeared due to a software error.

### Lemmatization

### Conclusion

*** Of all the categories, I have identified 4 main ones (real estate, housing, car, education, wedding) ***

### Data categorization

Relationship between income level and loan repayment on time
### Conclusion
***I have highlighted the main categories that I needed in the following paragraphs***

### Step 3: Answer the questions
The relationship between having children and repaying a loan on time
### Conclusion
***There is. Families without children repay loans better, while families with many children repay debts worse. I think this is due to the fact that a child takes a lot of time and money. It turns out that someone who spends, but does not earn, appears in the family. Also, parents cannot earn the same as without children, because they need to be educated.***
- Relationship between marital status and loan repayment on time
### Conclusion
*** Those who are not married and not married, as well as in a civil marriage, are most often young, and they do not understand how loans work in general, since there is no financial literacy, or it is at a minimum level, therefore they return loans less often than anyone. It turns out the category of married / married and divorced is mostly middle-aged people and they are more responsible. In the widower / widow category, the most common are the elderly, they almost always give money away.***
### Conclusion
***The rich return the loan less often than the poor and even the poor. Perhaps because entrepreneurs earn a lot of money, and a business loan is usually quite large and it is almost impossible to repay it if the business goes bankrupt. The poor most often simply do not have money to return, but the poor are mostly pensioners. They are more responsible. The middle class earns enough to return the money to the bank and most often they have a stable job.***
- How different purposes of the loan affect its repayment on time
### Conclusion
***A car loan is the least likely to be returned because this asset quickly loses its value and requires quite a large investment, and many do not think about it when buying. With education, it seems to me that people most often find it difficult to work and study. For a wedding, money is most often given and the family can pay off the loan together, it's not much easier than doing it alone, and real estate is the thing for which if you don't pay, they'll just be kicked out, so people try to find money anywhere to pay off the mortgage ***

### Step 4. General conclusion
On average, customers are about equally likely not to return money.
The level of income affects this the most. Another important feature is the purpose of the loan, marital status and the number of children.
Families without children repay loans better, while families with many children repay debts worse. Those who are not married and not married, as well as in a civil marriage, most often do not give loans, but a widower / widow most often gives money. The rich return loans less often than the poor and even the poor. The middle class earns enough to pay back the bank and usually they have stable jobs, so they are the most reliable borrowers in this category. And the riskiest category of credit is a car and education, but the most protected is real estate.
Portrait of the most reliable borrower - He has no children, is a widower, with earnings from 195759.75 to 2265604 and trying to get a loan for real estate.
Portrait of the most risky borrower - He has 4 children, is not married or in a civil marriage, and with an income of 2265604 and he is trying to take a credit
