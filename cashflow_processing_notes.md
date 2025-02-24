## Concatenate Transaction Data

GitHub has a file size limit of 25MB so the transaction data had to be chunked up.
To concatenate these files run:
```
import pandas as pd
from pathlib import Path
files = Path("transaction_data").glob("transaction_*.parquet")
transactions = pd.concat([pd.read_parquet(f) for f in files])
```
## Transaction Codes

0,0,SELF_TRANSFER
1,1,EXTERNAL_TRANSFER
2,2,DEPOSIT
3,3,PAYCHECK
4,4,MISCELLANEOUS
5,5,PAYCHECK_PLACEHOLDER
6,6,REFUND
7,7,INVESTMENT_INCOME
8,8,OTHER_BENEFITS
9,9,UNEMPLOYMENT_BENEFITS
10,10,SMALL_DOLLAR_ADVANCE
11,11,TAX
12,12,LOAN
13,13,INSURANCE
14,14,FOOD_AND_BEVERAGES
15,15,UNCATEGORIZED
16,16,GENERAL_MERCHANDISE
17,17,AUTOMOTIVE
18,18,GROCERIES
19,19,ATM_CASH
20,20,ENTERTAINMENT
21,21,TRAVEL
22,22,ESSENTIAL_SERVICES
23,23,ACCOUNT_FEES
24,24,HOME_IMPROVEMENT
25,25,OVERDRAFT
26,26,CREDIT_CARD_PAYMENT
27,27,HEALTHCARE_MEDICAL
28,28,PETS
29,29,EDUCATION
30,30,GIFTS_DONATIONS
31,31,BILLS_UTILITIES
32,32,MORTGAGE
33,33,CHILD_DEPENDENTS
34,34,RENT
35,35,BNPL
36,36,AUTO_LOAN
