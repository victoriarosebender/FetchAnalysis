Hello Lydia,

I have since review the data order files. 

A couple of validation notes:

The transaction file gave us transactions that took place between 6/12/24 - 9/8/24.

Continuing with the transaction file, there were 12,500 lines that had zero for final quantity.
These were excluded as it is assumed that items will be either purchased or returned with each transaction.
The sum of sales for these zero lines was $57,372.67 (33.4% of total). This is excluded from the analysis results.

After the above exclusion, there were 4,338 lines that had no barcode these account for $14,010.56 in sales (12.3% of total sales) and 4,672.79 quantity (11.5% of qty) and will be excluded.
There were 5 lines that had -1 barcode these account for $9.71 (<0.01% of total sales) in sales and 5 quantity and will be excluded.

After all of these exclusions, there were 11,156 transactions (~34% of the new total transactions) where final sale was blank. 
I assumed these were freebees given out to generate more business. 
I also assumed any final quantity with a decimal value was a valid transaction. 
Lastly, I removed any duplicate rows.

*When combining the User data with the Transaction file, 99.5% of users in the transaction file do not have corresponding user data.
When combining the Product data with the Transaction file, 97.5% of barcodes in the transaction file do not have corresponding product data.*


Moving on to the analysis:

**What are the top 5 brands by receipts scanned among users 21 and over?**
The answer is invalid due to missing data. Below is the result I was able to pull based on the limited data and queryF can be reran once the data is complete.
DEAN'S DAIRY DIP with 1 unique receipt attached to it.


**Who are Fetch’s power users?**
99.5% of users in the transaction file are not in the users file. This will need to be resolved.
In the meantime, I have supplied the top 5 users based on total sales
| User IDs                        | Total Qty | Total Sales |
|--------------------------------|-----------|-------------|
| 65e4bc2716cc391732143569       | 9         | $88.37       |
| 60a5363facc00d347abadc8e       | 44        | $84.58       |
| 6183300cf998e47aad2d6f5d       | 11.1      | $82.28       |
| 6475fd16a55bb77a0e279ee0       | 4         | $77.80       |
| 643059f0838dd2651fb27f50       | 4         | $75.99       |

**Which is the leading brand in the Dips & Salsa category?**
This answer is invalid due to missing data. Below is the result I was able to pull based on the limited data and queryD can be reran once the data is complete.
This assumes within the Dips & Salsa category the brand with the highest sales is the leading brand.
DEAN'S DAIRY DIP is the leading Brand in the Dips & Salsa category coming in with 22 units in sales and $39.95 in sales.


**Additional Insights**

![SalesOverTime](SalesOverTime.png)
This shows us total daily sales with rolling weekly average to help us better see the trends. The average daily sales ranged from $800 - $1,400 between mid June and early September.

![DayofWeek](DayofWeek.png)
This shows average sales by day of week. An insight we can draw from this is that on average weekend sales are 15% higher than weekday sales.


This concludes my insights for the time being. Once we have the completed user data and product data, we can conduct a deeper analysis. 
Please do not hesitate to reach out if you'd like any assistance working with the client. I would be happy to supply them a list of those missing barcodes and user ids.


Best,

Victoria Bender