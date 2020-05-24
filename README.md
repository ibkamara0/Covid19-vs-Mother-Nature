# Covid19-vs-Mother-Nature
As crazy as it may sound, my passion for data science is what motivated me to want to complete this project. I began this project hoping to visualize some positive data, in the light of our current situation. Lastly, I used this as an opportunity to enhance my knowledge in data science and potentially get some professional feedback.
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
- I web scraped by finding the element, then inspecting the html format of the element. With the link and heading of the data, I then requested the information from that specific URL, converted it to text, then parsed to find the weather information needed for this project. I used automation to help me iterate through different months using the same URL, just changing the month in the URL. Below is me inspecting the webpage to find where the data is located, in terms of HTML format.

![web scraping](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/web%20scraping.gif)

### Cleaning the data
First, I automated the process of recieving of the weather information. I then integrated it with the data from the csv, to create a complete dataframe that stored the Date, High Temperature, Low Temperature, and Average Temperature, and Number of Cases, for different areas. Afterwards, I normalized the data so that we can visualize different areas on the same scale. Normalizing data, meaning all the data wil be on a scale from 0 to 1.

Next, I created a dataframe that stored the increase in confirmed cases by percentage with its' respective temperature. I grouped the data by weeks and offset the data by one week. So, for example the average temperature for this week will affect next week's rise of confirmed cases.

Lastly, I removed outliers by only including data within certain range or standard deviation, This left me with a simple, more realistic dataset. The reason for this was because the initial spike in cases was causing alot of noise if the data set. For this project, I was more concerned with what happened after the intial spike when tests became more prominent, and how they confirmed cases slowed down.

## Data Analysis
I measured the correlation using Spearman correlation coefficient which has a scale of -1 to 1. -1 is perfect negative correlation, 1 is positive correlation, and 0 is no correlation. Positive correlation means as one variable increases so does the other. Negative correlation means as one increases the other decreases. Below is what was returned from the Spearman Correlation.

- **Spearman's Correlation Value:** -.6089704636091255

Not great but you can see just from this that there is a negative correlation, because it is closer to -1 then 0 or 1.

We can visualize the data and the correlation below, the weather is on the x-axis and the increase in confirmed cases on the y-axis. What is also seen is the best fit line generated through machine learning (red). This line help to display the trend of the points:

![Visualization of Data](https://github.com/ibkamara0/Covid19-vs-Mother-Nature/blob/master/Data%20Visualization.jpg)

Key:
- **Cyan:** New York, NY
- **Yellow:** Los Angeles, CA
- **Magenta:** Wayne, MI
- **Green:** Hudson, NJ
- **Blue:** Philadephia, PA
- **Red:** Linear Model

### Explanation of Visualization

What this graph represents is the weather and the growth of confirmed Covid-19 cases. This means that in relation to their area the higher to temperatures the lower percentage of growth, with the amount of Covid-19 cases. You can see this in the visual, while the are some point that do not correlate you can see that as you move along the x-axis (weather increases), you move down the y-axis(there is less increase confirmed Covid-19 cases).


## Conclusion
Now, I am not a data scientist, YET(one day)! This project was simply done for fun and to also gain experience and feedback doing one of the things I love. Who knows what this virus is capable of, we must all proceed with caution. My main goal for this project was to get a grasp of different data science skills, packages, and research methods. Please feel free to share with me any feedback you have on this project whether be good or bad. I will appreciate any feedback and as put myself out on the job market please let me know more ways to make myself more proficient and marketable in the world of data science.

Thank you. Stay safe and together we can all get through this. #HungryGrad

## Contact Information

- **Email:** ibkamara1997@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/ibrahim-kamara-81b427139/
