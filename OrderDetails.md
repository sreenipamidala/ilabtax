# Order Details Dashboard

## Workbook: Superstore

**Description:**  
The Superstore workbook is a Tableau workbook that covers various aspects of the company Superstore's operations, including sales, products, customers, regions, and categories. The workbook has pre-built dashboards which are Product, Customers, What If Forecast, and Order Details.

### Dashboard Description
The Superstore workbook is a Tableau workbook that covers various aspects of the company Superstore's operations, including sales, products, customers, regions, and categories. The workbook has pre-built dashboards which are Product, Customers, What If Forecast, and Order Details.

### Filters

1. **Order Date**
   - **Description:** Allows users to focus on order details for a specific order date.
   - **Type:** Range
   - **Default Value:** All
   - **Possible Values:** N/A
   - **Data Type:** Date
   - **Min Value:** 2020-03-01
   - **Max Value:** 2020-12-30

2. **Region**
   - **Description:** Allows users to focus on order details for a specific region.
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** ["All", "East", "West", "Central", "South"]
   - **Data Type:** String

3. **State/Province**
   - **Description:** Allows users to focus on order details for a specific state or province.
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** N/A
   - **Data Type:** String

4. **City**
   - **Description:** Allows users to focus on order details for a specific city.
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** N/A
   - **Data Type:** String

5. **Category**
   - **Description:** Allows users to focus on order details for a specific product category.
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** ["All", "Furniture", "Office Supplies"]
   - **Data Type:** String

6. **Segment**
   - **Description:** Allows users to focus on order details for a specific customer segment.
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** ["All", "Consumer", "Corporate"]
   - **Data Type:** String

### Fields

#### Product Detail Sheet

1. **Segment**
   - **Type:** ColumnField
   - **Description:** Allows users to focus on data and insights for specific customer segments. Offers four options: All, Consumer, Home Office, Corporate.
   - **Data Type:** STRING

2. **Category**
   - **Type:** ColumnField
   - **Description:** Allows users to analyze data by product category. Offers four options: All, Furniture, Office Supplies, Technology.
   - **Data Type:** STRING

3. **Profit Ratio**
   - **Type:** CalculatedField
   - **Description:** Profit Ratio, calculated as sum([Profit])/sum([Sales]), is a key financial metric used to assess the overall profitability of a business or product category.
   - **Formula:** sum([Profit])/sum([Sales])
   - **Data Type:** REAL

4. **Customer Name**
   - **Type:** ColumnField
   - **Description:** Name of the Customer
   - **Data Type:** STRING

5. **Ship Date**
   - **Type:** ColumnField
   - **Description:** Date on which an order is physically shipped from the warehouse and sent to the customer
   - **Data Type:** DATE

6. **Discount**
   - **Type:** ColumnField
   - **Description:** Discounts offered
   - **Data Type:** REAL

7. **Order ID**
   - **Type:** ColumnField
   - **Description:** ID of the order
   - **Data Type:** STRING

8. **Profit**
   - **Type:** ColumnField
   - **Description:** Profit for a specific period
   - **Data Type:** REAL

9. **Order Date**
   - **Type:** ColumnField
   - **Description:** Order date refers to the specific date and time when a customer places an order for a product
   - **Data Type:** DATETIME

10. **Region**
    - **Type:** ColumnField
    - **Description:** "Region" field categorizes entities (e.g., customers, orders, sales) into four geographic areas: Central, South, East, West
    - **Data Type:** STRING

11. **Sales**
    - **Type:** ColumnField
    - **Description:** The sales for the specific period
    - **Data Type:** INTEGER

12. **Days to Ship Scheduled**
    - **Type:** CalculatedField
    - **Description:** The scheduled number of days to ship the order
    - **Formula:** CASE [Ship Mode] WHEN "Same Day" THEN 0 WHEN "First Class" THEN 1 WHEN "Second Class" THEN 3 WHEN "Standard Class" THEN 6 END
    - **Data Type:** INTEGER

13. **Ship Mode**
    - **Type:** ColumnField
    - **Description:** Refers to the mode of shipping
    - **Data Type:** STRING

14. **Quantity**
    - **Type:** ColumnField
    - **Description:** Quantity of products shipped to the customer
    - **Data Type:** INTEGER

15. **City**
    - **Type:** ColumnField
    - **Description:** City
    - **Data Type:** STRING

16. **Days to Ship Actual**
    - **Type:** CalculatedField
    - **Description:** The actual number of days to ship the order
    - **Formula:** DATEDIFF('day', [Order Date], [Ship Date])
    - **Data Type:** INTEGER

17. **State/Province**
    - **Type:** ColumnField
    - **Description:** State/Province
    - **Data Type:** STRING
