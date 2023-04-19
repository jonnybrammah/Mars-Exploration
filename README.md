# Mars-Exploration
-----
![Curiosity Rover (Image Courtesy NASA/JPL-Caltech)](https://mars.nasa.gov/system/news_items/main_images/9378_PIA25413Cropped-web.jpg)

## Project Description
Having successfully analyzed the weather in cities across the world in a [previous project](https://github.com/jonnybrammah/World_Weather_Analysis) using APIs, the goal of this project was to analyze the weather on Mars by scraping data from the internet. This was done by running code in a jupyter notebook, which imported splinter to automate the browser and BeautifulSoup to parse the resulting html data. Pandas was used to analyze the resulting data in dataframes and matplotlib was used to visualize some of the important data.

-----

### Table of Contents
  1. [Data Exploration](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-exploration)
  2.[Data Analysis](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-analysis)

-----

### Data Exploration
- The first section of this project was to pull some recent news articles about Mars from [a Mars Planet Science webpage](https://static.bc-edx.com/data/web/mars_news/index.html). The code for this is in the [part_1_mars_news.ipynb file](https://github.com/jonnybrammah/Mars-Exploration/blob/main/part_1_mars_news.ipynb).
- The second section was to pull some information about the weather on Mars from [a Mission to Mars webpage](https://static.bc-edx.com/data/web/mars_facts/temperature.html). The code for this is in the [part_2_mars_weather.ipynb file](https://github.com/jonnybrammah/Mars-Exploration/blob/main/part_2_mars_weather.ipynb).
   - This section was more involved. The code here runs through the table in html format and goes through each row and stores each element as an element in a list. These lists are then all appended into a list of lists, which can be easily converted into a dataframe for analysis.
   - After some data cleaning, the questions to be answered were:
 1. How many months exist on Mars?
 2. How many Martian days of data are present in the dataset?
 3. What are the coldest and warmest months on average on Mars?
 4. Which months have the highest atmospheric pressure on Mars?
 5. How many terrestrial Earth days exist in a Martian year?
 
 -----
 
 ### Data Analysis
By counting the number of rows associated with each Martian month, it is possible to see that the dataset lists a total of <strong>12 Martian months</strong>, with a total of <strong>1867</strong> Martian days of data contained in the total dataset (over several years).

The temperature associated with each Martian month could then be identified. With no atmosphere, all temperatures are incredibly cold by Earth standards, but variability still exists between months due to the planet's slight changes in distance from the Sun.
The graph below shows the average minimum temperature at Curiosity's location on Mars for each month, and the seasonal variation is visible in the pattern.
![Minimum_Temperature Graph](https://raw.githubusercontent.com/jonnybrammah/Mars-Exploration/main/Output/Images/min_temp_by_month.png)

You can see from the graph that the coldest month is Month number 3 with an average minimum temperature of -83.3°C 
 4. What are the coldest and warmest months on average on Mars?
 5. Which months have the highest atmospheric pressure on Mars?
 6. How many terrestrial Earth days exist in a Martian year?
