1. ANALYZING THE TYPE CODE
- Assuming the data in the dataset belongs to current accounts, based on the transaction types, there will be 3 types of transactions greater than 5 smaller than 0 (because Internal transfer can record both positive and negative transactions). However, according to the data set, there are 5 positive types and 3 negative types. So, this assumption is incorrect. If it were only savings accounts, it would also be incorrect because there are all 7 types, and typically no one uses a savings account to top up a phone number. So, the remaining case is that this dataset contains information about both current accounts and savings accounts. 
- Type code 1 has both positive and negative transactions, so this type will be Internal Transfer. Among the type codes with negative amount, the phone top-up has the smallest and most reasonable average value when assigned to the average and maximum of this type (average is 27000 and max is 550000). The only remaining negative type code and 5 positive type codes. 
- Since the type code with negative values has a relatively large average value, it is likely not a Gift Payment. Here, only the positive values remain, and since Gift Payment is likely to have the recipient as a SuperBank customer, the condition of this dataset may only select the recipient as a SuperBank customer. 
- Among the type codes with positive values, type code 6 has the lowest and most reasonable average value if it is a gift payment because the other types are all savings deposits (rarely does a savings deposit appear as low). So, Type Code 6 is Gift Payment. 
- Only one type code remains, consisting entirely of negative values, which is likely Interbank Transfer. So, type code 2 is Interbank Transfer. 
- The remaining 3 type codes with positive values, I have not found enough evidence to differentiate them, so I will put them into a common category for analysis on savings (of these 3 types, 1 are savings accounts, and 2 is a current account).
2. ANALYSIS OF THE NUMBER OF TRANSACTIONS OCCURRING PER MINUTE
- I'll take a quick moment to analyze the number of transactions per minute to see if there's a need to alert for system load awareness.
- The number of transactions occurring per minute is relatively low according to the data, with the highest being only 14 transactions per minute. On average, there are only 1.5 transactions per minute. This figure is unlikely to have any impact on the system's capacity, as banking systems can handle thousands of transactions per minute.
3. ANALYZING CUSTOMER BEHAVIOR
Based on the charts and data in the Jupyter file, several observations can be made:
- The majority of customers at SuperBank are typically in the 18-40 age group. Specifically, the younger demographic aged 18-25 holds a significant share, particularly noticeable in February (during holidays and festivals), where they often use the services for gifting or mobile top-ups.
- A substantial number of young individuals participate in savings, with the average rate per customer comparable to that of middle-aged groups. This indicates that today's youth are also interested in accumulating cash assets.
Despite representing a large portion of SuperBank's account holders, the usage of services per customer does not significantly outstrip other age groups across all products. The 18-25 age group shows a strong average transaction count per user, particularly in transfer transactions, while in savings and other utility applications, it may be equal to or slightly higher than older age groups. SuperBank may need to optimize the transfer section to better cater to the older generation.
- Additionally, there is a significant difference in the average transaction value between the under-40 and over-40 age groups. This indicates variations in service usage behavior among different age groups: Using services frequently does not necessarily equate to higher spending, while infrequent usage does not imply lower spending. Therefore, SuperBank could leverage this insight to develop customer segmentation strategies based on objectives: focusing on quantity or quality of customers?


