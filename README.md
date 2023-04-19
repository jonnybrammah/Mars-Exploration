# Mars-Exploration
-----
![Curiosity Rover (Image Courtesy NASA/JPL-Caltech)](https://mars.nasa.gov/system/news_items/main_images/9378_PIA25413Cropped-web.jpg)

## Project Description
Having successfully analyzed the weather in cities across the world in a [previous project](https://github.com/jonnybrammah/World_Weather_Analysis) using APIs, the goal of this project was to analyze the weather on Mars by scraping data from the internet. This was done by running code in a jupyter notebook, which imported splinter to automate the browser and BeautifulSoup to parse the resulting html data. Pandas was used to analyze the resulting data in dataframes and matplotlib was used to visualize some of the important data.

-----

### Table of Contents
- [1. Data Exploration](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-exploration)
- [2. Data Analysis](https://github.com/jonnybrammah/Mars-Exploration/blob/main/README.md#data-analysis)

-----

### Data Exploration
- The first section of this project was to pull some recent news articles about Mars from [a Mars Planet Science webpage](https://static.bc-edx.com/data/web/mars_news/index.html). The code for this is in the [part_1_mars_news.ipynb file].
- The second section was to pull some information about the weather on Mars from [a Mission to Mars webpage](https://static.bc-edx.com/data/web/mars_facts/temperature.html)
