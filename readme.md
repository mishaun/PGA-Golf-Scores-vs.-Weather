# PGA Tour Golf Data Project

<br>

# Overview
As a golf enthusiast, the desire to see historical golf tournament results at my fingertips was essential for answering questions that not even ChatGPT can generate for me.  I wanted to take a deeper dive on how weather impacts tournament results, which courses are difficult, player details, and much more.  

This project allowed me to practice key data analytical skills to scrape raw data, clean, and finally build a useful dashboard!

<br>

# Goals of Project
1. Compile golf tournament historical records in one location to answer questions like:
    * Who has won the most in the past 20+ years per starts 
    * What courses proved to be the most difficult
    * How does weather potentially impact scores for a given week based on wind and rain.  
        * How does it impact scores if it rains before the tournament but not afterwards? 
        * Are there courses where we can see the differences between years it rained versus not?

<br>

# Challenges
1. Golf data API was an expensive option for project and had incomplete data for tournament and course details.
2. Scraping ESPN was difficult due to the tournament ID's changing season by season after 2018.  Manual inspection was required to mark tournament ID ranges.
3. Missing data upon scraping for certain tournaments and elements.
4. Weather data required Selenium Web Crawler and proper packages for ARM architecture to be performant. 
5. Handling exceptions for web crawlers for errors like page timeouts, element interception, stale elements, etc.
    Constant ensurance that chromedriver was matching chrome version so latest versions are used for performance
    Observed that after chrome update the chromedriver was not bheaving like it was in a prior week of development. 
6. Preparing weather data so best information is used by considering things like time of tournament play weather versus weather outside tournament time

<br>

# Packages
* Had to create virtual environment for ARM64 architecture for Selenium to be performant
1. Python 3.7
2. Pandas
3. BeautifulSoup
4. Selenium


# Key Troubleshooting Articles
1. How to create env for ARM architecture: 
    https://stackoverflow.com/questions/65415996/how-to-specify-the-architecture-or-platform-for-a-new-conda-environment-apple\
2. Root cause for slow Selenium
    https://stackoverflow.com/questions/76957026/chromedriver-starts-chrome-as-x86-64-translated-on-m1-very-slow-performance

