# Retail Data Warehouse ETL Project

## Project Overview
This project implements an ETL process to build a data warehouse for a retail company using transaction, employee, and date data. The project uses Tableau Prep for data cleaning, aggregation, and transformation to create fact and dimension tables following a star schema structure. The final output is a consolidated Excel workbook containing multiple sheets, each representing a different table.

## Project Components

### 1. Data Sources
- **`transaction_data.xlsx`**: Contains retail transaction details such as sales transactions, customer purchases, product details, and store information.
- **`employee_data.xlsx`**: Includes employee details such as employee IDs, names, departments, and their respective managers.
- **`Date_HR.csv`**: Contains date details from the HR department including calendar year, month, and day.
- **`Date_Finance.xlsx`**: Contains fiscal year details including fiscal quarters and fiscal year mappings.

### 2. ETL Process
The ETL process involves **Extracting**, **Transforming**, and **Loading** data using Tableau Prep:

- **Extract**: Load data from the four different data sources.
- **Transform**: 
  - Clean, aggregate, and merge the datasets using Tableau Prep.
  - Create the following tables:
    - **`Date_Dimension`**: Merged HR and Finance date details.
    - **`Employee_Dimension`**: Contains unique employee information, including department and manager details.
    - **`Customer_Dimension`**: Extracted unique customer information from the transaction data.
    - **`Product_Dimension`**: Extracted unique product details including product name and category.
    - **`Store_Dimension`**: Extracted unique store details.
    - **`Transaction_Fact`**: Combines transaction details with references to date, employee, customer, product, and store dimensions.
- **Load**: The final output is stored in a single Excel workbook (`Retail_DataWarehouse.xlsx`) containing separate worksheets for each table.

### 3. Final Output
The final output is an Excel file named **`Retail_DataWarehouse.xlsx`**, which includes the following worksheets:

- `Date_Dimension`
- `Employee_Dimension`
- `Customer_Dimension`
- `Product_Dimension`
- `Store_Dimension`
- `Transaction_Fact`
