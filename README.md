# Covid19-vs-Mother-Nature
As crazy as it may sound, I did this project out of my sheer enjoyment of data science. I wanted to one, see if I could visualize some good news, then two, gain experience and sharpen my knowledge and skills in data science.
## Overview
- Web scraped, read, parsed and cleaned data for easier implementation into model
- Created a visual representation of the relationship between increase in weather temperature and increase of Covid19 confirmed cases.
- Used machine learning to generate a model that displays a linear correlation between the two variables
- Extracted meaningful information from large dataset
## Resources and Data Acquisition
- Packages: scipy, sklearn, statistics, seaborn, matplotlib, pandas, numpy
- **Kaggle Data**: https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset
- **Weather Data**: https://www.accuweather.com/

## Data Preprocessing
- Web scraped data from accuweather.com 
- Read csv file and cleaned by inserting into dataframe, and cleaning to increase efficiency
### Web Scraping
- Found the element that will be parsed by inspecting the website. With the link and heading location of the data, just request the website, convert it to text, then parse to find the information of the data we're looking for

![web scraping](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/web%20scraping.gif)

### Data Cleaning
Automated the recieving of the weather information and integrated with the data from the csv, to create a data frame that stored the Date, High Temperature, Low Temperature, and Average Temperature, and Number of Cases, for different areas. Then I normalized the data so that we can visualize different areas on the same scale

Created a dataframe that stored the increase in confirmed cases as percentage with its' respective temperature. The temperature would be relative to the increase in cases the week after. 

Removed outliers by only including data within certain standard deviation, leaving us with a simple more realistic dataset. The reason for this was because the initial spike in cases was causing alot of noise if the data set. I was more concerned with after the intial spike when tests became more prominent, what was the effect then.

## Results
I measured the correlation using Spearman correlation coefficient which has a scale of -1 to 1. -1 is perfect negative correlation, 1 is positive correlation, and 0 is no correlation. 

- **Spearman's Correlation Value:** -.6089704636091255

Not great but you can see just from this that there is a negative correlation

We can visualize the data and the correlation below:

![Visualization of Data](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/Data%20Visualization.jpg)

Key:
- **Cyan** New York, NY
- **Yellow:** Los Angeles, CA
- **Magenta** Wayne, MI
- **Green:** Hudson, NJ
- **Blue:** Philadephia, PA
- **Red:** Linear Model
