# Data Analyst|Data Engineer

## Education
**Master of Data Science**
*The University of Adelaide* 

**Bachelor of Computer Science**
*Savitribai Phule Pune University*

## Projects

# Sales analysis of Hardware chain

### Dashboard Link : 
## Problem Statement

The organisation's OLAP lacks generating valuable insights and reports which is easy ti read for business people such as Area managers and State managers. The organisation relys on Excel files generated by OLAP for insights to Area managers, where individual man hours is put into understanding and generating insights.

Since, number of neutral/dissatisfied customers (almost 57 %) are more than satisfied customers (around 43 %), thus in all they must work on improving their services. 

Also since average delay in arrival & departure both is 15 minutes, thus they must try to reduce it.


### Steps followed 

- Step 1 : Data was in the form of .sql file obtained from the on-premise RDBMS of the organisation containing 5 tables and 1000 rows.
- Step 2 : Performed initial analysis of data on MySql Workbench using Aggregate functions like COUNT, SUM.
- Step 3 : Identified and created the STAR schema of the database, here Transactions table is our fact table and main analysi is done on this table and the rest of the tables are reference tables.
  
![Star schema](https://github.com/user-attachments/assets/096d47ed-9f97-4085-a61d-7285bae133ef)
- Step 4 : Importing the .sql file into Power BI
- Step 5 : Identified basic problems with the data such as different currencies, unwanted values such as -1 and 0 in the sales_amount.
- Step 6 : Filtered out the unwanted values as they were less than 2 percent of the entire data hence wouldn't cause significant distortion in real analysis.
- Step 7 : Created a new conditional column called'Normalized sales amount' by filtering out the different currency i.e. USD and cross checking with the it's INR value for the date that the transaction occured and thus converting the value to INR.
![normalised](https://github.com/user-attachments/assets/018bf938-9e25-4353-92d6-b3bc844ab58e)

- Step 8 : Created base measures of sales quantity, sales amount and assigned them appropriate visualization.
- Step 9 : Created number cards for base measures.
![sales quant](https://github.com/user-attachments/assets/ca20c845-01c5-4dd1-9719-aad9414a000a)
- Step 10 : Using the combination of Base measure, created cards for revenue in area, sales in area.
  
![revenue market](https://github.com/user-attachments/assets/3b03ff9d-be42-46c1-80c4-2cec2c1f1dd2)
![sales area](https://github.com/user-attachments/assets/dad07755-0135-40d7-9819-655604afff19)
- Step 10 : Bar charts were made for top 5 customers and top 5 products sold.
![5customers](https://github.com/user-attachments/assets/685a8823-0ee2-4096-80d6-992ccc045180)
![top5 products](https://github.com/user-attachments/assets/4868079b-ca6f-4b0a-baff-c86557c13507)
- Step 11 : A line chart was added for revenue against the date and time spanning for the entire available range from 2018 to 2020.

As you can see the top 1st product is blank that is because the dataset that was provided had errors, this must be accurately resolved by contacting the data administrator team.

## Entire dashboard

![dash](https://github.com/user-attachments/assets/ab2d7f2c-a3a4-4cab-82fd-6ea8ab4409b3)

# Insights

A single page report was created on Power BI Desktop and uploaded the pbx file to github.

Following inferences can be drawn from the dashboard;

### [1] Total revenue for the entire period = INR 984.41M 

   The Top 1 customer Electric sara stores bring in revenue worth INR 413.33M

   The top 1 product generates revenue worth INR 468.96M

This gives a clear understanding about the nationwide statistics, marketing and statistics team could draw there insights by analysing various fields such as area wise sales, product distribution etc.
### [2] Year wise sales
The inital year of 2017 had the lowest sales revenue which increased drastically in the 2018.
There was again a dip in revenue in 2019 but it was not much but it continued going down in 2020, the decline can be observed from the months of march to June. 
