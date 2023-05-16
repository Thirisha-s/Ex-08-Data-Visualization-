# Ex-07-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

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
Name:THIRISHA.S
Register number: 212222230160
```python
#Reading the given dataset
import pandas as pd
df=pd.read_csv("Superstore.csv",encoding='unicode_escape')
df.head()
#Data Visualization using Seaborn
import seaborn as sns
from matplotlib import pyplot as plt
#1.Line Plot
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
#2.Scatterplot
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
#3.Boxplot
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
#4.Violin Plot
sns.violinplot(x="Profit",data=df)
#5.Barplot
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
#6.Pointplot
sns.pointplot(x=df["Quantity"],y=df["Discount"])
#7.Count plot
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
#8.Histogram
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
#9.KDE Plot
sns.kdeplot(x="Profit", data = df,hue='Category')
#Data Visualization Using MatPlotlib
#1.Plot
plt.plot(df['Category'], df['Sales'])
plt.show()
#2.Heatmap
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
#3.Piechart
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()
df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
labels.append(i)
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
#4.Histogram
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
#5.Bargraph
plt.bar(df.index,df['Category'])
plt.show()
#6.Scatterplot
OUPUT
Reading the given dataset
## Data Visualization Using Seaborn: ### 1.Line Plot
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show()
#7.Boxplot
plt.boxplot(x="Sales",data=df)
plt.show()
```
# OUPUT
# Reading the given dataset
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/ef596a2e-e3d6-4617-ad28-2ed9f456d799)

# Data Visualization Using Seaborn
# 1.Line Plot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/eb9387fa-5661-46e6-a938-c937abc26206)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/89c2c0ba-e161-4a24-9ca8-438d6ed95930)
# 2.Scatterplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/d46c5478-5d8c-4f84-b49c-aed2eddb9ab4)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/634a77ee-4bb7-445e-98d3-386d679d14ca)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/24c33ba6-a544-4b4a-852f-2f25e657477d)

# 3.Boxplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/d73a2836-a2b1-4730-8b52-c70438b8ca34)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/5d230597-cc8c-4f64-81b3-c1408396b607)

# Violin Plot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/b4ea2298-7aff-4738-9928-acb1720932b9)


# 5.Barplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/538f609c-29e6-4e76-ac6c-937b5dee5868)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/b21446f4-5fc7-4b97-ae6a-d5ecbbfeba3f)

# pointplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/de2f036b-a40a-48c3-9b92-8024c139b6c4)

# Count plot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/2b91c7ee-3bb4-4aad-8b86-a50c03e9a944)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/28c8b2bb-e9d6-43b9-933e-9e45dc6ac981)

# Histogram
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/c1e9d0f0-e06d-4c88-bf9f-0c049e47e9cd)
# DE Plot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/f436f464-976e-4548-8e79-11b981e9c0dd)
# Data Visualization Using Matplotlib:
# Plot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/b4b4bba2-0cdd-4230-8dc9-2c8f7290f194)
# Heatmap
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/9ef4055e-b2b7-497e-b708-8abeb987e24b)
# Piechart
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/996d83b7-207e-4823-8784-44bb66b35f6c)
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/13eac7f3-e06f-409a-8726-9a277090bec8)
# Histogram
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/f32526d8-0061-42dd-9fb5-d67768d98dea)
# Bargraph
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/f51e26a0-5fcd-47d1-be6e-eb46fabc5c43)
# Scatterplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/a370de98-2122-49ac-82e4-39d25d161e50)
# Boxplot
![image](https://github.com/Thirisha-s/Ex-08-Data-Visualization-/assets/120380280/f2b8c93b-a22e-4d52-89cd-81f65cbcc199)
### RESULT

Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file

