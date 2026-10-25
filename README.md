# Retail Customer Segmentation Using RFM Analysis

## Overview
Customer segmentation on the Online Retail dataset (a UK-based online gift store, December 2010 to December 2011) using RFM analysis. Customers are scored on how recently, how often and how much they buy, then grouped into segments with a marketing action for each.

## What RFM means
- **Recency:** days since the customer's last purchase (lower is better)
- **Frequency:** number of distinct orders placed
- **Monetary:** total amount spent

## What I did
- Loaded 541,909 transactions and explored data quality problems
- Cleaned the data: removed rows with no CustomerID, cancelled orders (invoices starting with "C"), zero or negative quantities and prices, and duplicates
- Created a `TotalPrice` column (Quantity x UnitPrice)
- Built an RFM table for 4,338 customers using a snapshot date one day after the last purchase
- Scored each metric from 1 to 5 using quintiles
- Grouped customers into 10 segments (Champions, Loyal Customers, At Risk, Hibernating and more)
- Profiled each segment by size, average spend and share of revenue
- Visualized the segments with bar charts and a heatmap
- Wrote a marketing recommendation for each segment

## Key findings
- **Champions** are [X]% of customers but generate [Y]% of revenue
- The largest segment is **[SEGMENT NAME]** with [N] customers
- The median customer made 2 purchases and spent about 669, but the top spender spent over 280,000, so a
