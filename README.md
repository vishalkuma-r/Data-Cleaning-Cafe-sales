👨‍💻 Author

Vishal Kumar
Data Analyst Aspirant | SQL | Python | Power BI

Project: Data Cleaning of Cafe Sales Dataset (Python & Pandas)

This notebook performs a complete data-cleaning workflow on a raw cafe sales dataset using Python. The goal is to remove inconsistencies, handle missing values, correct data types, and prepare the dataset for analysis and visualization.

✅ Steps Performed
1. Load Raw Dataset

Imported the CSV file dirty_cafe_sales.csv using Pandas.

Performed initial inspection using:

df.head()

df.info()

df.describe()

df.isnull().sum()

2. Identify Data Quality Issues

Missing values detected in:

Location

Transaction Date

Inconsistent and duplicate values found using:

df[column].unique() across all columns.

Incorrect data type for:

Transaction Date (initially stored as string)

3. Handle Missing Values

Replaced missing Location values with:

df['Location'] = df['Location'].replace(np.nan, 'UNKNOWN')


Filled missing Transaction Date values using forward-fill:

df['Transaction Date'] = df['Transaction Date'].ffill()

4. Fix Data Types

Converted Transaction Date column to datetime:

df['Transaction Date'] = pd.to_datetime(df['Transaction Date'])

5. Remove Noise & Verify Data

Verified cleaned dataset using:

df.info()

df.isnull().sum()

df.shape

6. Export Clean Dataset

Final cleaned file saved as:

Clean_Data1.csv

📂 Final Output

✔️ Cleaned dataset ready for analysis

✔️ No missing values in critical columns

✔️ Corrected data types

✔️ Standardized & consistent values
