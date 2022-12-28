# Study of flu trends during rainy seasons

## Project Background 

This is the first graded project, as part of the General Assembly Data Science Immersive (Flex) course. 

## Problem Statement

In the recent years, Covid-19 has been the focus of our lives. Besides the normal hygeniene precautions, we have been asked to be more vigilant during the rainy season to prepare for the spike in cases. How true would that be? We will find out

The purpose of the study is to find out whether flu cases are more prevalent during rainy seasons.The inspiration of the study is derived from [this article.](https://www.channelnewsasia.com/commentary/influenza-cold-sick-covid-vaccine-tripledemic-3133906)

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

tbd

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
