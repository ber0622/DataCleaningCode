# Import necessary libraries
import pandas as pd

# Load the cleaned dataset
filepath = "cleaned_data.csv"  # Adjust path if needed
eabldata = pd.read_csv(filepath)

# Display general information about the dataset
print("Dataset Information:")
print(eabldata.info())

# Display summary statistics for numerical columns
print("\nSummary Statistics:")
print(eabldata.describe())

# Display summary statistics including non-numeric columns
print("\nSummary Statistics (Including All Columns):")
print(eabldata.describe(include='all'))

# Check for missing values
print("\nMissing Values:")
print(eabldata.isnull().sum())

# Check for duplicate rows
print("\nNumber of Duplicates:", eabldata.duplicated().sum())

# Display correlation matrix
print("\nCorrelation Matrix:")
print(eabldata.corr())

# Check skewness and kurtosis of numerical features
print("\nSkewness of Features:")
print(eabldata.skew())

print("\nKurtosis of Features:")
print(eabldata.kurtosis())
