# LDS Temples World Wide
For this project I will be geographical ploting and  analyzing how many and where are all the LDS temples are located worldwide with data from [Temples of the Church of Jesus Christ of Latter Day Saints](https://churchofjesuschristtemples.org/maps/downloads/). The CSV file contains the following data fields:

* Temple
* Latitude
* Logitude
* LatitudeDegrees
* LongitudeDegress
* Address
* City
* State 
* Postal Code
* Country
* Phone

## Technology Used
* Pandas
* MatplotLib
* Seaborn
* Plotly
* [Cufflinks](https://github.com/santosjorge/cufflinks)

## Process
### Analysis

I used pandas to read in the csv dat to create a dataframe

```python
data = "Resources/ChurchofJesusChristTemples.csv"
temple_data = pd.read_csv(data)
temple_data.head()
```

I checked the date set for any crucial values missing by using isnull() how many rows and columns the data set contained by using .shape and nunique() to determine the number of unique values in the temple column. 

#### Question
How many temples are there world wide?

What are the top 5 countries with temples?

How many temples in the USA?

What are the top 5 US States with temples?


#### Graphs
I used plotly to cretate interactive maps of the temples by country and US states. 


##### Country Graphs


##### State Graphs
In order to create state graphs I need to convert the State column from full US state name to be abbriviated by creating a dictionary with state abbriviations and using .map to create a new column with state abbrivations








