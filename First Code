#importing libraries
import pandas as pd
import numpy as np
import sklearn as sc

#import data
filepath = "C://Users//ADMIN//OneDrive//Desktop//HistoricalPrices data.csv"
eabldata = pd.read_csv(filepath)

##inspecting the data
#check on data
eabldata.info()

#summary of statistics
eabldata.describe()

#preview first and last rows
eabldata.head(5)
eabldata.tail(5)

#Handling missing values
eabldata.isnull().sum()


#Remove duplicates if any
eabldata.drop_duplicates(inplace=TRUE_)

#Remove leading spaces from column names
eabldata.columns=eabl.columns.str.strip()

#Fix Data Types
#Covert "date" column to date time format
eabldata["date"]=pd.to_datetime(eabldata["date"],format="%m/%d/%y")

#Set data by ascending order
eabldata=eabldata.sort_values(by="date").reset_index(drop=TRUE)


#Handling outliers
Q1 = eabldata['column_name'].quantile(0.25)
Q3 = eabldata['column_name'].quantile(0.75)
IQR = Q3 - Q1
df = eabldata[(eabldata['column_name'] >= Q1 - 1.5 * IQR) & (eabldata['column_name'] <= Q3 + 1.5 * IQR)]


#Use z-score to detect extreme outliers #Removes values beyond 3 standard deviations
eabldata= eabldata[(np.abs(stats.zscore(eabldata['column_name'])) < 3)]  

#Normalize and standardize data

scaler = MinMaxScaler()  # Scales values between 0 and 1
eabldata[['column_name']] = scaler.fit_transform(df[['column_name']])

scaler = StandardScaler()  # Standardizes to mean=0, std=1
eabldata[['column_name']] = scaler.fit_transform(df[['column_name']])

#Save the cleaned data
eabldata.to_csv('cleaned_data.csv', index=False)
