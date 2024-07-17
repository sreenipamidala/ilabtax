# Product Dashboard

## Workbook: Superstore

**Description:**  
The Superstore workbook is a Tableau workbook that covers various aspects of the company Superstore's operations, including sales, products, customers, regions, and categories. The workbook has pre-built dashboards which are Product, Customers, What If Forecast, and Order Details.

### Dashboard Description
The Superstore workbook is a Tableau workbook that covers various aspects of the company Superstore's operations, including sales, products, customers, regions, and categories. The workbook has pre-built dashboards which are Product, Customers, What If Forecast, and Order Details.

### Filters

1. **Region**
   - **Description:** Used for comparing Sales and Profit across Regions
   - **Type:** Non-range
   - **Default Value:** All
   - **Possible Values:** ["All", "East", "West", "Central", "South"]
   - **Data Type:** String

### Fields

#### ProductView

1. **Category**
   - **Type:** ColumnField
   - **Description:** Allows users to analyze data by product category. Offers four options: All, Furniture, Office Supplies, Technology.
   - **Data Type:** STRING

2. **Profit**
   - **Type:** ColumnField
   - **Description:** Profit for a specific period
   - **Data Type:** REAL

3. **Order Date**
   - **Type:** ColumnField
   - **Description:** Order date refers to the specific date and time when a customer places an order for a product
   - **Data Type:** DATETIME

4. **Region**
   - **Type:** ColumnField
   - **Description:** "Region" field categorizes entities (e.g., customers, orders, sales) into four geographic areas: Central, South, East, West
   - **Data Type:** STRING

5. **Sales**
   - **Type:** ColumnField
   - **Description:** The sales for the specific period
   - **Data Type:** INTEGER

#### ProductDetails

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

4. **Profit**
   - **Type:** ColumnField
   - **Description:** Profit for a specific period
   - **Data Type:** REAL

5. **Product Name**
   - **Type:** ColumnField
   - **Description:** Name of the product
   - **Data Type:** STRING

6. **Order Date**
   - **Type:** ColumnField
   - **Description:** Order date refers to the specific date and time when a customer places an order for a product
   - **Data Type:** DATETIME

7. **Region**
   - **Type:** ColumnField
   - **Description:** "Region" field categorizes entities (e.g., customers, orders, sales) into four geographic areas: Central, South, East, West
   - **Data Type:** STRING

8. **Sub-Category**
   - **Type:** ColumnField
   - **Description:** It is a sub-section of the Product Category with values like Accessories, Bookcases, Chairs, Tables, etc.
   - **Data Type:** STRING

9. **Sales**
   - **Type:** ColumnField
   - **Description:** The sales for the specific period
   - **Data Type:** INTEGER
