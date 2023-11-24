# Combo-Offer
This project was to help the small scale Hotels for the combo price offers to increase the revenue
bo offer prediction project:

**Combo Offer Prediction Project Documentation**
# Business Problem
A store sells 4 products - Item1, Item2, Item3 and Item4. The store wants to offer combo discounts to boost sales but does not know what discounts to offer. The goal of this project is to analyze different combo discount options and determine the discounts that maximize overall profit.

**Data**
The data used is transactions data stored in a dataframe called c_selling. It contains the following key columns:

Inv Sl no: Invoice Number
ITEM1/2/3/4: Quantity sold of each item
unit_cost1/2/3/4: Unit cost of each item
margin1/2/3/4: Profit margin of each item
Billed Amount: Total billed amount for invoice
Margin: Total profit margin across all items
Analysis Approach
The key steps in the analysis approach were:

**Engineer features to identify combo purchase**s:
ITEM3_124: Only Item3 purchased
ITEM4_123: Only Item4 purchased
ITEM3_12: Item3 purchased with Item1 and/or Item2
ITEM4_12: Item4 purchased with Item1 and/or Item2
ITEM12n3: Item1/2 and Item3 purchased (without Item4)
ITEM12n4: Item1/2 and Item4 purchased (without Item3)
ITEM12n3n4: Item1/2, Item3 and Item4 purchased
Simulate discounting one item in the combo by 1 to 20 units
Calculate new bill, profit delta and total profit for each discount unit
**Store results in dictionaries and convert to dataframes:**
final_results_df1: Only Item3 discounts
final_results_df2: Only Item4 discounts
final_results_df3: Item1/2 combo with Item3 discounts
final_results_df4: Item1/2 combo with Item4 discounts
final_results_df5: Item1/2 combo with Item3 & Item4 discounts
For each dataframe, account for profit loss when discounting the 'primary' item in combo
Build regression models to estimate max profit discount level
**Key Insights**
Discounting only Item3 yields highest incremental profit. But it cannibalizes sales of Item1/2 combo.
Discounting Item1/2 combo with Item3 has maximum profit at 20% additional discount.
Discounting Item1/2 combo with Item4 has maximum profit at 14% additional discount.
**Recommendations**
Offer a discounted combo of Item1/2 with Item3 with an additional 20% off.
Also offer a discounted combo of Item1/2 with Item4 with an additional 14% off.
