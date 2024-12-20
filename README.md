# Data Analyst | Data Engineer

## Table of contents
1. [Certifications](#certs)
2. [Projects](#pro)
    1. [Power BI sales project](#power)
    2. [Azure data migration Project](https://github.com/rp192/dataengineer_portfolio/blob/master/dataengineer_project.md)
3. [University Projects](#uni)
    1. [Household energy prediction](#python)
    2. [Spotify genre prediction](#R)

## Certifications <a name="certs"></a>

### Microsoft Certified: Azure Data Fundamentals(DP-900)
![DP900](https://github.com/user-attachments/assets/df270aa0-6eb9-4d36-8351-e36fa529a415)

### Academy Accreditation - Databricks Lakehouse Fundamentals
![lakehouse fundamentals](https://github.com/user-attachments/assets/f9e8467f-656d-4ca1-80f0-3d3fcad21f73)

## Projects <a name="pro"></a>

### Sales analysis of Hardware chain <a name="power"></a>

#### Dashboard Link : https://github.com/rp192/PowerBI_projects
#### Problem Statement

The organisation's OLAP lacks generating valuable insights and reports which is easy ti read for business people such as Area managers and State managers. The organisation relys on Excel files generated by OLAP for insights to Area managers, where individual man hours is put into understanding and generating insights.

#### Steps followed 

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

#### Entire dashboard

![dash](https://github.com/user-attachments/assets/ab2d7f2c-a3a4-4cab-82fd-6ea8ab4409b3)

#### Insights

A single page report was created on Power BI Desktop and uploaded the pbx file to github.

Following inferences can be drawn from the dashboard;

#### [1] Total revenue for the entire period = INR 984.41M 

   The Top 1 customer Electric sara stores bring in revenue worth INR 413.33M

   The top 1 product generates revenue worth INR 468.96M

This gives a clear understanding about the nationwide statistics, marketing and statistics team could draw there insights by analysing various fields such as area wise sales, product distribution etc.
#### [2] Year wise sales
The inital year of 2017 had the lowest sales revenue which increased drastically in the 2018.
There was again a dip in revenue in 2019 but it was not much but it continued going down in 2020, the decline can be observed from the months of march to June.

## University projects <a name="uni"></a>
### Predicting future energy use of a household <a name="python"></a>

#### Jupyter notebook Link : https://github.com/rp192/ML-projects
#### Goal

Predicting the energy usage in of the house based on 20+ factors including signals obtained from the sensors around the house. The goal is to use regression to predict the energy usage. 

#### Steps followed 

- Step 1 : Loading the necessary libraries such as Numpy, Pandas and sklearn.
- Step 2 : Loading the .csv file dataset into a pandas dataframe.
- Step 3 : Data.info() is used to gain preliminary information about the data such as the attributes, their non-null counts and the data type of the values stored for the attributes. This step is essential for data cleaning by converting the attribute to an appropriate data type.
![describe](https://github.com/user-attachments/assets/2fa3146f-3582-46bb-93c3-2d2f68d73a18)
- Step 4 : Describing the dataset reveals insights into the mean, standard deviation in the values, min & max which is useful in understanding the shape of data. Appliances is our target variable.
![info](https://github.com/user-attachments/assets/db77a98a-8856-4908-9ecc-e708f77fbffd)
- Step 5 : Visulalizing the skewness of the data is important as it helps as prepare the data by scaling so as to get accurate predictions hence plotting histogram of the data for each attribute .
![hist](https://github.com/user-attachments/assets/7e36bb9c-f7f0-4151-9933-f6afb29ea678)
- Step 6 : Observing the histograms give us an idea about the shape 
         
   a) The appliances is Right skewed.

   b) T4 and T8 has similiar influence

   c) Rv1 and RV2 seem to be irrelevant as they are evenly distributed

- Step 7 : To predict the accurate usage it is the best practice to use only relevant attributes and redundancy will decrease the performance of the model, hence finding the correlation between the attributes is necessary and then producing a heat map with it so that it is easier to read.
![heatmap](https://github.com/user-attachments/assets/35136579-9361-45fa-92a8-364145ba17d3)
- Step 8 : Next step for data cleaning is dealing with the outliers. Boxplot is used to identify the extent of outliers.
![appliances](https://github.com/user-attachments/assets/4b868da6-f9b9-473b-9d69-47d68189654b)
![other](https://github.com/user-attachments/assets/fde4e1c8-f86c-4f06-82d4-0c4f653a3a33)
- Step 9 : Removing the outliers.
      
      a) Dropping the outliers based on the box plot analysis as majority data lies in the scale of 0 to 200
      b) The attributes of T6,T9, Visibility, pressure, Tdewpoint, Rh_1,RH_2 seems to be irrelevant as analyzed by heatmap above.

- Step 10 : Splitting the training and test data in the rato of 80:20. Random state is introduced so that if you run a different instance to get the same data to be split you shoudl use the same state.

      x_train, x_test, y_train, y_test = train_test_split(X, Y, test_size=0.2, random_state = 42) 

- Step 10 : Scaling the data is important so that the range of all the values in a dataset is of same range as regression analysis is mathematical and prediction is done on slope of the line, this is necessary.

      from sklearn.preprocessing import StandardScaler
      scaler = StandardScaler()
      scaler.fit(x_train)
      x_train = scaler.transform(x_train)
      x_test = scaler.transform(x_test

#### Evaluation of model

Evaluation of linear regression is as follows
      
      LinearRegression() 
      Average Error(Mean Absolute Error)       : 19.2971 degrees
      Variance score R^2  : 27.15%
      Accuracy            : 68.97%


Evaluation of SVR model is as follows

      SVR() 

      Average Error(Mean Absolute Error)       : 17.6548 degrees
      Variance score R^2  : 28.56%
      Accuracy            : 74.11%
      The accuracy of the model is 74.11%

Following inferences can be drawn from the output

#### [1] SVR performs better than simple linear regression.
#### [2] Skweness of Applicanes i.e. Target variable is not taken into consideration.
\
Further tuning of the model will result into better model prediction.

### Spotify genre predictiion in R <a name="R"></a>

#### RMD file : https://github.com/rp192/Spotify_genre_prediction/tree/master
#### Goal

Analysing and building predictive models
for Spotify to predict the genre of the song by using data such as

      - the year the song was released
      - how “speechy” the song is
      - how danceable the song is
      - the tempo of the song

#### Steps followed 

- Step 1 : Loading the necessary libraries such as Tidyverse,ggplot, lubridate and tidymodels
- Step 2 : Reading the .csv file dataset which is at a remote location to a dataframe.
- Step 3 : Skim without charts gives vital information such as number of rows and columns in the dataset and differentiate charcter and numeric variables.
![skimr](https://github.com/user-attachments/assets/41ed2b6a-3c57-44cb-a37a-b13f725e57e7)
- Step 4 : Getting rid of null values by 
            
            spotify_songs <- na.omit(spotify_songs)

- Step 5 : Slicing the dataset to 1000 songs in each genre. Using the pipe operator '%>%' from dpylr in R , you can basically recreate SQL syntax in R. 
            
            song_select <- song_select %>%
            group_by(playlist_genre) %>%
            sample_n(1000) %>%
            ungroup()

- Step 6 : Factorizing the target variable by using as.factor, R automatically converts it for you.
            
            song_select$playlist_genre = as.factor(song_select$playlist_genre)

- Step 7 : To get insight into the data, visualization is done. Plotting a side by side boxplot of Popularity vs Genre helps in gaining valueble insights.
![pvsg](https://github.com/user-attachments/assets/5c685b2c-8df0-4ef6-952b-f232e554208f)

            a) It is evident that ‘Pop’ has the most poluarity
            b) ‘Latin’ slightly less popular than pop
            c) Rest of the genre having relatively high popularity than ‘EDM’
            d) Popularity differs between genres

- Step 8 : Next step is to plot a side by side boxplot on Speachiness vs Genre.
![speachvsgenre](https://github.com/user-attachments/assets/496485d9-3845-4a40-9088-90410af8c4cf)

            a)The above box plot concludes that ‘Rap’ and ‘R&B’ genre has more speechiness distribution.
            b)‘Rock’ genre being the least.
- Step 9 : Next step is to visualise the mean popularity of a genre over the years from 1960 to 2020.
![avg](https://github.com/user-attachments/assets/6a8738c4-c998-4a02-a077-94247b63082a)

- Step 10 : Splitting the training and test data in the rato of 80:20. Random state is introduced so that if you run a different instance to get the same data to be split you shoudl use the same state. 

- Step 10 : First model to build is  Linear discriminant analysis (LDA).

      set.seed(1893161)
      song_split = initial_split(song_select)
      song_train = training(song_split)
      song_test = testing(song_split)

#### Evaluation of model

Evaluation of linear regression is as follows

![accuracy](https://github.com/user-attachments/assets/45cb1650-795e-4ab5-9197-1145c7b50d6b)

Following inferences can be drawn from the output

##### [1] Accuracy of only 0.408 is achieved with LDA.
##### [2] Future work is required using KNN and Random forest regression.
