# Study of flu trends during rainy seasons

## Project Background 

This is the first graded project, as part of the General Assembly Data Science Immersive (Flex) course. 

## Problem Statement

**Aim: To find out if rainy seasons has a correlation with the number of flu cases in Singapore**

Flu season is an annually recurring time period characterized by the prevalence of an outbreak of influenza, and it is widely known to happen during colder seasons. Recently, there was a commentary in Singapore that has warned the public against the flu season ahead of the upcoming December holidays. 

To quote the article: "In Singapore, we experience year-round circulation of influenza virus, with two prominent peaks from May to July and from December to February, coinciding with the rainy seasons."

The aim of the study is to study the variations of Singapore's rainfall, and whether this will lead to a 'flu season'. We will be using the covid-19 cases as a proxy to measure flu cases.

![image.png](![flu-peak-activity-2021-2022](https://user-images.githubusercontent.com/17240005/212446653-6e9d3491-5ceb-442a-85c5-3819af1940da.jpeg)
)
    </br> source: Centres for Disease Control and Prevention, US

**Findings**:
1. Flu season in US typically happens from [Dec-Feb](https://www.cdc.gov/flu/about/season/flu-season.htm). US experiences [its coldest periods during Dec.](https://www.ncei.noaa.gov/news/coldest-day-of-the-year#:~:text=Most%20prominently%2C%20the%20portion%20of,its%20seasonal%20minimum%20in%20January.)

2. Flu season in Australia typically happens from [May - Oct](https://www.health.gov.au/our-work/influenza-surveillance-program#annual-influenza-reports). Australia experiences [its coldest month in July](http://www.bom.gov.au/climate/updates/articles/a028.shtml)

From these two examples, We can sense that the flu seasons typically happen during the countries' coldest periods
---

## Datasets

All datasets were obtained from [data.gov.sg](https://data.gov.sg). 
1. [total amount of rainfall of the month](https://data.gov.sg/dataset/rainfall-monthly-total)
2. [monthly maximum daily total rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
3. [number of rainy days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)
4. [monthly mean temp](https://data.gov.sg/dataset/surface-air-temperature-monthly-mean)
5. [monthly relative humidity](https://data.gov.sg/dataset/relative-humidity-monthly-mean)
6. [epidemic curve](https://data.gov.sg/dataset/covid-19-case-numbers)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|date|datetime|all datasets|Jan 1982 - Aug 2022 (datasets #1 & #3), Jan 1982 - Oct 2022 (datasets #2 & #5), Jan 1982 - Nov 2022 (dataset #4)
|year|integer|all datasets|1982 - 2022
|month|integer|all datasets|Jan - Dec, represented by 01 - 12 respectively
|decade|obj|merged_df|80s to 2020s
|season|obj|merged_df|Northeast Monsoon (Dec-Feb), Southwest Monsoon (Jun-Sept), Inter-monsoon (Oct-Nov), Inter-monsoon (May-Mar)
|total rainfall|float|rainfall-monthly-total|the total monthly rainfall, recorded in millimetre| 
|maximum daily rainfall|float|rainfall-monthly-highest-daily-total|the highest daily total rainfall for the month in millimetre| 
|number of rainy days|int|rainfall-monthly-number-of-rain-days|the number of rain days (day with rainfall amount of 0.2mm or more) in a month| 
|mean daily surface air temperature|float|relative-humidity-monthly-mean|in Degree Celsius|
|monthly relative humidity|float|relative_humidity-monthly-mean|Percentages, expressed as a value over 100. It represents the ratio of how much water vapour is in the air and how much water vapour the air could potentially contain at a given temperature.|
|imported Covid cases|int|epidemic-curve|Number of cases in a month|
|local Covid cases|int|epidemic-curve|Number of cases in a month, this number will be used in most of the analysis|
|total Covid cases|int|epidemic-curve|Number of cases in a month|

### Related to rainfall
* [Monthly number of rainy days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)
* [Monthly total rainy days](https://data.gov.sg/dataset/rainfall-monthly-total) 
* [Monthly Maximum Daily Rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)

### Other supporting datasets
* [Monthly mean temperature](https://data.gov.sg/dataset/surface-air-temperature-monthly-mean)
* [Monthly relative humidity](https://data.gov.sg/dataset/relative-humidity-monthly-mean)
* [Epidemic curve](https://data.gov.sg/dataset/covid-19-case-numbers)

---

## Techniques and methodology
1. Import and clean data
    * check for null values
    * convert datetime values from object to datetime format
2. Minor feature engineering
    * group years into decades
    * group months into seasons
3. Data Dictionary
4. EDA
    * Summary statistics
    * Which month have the highest and lowest total rainfall in 1990, 2000, 2010 and 2020?
    * Which year have the highest and lowest total rainfall in the date range of analysis?
    * Which month have the highest and lowest number of rainy days in 1990, 2000, 2010 and 2020?
    * Which year have the highest and lowest number of rainy days in the date range of analysis?
    * Are there any outliers months in the dataset?
    * If there are outliers, how many datapoints/occurences are there throughout the trends?
      *  Aided with the box-and-whiskers plots
5. Data visualizations on matplotlib and seaborn
- Rainfall and weather analysis: 
    * Plot the histogram of the rainfall data with various bins and comment on the distribution of the data - is it centered, skewed?
    * Is there a correlation between the number of rainy days and total rainfall in the month? What kind of correlation do your suspect? Does the graph show the same?
    * Rainfall across all months to find seasonality - when does it rain most across the decades?
    * How does total rainfall correlates with the number of rainy days by season, and does this change across the decades?
    * Does more rainy days means there is a higher humidity? does that change across the seasons and decades?
    * Is there any relationship between mean temperature and mean relative humidity?
- Covid-19 and rainfall analysis:
    * find out the correlation between Covid-19 cases and the variables related to weather
    * how does the number of cases grow across time?
    * number of local cases by season across the years
    * find out the pattern by months across the three years in pandemic
    * A closer look at the pattern of correlation between number of rainy days, mean temperature, and mean humidity with the number of local cases
---

## Conclusion and recommendation

**Conclusion:** Singapore has a pretty stable weather conditions, with a gradual increase of total rainfall per month in the recent decades. The number of rainy days is roughly 14 days, and the temperature is roughly 27 degree celcius. The Northeast Monsoon season (Dec-Feb) often has the highest amount of rainfall and maximum amount of rainfall. Singapore also has a pretty stable relative humidity as well.

Having said that, there is still a slight variation in total rainfall, number of rainy days, temperature, and humidity. Rise in flu cases usually happens after the Northeast Monsoon season, which has the most amount of rain and rainy days.

**Key takeaways / recommendations:** 
1. Are the cases always increasing during the rainy seasons? 
    * From the analysis, it is not that conclusive as the data is not so complete
    * Flu cases are might be more affected by other factors, such as the country's policies of opening up, personal lifestyle and hygiene, as well as immunity. 
    * Also, most of the festive seasons important to Singaporeans such as Christmas, New Year, and Chinese New Year happens during this period.
    * There might be scenarios of under-reported cases after the government's opening up policies, where individuals do not have to declare their status if they are not tested positive in a medical establishment
2. There is a potential for deeper analysis with the suitable data, i.e.: immunity rate in Singapor
3. Although the positive correlation is minimal, we should take the necessary precautions as we live with covid.
---

## Libraries
* Pandas
* Numpy
* Matplotlib
* Seaborn
 
---

## References
1. [Timeline of Covid-19](https://en.wikipedia.org/wiki/Timeline_of_the_COVID-19_pandemic_in_Singapore_(2021))
2. [Singapore climate](http://www.weather.gov.sg/climate-climate-of-singapore/)
3. [Commentary on Tripledemic in Singapore](https://www.channelnewsasia.com/commentary/influenza-cold-sick-covid-vaccine-tripledemic-3133906)
4. [Flu season](https://en.wikipedia.org/wiki/Flu_season)
