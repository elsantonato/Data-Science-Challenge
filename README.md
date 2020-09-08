# Data-Science-Challenge

## Question 1:

 Given some sample data, write a program to answer the following: 
 
 On Shopify, we have exactly 100 sneaker shops, and each of these shops sells only one model of shoe. We want to do some analysis of the average order value (AOV). When we look at orders data over a 30 day window, we naively calculate an AOV of $3145.13. Given that we know these shops are selling sneakers, a relatively affordable item, something seems wrong with our analysis. 

1. Think about what could be going wrong with our calculation. Think about a better way to evaluate this data.
2. What metric would you report for this dataset?
3. What is its value?

## Answers: 

1. The incorrect AOV calculation of $3145.13 was most likely arrived at by mistakenly calculating the total_items with the count() function instead of sum(). Whereas count() will only provide the total count of the number of rows, sum() will more accurately provide the AOV value by adding together all of the values in the total_items column. 

2. To determine the correct Average Order Value (AOV), the reporting metrics are the respective sums of both 'order_amount' and 'total_items':<br/>

   oa_sum = data_df['order_amount'].sum()\
   ti_sum = data_df['total_items'].sum()

   Next divide the total order amount (oa_sum) by the total items amount (ti_sum):\
   AOV = oa_sum/ti_sum

3. The Average Order Value (AOV) is: $357.92 
