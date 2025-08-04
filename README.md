# task-1
sales data task 1 elevate labs


This project uses a dataset named sales_data_sample.csv, which is loaded and cleaned using Pandas in Python. Below are the key data handling steps:

I read the CSV file using pandas.read_csv() and specified the full file path (for Windows systems, we use raw string format r"" to avoid backslash issues).
import pandas as pd

df = pd.read_csv('sales_data_sample.csv', encoding= 'unicode_escape')

I have used .dtypes and .info() to check each column's data type. Since the order_date column was of type object (i.e., string), we converted it to a proper datetime format:

df['Order_Date'] = pd.to_datetime(df['Order_Date'])

I have checked for duplicate rows and removed them if necessary:

df.duplicated().any()

These steps ensure the dataset is clean, consistent, and ready for analysis or visualization.
