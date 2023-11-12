# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
## Developed by: VASUNDRA SRI R
## Register number:212222230168
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()
```
## Which day of the week has the highest total bill amount?
sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")

## What is the average tip amount given by smokers and non-smokers?
sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")

## How does the tip percentage vary based on the size of the dining party?
sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")

## Which gender tends to leave higher tips?
sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")

## Is there any relationship between the total bill amount and the day of the week?
plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()

## How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?
sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")

## Which dining party size group tends to have the highest average total bill amount?
sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")

## What is the distribution of tip amounts for each day of the week?
sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")

## How does the tip amount vary based on the type of service (lunch vs. dinner)?
sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")

## Is there any correlation between the total bill amount and the tip amount?
sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)

## Heatmap
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)

# OUTPUT
## initial dataset:
![9 0](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/ebf0435b-6d15-43ea-8434-c38c16a73abe)

## tips.head()
![9 1](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/b15b0080-8a74-4d36-a5b4-69b290e46a98)

## tips.head()
![9 3](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/daf1b0b2-54ec-4c13-9752-f7c91132719d)

## Barplot
![9 4](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/86bf8cd5-758b-4ff2-84d7-ff627e83dd82)
![9 5](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/8c2a5cd6-999e-4684-82f2-556082b8023e)

## Boxplot
![9 6](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/951091ba-5dc8-43cf-a629-78f4a652bf15)
![9 7](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/2e46aab1-1f5b-48df-b887-5afae22918d5)

## Plot:
![9 8](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/bbe7d988-ffa8-4b27-87eb-a34a126387f9)

## Violinplot:
![9 9](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/733c339a-fd35-4266-b978-841a56ec0a1b)

## Barplot:
![9 10](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/8a28abee-2d3a-4a35-abe2-9ed1b7bee576)

## Boxplot:
![9 11](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/c910ed67-1361-415a-a65b-9e19164771c8)

## Violinplot:
![9 12](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/4b44726f-94b9-4042-9f71-ca1f14e4a7ae)

## Scatterplot:
![9 13](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/4172464c-12b5-47d3-8006-c1e4e537cef8)

## Heatmap:
![9 14](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex-09/assets/119393983/925935a5-5e05-4b32-9855-2bc221e7c84a)

# Result:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file
