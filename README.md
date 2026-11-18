# Power-Bi-Retail-Sales-Dashboard
# Executive Sales & Profitability Dashboard (Maven Fuzzy Factory)
### Project Overview -
Built a complete end to end operational dashboard to analyze 4 years of multi table retail data, tracking revenue scaling, product margin performance, and refund rates. 
### Dashboard Preview -
<img width="961" height="633" alt="image" src="https://github.com/user-attachments/assets/db92d9e6-e261-4b4d-8544-90114095816e" />

### Data Architecture & Modeling -
* Star Schema Design structured a relational model connecting a central Orders & order_items fact structure to dimension tables (Dim_Date, products, order_item_refunds).
* Cleaned complex Timestamp strings and handled data types using power query to ensure seamless time intelligence.
### Key DAX Measures Developed -
* Total Revenue = Sumx(order_items, order_items[price_usd])
* Total Profit = Sumx(order_items, order_iitems[price_usd] - order_items[cogs_usd])
* Refund Rate = DIVIDE(DiSTINCTCOUNT(order_item_refunds[order_item_id]), DISINCTCOUNT(order_items[order_item_id]))
