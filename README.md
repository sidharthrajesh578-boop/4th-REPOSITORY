Project Overview
This assignment focuses on using Microsoft Power BI to clean, transform, analyze, model, and summarize sales data. The project uses three datasets: List of Orders, Order Details, and Sales Target.
1. Data Import
The following datasets were imported into Power BI:
- List of Orders
- Order Details
- Sales Target
These datasets were loaded into Power Query Editor for data preparation and transformation.
2. Data Transformation and Cleaning
List of Orders
- Retained the required 500 records.
- Verified Order Date as a Date data type.
- Formatted CustomerName using Capitalize Each Word.
- Combined City and State into a single LOCATION column.
- Checked the dataset for missing and error values.
Order Details
- Changed Amount to Fixed Decimal Number.
- Created a Profit Margin column using:
Profit Margin = Profit / Amount
- Converted Profit Margin to Percentage format.
- Created a Profit Status column:
  - Profit < 0 → LOSS
  - Profit = 0 → BREAK-EVEN
  - Profit > 0 → PROFIT
Sales Target
- Changed Target to an appropriate numeric/currency data type.
- Verified Month of Order Date as a Date field.
- Checked the data for missing and error values.
3. Data Integration
The List of Orders and Order Details tables were merged using Order ID as the common column.
A new table named Orders Data was created using a Left Outer Join. Relevant columns from Order Details were expanded into the merged table.
The data was also:
- Sorted by Order Date in descending order.
- Filtered using the LOCATION field for Tamil Nadu during analysis.
- Checked for duplicate records.
4. Grouping and Aggregation
Several summary tables were created using duplicated tables and the Group By feature.
Order Details Summary
Calculated the count of each Order ID.
Category Profit Summary
Calculated the Average Profit by Category.
Subcategory Amount Summary
Calculated the Total Amount by Sub-Category.
Monthly Target Summary
Calculated the Total Target Amount by Month of Order Date.
5. Data Modeling
Relationships were established between the datasets:
Relationship 1
List of Orders → Order Details
- Common column: Order ID
- Relationship: One-to-Many (1:*)
- Status: Active
Relationship 2
Order Details → Sales Target
- Common column: Category
- Relationship: Many-to-Many (:)
- Status: Active
The relationships were verified through Manage Relationships in Power BI.
6. Final Outcome
The completed Power BI project demonstrates the ability to:
- Import and prepare datasets
- Clean and transform data
- Create calculated columns
- Merge tables using common keys
- Identify and handle data quality issues
- Sort and filter data
- Group and aggregate data
- Create summary tables
- Establish relationships between tables
- Build a structured data model for further analysis
