# acing-DS-Questions-Interview
This will aid you prepare for an interview

# Pandas
import pandas as pd

# Read a CSV file into a Pandas DataFrame
df = pd.read_csv('data.csv')

# Select a column from a DataFrame
column = df['column_name']

# Filter a DataFrame based on a condition
filtered_df = df[df['column_name'] > 10]

# Group a DataFrame by a column and calculate the mean of another column
grouped_df = df.groupby('column_name')['other_column'].mean()

# Data Analysis
import pandas as pd

# Read a CSV file into a Pandas DataFrame
df = pd.read_csv('data.csv')

# Drop rows with missing values
df = df.dropna()

# Remove duplicate rows
df = df.drop_duplicates()

# Remove outliers based on a condition
df = df[df['column_name'] < 10]

# Data Transformation
import pandas as pd

# Read a CSV file into a Pandas DataFrame
df = pd.read_csv('data.csv')

# Convert a column to a different data type
df['column_name'] = df['column_name'].astype(float)

# Scale a column to have a mean of 0 and a standard deviation of 1
df['column_name'] = (df['column_name'] - df['column_name'].mean()) / df['column_name'].std()

# Apply a mathematical function to a column
df['column_name'] = df['column_name'].apply(lambda x: x**2)


# Matplotlib
import matplotlib.pyplot as plt

# Create a bar plot
x = [1, 2, 3, 4, 5]
y = [10, 5, 15, 20, 8]
plt.bar(x, y)

# Create a scatter plot
x = [1, 2, 3, 4, 5]
y = [10, 5, 15, 20, 8]
plt.scatter(x, y)

# Create a line plot
x = [1, 2, 3, 4, 5]
y = [10, 5, 15, 20, 8]
plt.plot(x, y)

import pandas as pd
import sqlite3

# Connect to a SQLite database
conn = sqlite3.connect('database.db')

# Execute a SQL query and return the results as a Pandas DataFrame
df = pd.read_sql_query('SELECT * FROM table_name', conn)

# PDF
import PyPDF2

# Open a PDF file in read-binary mode
with open('data.pdf', 'rb') as pdf_file:
    # Create a PDF reader object
    pdf_reader = PyPDF2.PdfFileReader(pdf_file)

    # Get the number of pages in the PDF document
    num_pages = pdf_reader.getNumPages()

    # Extract the text from each page and store it in a list
    text_list = []
    for page_num in range(num_pages):
        page_obj = pdf_reader.getPage(page_num)
        text = page_obj.extractText()
        text_list.append(text)
