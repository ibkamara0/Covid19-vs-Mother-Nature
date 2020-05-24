# Covid19-vs-Mother-Nature
As crazy as it may sound, I did this project out of my sheer enjoyment of data science. I wanted to one, see if I could visualize some good news, then two, gain experience and sharpen my knowledge and skills in data science.
## Overview
- Web scraped, read, parsed and cleaned data for easier implementation into machine learning model
- Created a visual representation of the relationship between increase in weather temperature and change in Covid19 confirmed cases
- Used machine learning to generate a model that displays a linear correlation between the two variables
- Extracted meaningful information from large dataset
## Resources and Data Acquisition
- Packages: scipy, sklearn, statistics, seaborn, matplotlib, pandas, numpy
- **Kaggle Data**: https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset
- **Weather Data**: https://www.accuweather.com/

## Data Preprocessing
- Web scraped and parsed data from accuweather.com 
- Read and transformed csv file by reading into dataframe using pandas, to give data more readable format
### Web Scraping
- I web scraped by finding the element, then inspecting the html format of the element. With the link and heading of the data, I then requested the information from that specific URL, converted it to text, then parsed to find the weather information needed for this project. I used automation to help me iterate through different months using the same URL, just changing the month in the URL. Below is me inspecting the webpage to find where the data is located.

![web scraping](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/web%20scraping.gif)

### Cleaning the data
First, I automated the process of recieving of the weather information. I then integrated it with the data from the csv, to create a complete dataframe that stored the Date, High Temperature, Low Temperature, and Average Temperature, and Number of Cases, for different areas. Then I normalized the data so that we can visualize different areas on the same scale. Normalizing data, meaning all the data wil be on a scale from 0 to 1.

Next, I created a dataframe that stored the increase in confirmed cases by percentage with its' respective temperature. I grouped the data by weeks and offset the data by one week. So, for example the average temperature for this week will affect next week's rise of confirmed cases.

Lastly, I removed outliers by only including data within certain range or standard deviation, This left me with a simple, more realistic dataset. The reason for this was because the initial spike in cases was causing alot of noise if the data set. For this project, I was more concerned with what happened after the intial spike when tests became more prominent, and how they confirmed cases slowed down.

## Data Analysis
I measured the correlation using Spearman correlation coefficient which has a scale of -1 to 1. -1 is perfect negative correlation, 1 is positive correlation, and 0 is no correlation. 

- **Spearman's Correlation Value:** -.6089704636091255

Not great but you can see just from this that there is a negative correlation

We can visualize the data and the correlation below:

![Visualization of Data](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/Data%20Visualization.jpg)

Key:
- **Cyan:** New York, NY
- **Yellow:** Los Angeles, CA
- **Magenta:** Wayne, MI
- **Green:** Hudson, NJ
- **Blue:** Philadephia, PA
- **Red:** Linear Model

### Explanation of Visualization

What this graph represents is the weather and the growth of Covid19 cases. This means that in relation to their area the higher to temperatures the lower percentage of growth, with the amount of Covid19 cases.


## Conclusion
Now, I am not a data scientist, YET!! This project was simply done for fun. Who knows what this virus is capable of. My main goal for this project was to get a grasp of different data science skills, packages, and knowledge. Please feel free to share with me any feedback you have on this project whether be good or bad. As, I put myself out on the job market please let me know more ways to make myself more proficient and marketable in the world of data science.

## Contact Information

- **Email:** ibkamara1997@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/ibrahim-kamara-81b427139/
