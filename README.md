# Data-Analysis-of-the-Global-Disaster-Titanic
EDA is Exploratory and Explanatory Data Analysis. There is so many global disaster in this world, one of the legendary story is Titanic. Titanic is the one of the biggest cruise in the world, it launched on May 31, 1911. Titanic broke apart and sank to the bottom of the ocean, taking with it the lives of more than 500 passengers and crews
the project you can check on https://colab.research.google.com/drive/17RX86X6NHKHGcuqjIeUQs1fo0jq9Sj6p

# Methodes
In this project, I used the pandas for python to manipulation and analyze the data. 
I used the Exploratory and Explanatory Data Analysis as the main methode.

# Exploratory Data Analysis

In Exploratory Data Analysis, the methodes is found the head, the tail, and 5 samples random.
and the results is:
- There has two columns of numericals(survived and age) and 2 columns of categorical (name and sex)
- Sex column seems to contain two distinct values (female OR male), but will confirm later
- Survived is apparently also binary (0,1)
- No obvious on the data (column name vs its entries), all seems good

# Statistical Summary

A statistics summary gives information about the data in a sample. It can help understand the values better. It may include the total number of values, minimum value, and maximum value, along with the mean value and the standard deviation corresponding to a data collection. With this, you can understand the trends, outliers, and distribution of values in a data set. The result is : 
- Overall, the minimum and maximum values make sense for each column
- Mean ~50% (Median) in AGE is somewhat symmetrical distribution
- Survived column is boolean/binary column since the values is 1 or 0, no need to conclude its simmetricity. Only need to check balance level

# Cleaning Data

In this methode there is 2 ways for cleaning the datas:
- Duplicates Handling by : df = df.drop_duplicates()
- Missing Values Handling by : df.isna().sum()
        - The percentage of missing values below 20% so we handle numerically with median, categorical with mode :
          # if the column is objects use mode,
        df[column].fillna(df[column].mode()[0], inplace=True)
    else: # if the data is numericals and objects, there is no other type, used the methode below:
          # if the column is numericals user median,
        df[column].fillna(df[column].median(), inplace=True)


  # Result
  If the results is:
Index: 499 entries, 0 to 499
Data columns (total 4 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   survived  499 non-null    int64  
 1   name      499 non-null    object 
 2   sex       499 non-null    object 
 3   age       499 non-null    float64
dtypes: float64(1), int64(1), object(2)
memory usage: 19.5+ KB

the cleaning data is done. 




