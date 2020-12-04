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

I used pandas to read in the csv data to create a dataframe

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
To use the USA States geometry, I need to  provide the  locations as two-letter state abbreviations: The states column contained the full name I used the .map() with this dictionary to map the full state name to the two-letter state abbreviation
```python
us_state_abbrev = {
    'Alabama': 'AL', 'Alaska': 'AK',
    'American Samoa': 'AS', 'Arizona': 'AZ', 'Arkansas': 'AR', 'California': 'CA', 'Colorado': 'CO', 'Connecticut': 'CT', 
    'Delaware': 'DE', 'District of Columbia': 'DC', 'Florida': 'FL', 'Georgia': 'GA', 'Guam': 'GU', 'Hawaii': 'HI',
    'Idaho': 'ID', 'Illinois': 'IL', 'Indiana': 'IN','Iowa': 'IA', 'Kansas': 'KS', 'Kentucky': 'KY','Louisiana': 'LA',
    'Maine': 'ME','Maryland': 'MD', 'Massachusetts': 'MA', 'Michigan': 'MI', 'Minnesota': 'MN', 'Mississippi': 'MS','Missouri': 'MO',
    'Montana': 'MT','Nebraska': 'NE','Nevada': 'NV','New Hampshire': 'NH','New Jersey': 'NJ','New Mexico': 'NM','New York': 'NY',
    'North Carolina': 'NC', 'North Dakota': 'ND','Northern Mariana Islands':'MP','Ohio': 'OH', 'Oklahoma': 'OK','Oregon': 'OR',
    'Pennsylvania': 'PA','Puerto Rico': 'PR','Rhode Island': 'RI', 'South Carolina': 'SC','South Dakota': 'SD','Tennessee': 'TN',
    'Texas': 'TX', 'Utah': 'UT', 'Vermont': 'VT', 'Virgin Islands': 'VI','Virginia': 'VA', 'Washington': 'WA',
    'West Virginia': 'WV','Wisconsin': 'WI','Wyoming': 'WY'
}
```
```python
temple_count_state['Abbrev'] = temple_count_state['State'].map(us_state_abbrev)
```








