NAME:JANSI RANI A A
REG NO: 212224040130
# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

```
import pandas as pd
df=pd.read_csv("C:\\Users\\admin\\Downloads\\Data_set.csv")
df
```
<img width="772" height="462" alt="Screenshot (1021)" src="https://github.com/user-attachments/assets/514bb27c-7414-4aeb-8615-ae0c791d90a3" />

```
df.head(6)
```
<img width="947" height="285" alt="Screenshot (1022)" src="https://github.com/user-attachments/assets/5a9193bf-d4ba-462f-aa36-2bd8b0e89af2" />

```
df.tail(6)
```
<img width="944" height="292" alt="Screenshot (1023)" src="https://github.com/user-attachments/assets/451994fd-fa66-47de-8f0b-26fbf317f030" />

```
df.isnull()
```
<img width="874" height="346" alt="Screenshot (1024)" src="https://github.com/user-attachments/assets/daf16141-f3c6-443c-b241-594d4ff3a422" />

```
df.notnull()
```
<img width="824" height="358" alt="Screenshot (1025)" src="https://github.com/user-attachments/assets/06915316-9876-4aa3-a027-915a703d1223" />

```
df.isnull().sum()
```
<img width="795" height="315" alt="Screenshot (1026)" src="https://github.com/user-attachments/assets/a81f1d29-c986-457b-9817-4ed4070136d0" />

```
df.describe()
```
<img width="664" height="269" alt="Screenshot (1027)" src="https://github.com/user-attachments/assets/8ed796fc-bfd5-4167-8c73-2db87f63a9a8" />

```
df.iloc[1:6,:7]
```
<img width="792" height="183" alt="Screenshot (1028)" src="https://github.com/user-attachments/assets/920e2524-fac4-445a-b9d3-e03cfc04a823" />
```
df.info()
```
<img width="665" height="264" alt="Screenshot (1029)" src="https://github.com/user-attachments/assets/08594bcd-6584-41ad-8043-6f1572a8c285" />
```
df[df['num_episodes']>20]
```
<img width="991" height="535" alt="Screenshot (1030)" src="https://github.com/user-attachments/assets/1cf51c3b-400e-44dc-957b-12d4fae29840" />
```
df['country'].value_counts()
```
<img width="665" height="228" alt="Screenshot (1031)" src="https://github.com/user-attachments/assets/3b54cc21-dd8d-439c-a00c-18c4133785dd" />
```
df.dropna(axis=0)
```
<img width="934" height="470" alt="Screenshot (1032)" src="https://github.com/user-attachments/assets/da570b59-9c97-445b-a6ce-7a92d561931a" />
```
df.fillna(0)
```
<img width="940" height="469" alt="Screenshot (1033)" src="https://github.com/user-attachments/assets/f18f95c3-b14e-4cb8-9120-7a357e8c569b" />
```
df.fillna(method='ffill')#forward fill
```
<img width="940" height="433" alt="Screenshot (1034)" src="https://github.com/user-attachments/assets/3dfa0ce3-d483-452f-8a5e-13dd709c1269" />
```
df.fillna(method='bfill')#back fill
```
<img width="924" height="440" alt="Screenshot (1035)" src="https://github.com/user-attachments/assets/117a8392-41e8-407f-bb40-0c07b773d787" />
```
df.interpolate()
```
<img width="935" height="447" alt="Screenshot (1036)" src="https://github.com/user-attachments/assets/5c73190f-a799-45bc-9baf-27c64a58873e

# Result
         
**Result:**

The given dataset was successfully cleaned by handling missing values, removing duplicates, and eliminating outliers using IQR and Z-score methods. The cleaned data was then saved to a file for further analysis.
