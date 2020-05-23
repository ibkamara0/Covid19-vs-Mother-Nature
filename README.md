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
