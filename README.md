# Do we have to be more prepared during rainy seasons?

## Project Background 

This is the first graded project, as part of the General Assembly Data Science Immersive (Flex) course. 

## Problem Statement

In the recent years, Covid-19 has been the focus of our lives. Besides the normal hygeniene precautions, we have been asked to be more vigilant during the rainy season to prepare for the spike in cases. How true would that be? We will find out

The purpose of the study is to find out whether flu cases are more prevalent during rainy seasons.  

[Inspiration of the study](https://www.channelnewsasia.com/commentary/influenza-cold-sick-covid-vaccine-tripledemic-3133906)

---

## Datasets

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
    * Which month have the highest and lowest total rainfall in 1990, 2000, 2010 and 2020?
    * Which year have the highest and lowest total rainfall in the date range of analysis?
    * Which month have the highest and lowest number of rainy days in 1990, 2000, 2010 and 2020?
    * Which year have the highest and lowest number of rainy days in the date range of analysis?
    * Are there any outliers months in the dataset?
    * If there are outliers, how many datapoints/occurences are there throughout the trends?
      *  Aided with the box-and-whiskers plots
5. Data visualizations on matplotlib and seaborn
    * Plot the histogram of the rainfall data with various bins and comment on the distribution of the data - is it centered, skewed?
    * Is there a correlation between the number of rainy days and total rainfall in the month? What kind of correlation do your suspect? Does the graph show the same?
    * (to be continued) Rainfall across all 
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
