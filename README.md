# Mars-Exploration
-----
![Curiosity Rover (Image Courtesy NASA/JPL-Caltech)](https://mars.nasa.gov/system/news_items/main_images/9378_PIA25413Cropped-web.jpg)

## Project Description
Having successfully analyzed the weather in cities across the world in a [previous project](https://github.com/jonnybrammah/World_Weather_Analysis) using APIs, the goal of this project was to analyze the weather on Mars by scraping data from the internet. This was done by running code in a jupyter notebook, which imported splinter to automate the browser and BeautifulSoup to parse the resulting html data. Pandas was used to analyze the resulting data in dataframes and matplotlib was used to visualize some of the important data.

-----

### Table of Contents
1. [Data Exploration](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-exploration)
2. [Data Analysis](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-analysis) </br>

    a) [Martian Months and Martian Days](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#Martian-Months-and-Martian-Days)
    b) [Temperature by Month on Mars](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#Temperature-by-Month-on-Mars)
    c) [Pressure by Month on Mars](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#Pressure-by-Month-on-Mars)
    d) [Terrestrial Days in Martian Year](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#Terrestrial-Days-in-Martian-Year)

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

#### Martian Months and Martian Days
By counting the number of rows associated with each Martian month, it is possible to see that the dataset lists a total of <strong>12 Martian months</strong>, with a total of <strong>1867</strong> Martian days of data contained in the total dataset (over several years).

#### Temperature by Month on Mars
The temperature associated with each Martian month could then be identified. With no atmosphere, all temperatures are incredibly cold by Earth standards, but variability still exists between months due to the planet's slight changes in distance from the Sun.
The graph below shows the average minimum temperature at Curiosity's location on Mars for each month, and the seasonal variation is visible in the pattern.
![Minimum Temperature Graph](https://raw.githubusercontent.com/jonnybrammah/Mars-Exploration/main/Output/Images/min_temp_by_month.png)

You can see from the graph that the coldest month is Month number 3 with an average minimum temperature of -83.3°C. The warmest month is roughly half a year later (as expected) at Month number 8, which has an average minumum temperature of -68.4°C.
This is perhaps more visible in the following graph which shows the average minimum temperature against month, but sorted from coldest to warmest:
![Minimum Temperature Graph](https://raw.githubusercontent.com/jonnybrammah/Mars-Exploration/main/Output/Images/min_temp_by_month_sorted.png)

#### Pressure by Month on Mars
The pressure associated with each Martian month was also then identified from the data, and this is also shown in the graph below:
![Pressure Graph](https://raw.githubusercontent.com/jonnybrammah/Mars-Exploration/main/Output/Images/pressure_by_month_sorted.png)

From the graph, it can be seen that the highest pressure occurs in Month number 9, with a pressure of 913 Pa (about 100 times lower than atmospheric pressure on Earth). The lowest pressure recorded was in Month number 6, with a record low of 745 Pa.

#### Terrestrial Days in Martian Year
Finally, an estimate of the number of terrestrial days in a Martian year was made by plotting the minimum temperature recording from the Curiosity rover against the count of terrestrial days. This results in the following graph:
![Temperature per terrestrial day Graph](https://raw.githubusercontent.com/jonnybrammah/Mars-Exploration/main/Output/Images/min_temp_per_terrestrial_day.png)

As discussed in the temperature section, we would expect the minimum temperature to fluctuate seasonally due to the changes in distance from the planet to the Sun, and this seasonal variation is visible in the graph. By counting the number of terrestrial days between two peaks or troughs, we can estimate how many terrestrial days occur between one full cycle of Mars' orbit. This results in about 625 Earth days in one Martian year. A google search for the same thing reveals the expected result is about [687 days](https://mars.nasa.gov/all-about-mars/facts/mars-year), which puts my estimate off by a percentage difference of about 9%.
