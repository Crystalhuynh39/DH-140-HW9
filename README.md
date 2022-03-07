# DH-140-Assignment 9

This notebook contains Assignment 5: Web Scraping from DH 140 Coding for Humanities with Professor Winjum.

To get an interactive version of this, click here: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Crystalhuynh39/DH-140-HW9/HEAD)

## Step 1
#### Use requests and BeautifulSoup to make a list of all the CORGIS datasets.

I looked for h3 tags on the webpage with all the CORGIS datasets and got a list of all the dataset titles on the page.

## Step 2
#### Write a function that takes an element from the list of CORGIS datasets, searches the respective CORGIS page for the CSV download link, and returns a Pandas dataframe.

I wrote a function called pdcorgis and then tested it with the Classics dataset to make sure it returns a dataframe. In thie function, I coverted the element to lowercase, used request to grab the respective site's HTML, and used BeautifulSoup to find all the link elements on the page. I then wrote a for loop which would check if the links were downloadable, grabbed the link for the csv file, and returned corgisdf which is the value returned by pd.read_csv() with the download link.

## Step 3
#### Using dataframes returned by your new function, make a line plot, a bar plot, and a histogram plot

I used the function I wrote to make three plots using three different datasets.

For the Graduates dataset, I wanted to make a line graph that showed the mean salaries for economics Major graduates over the years to see how much they were making and whether or not econommics was a decent major to study for a future career.

For the Ingredients dataset, I wanted to make a bar chart to look at how much sugar was in different kinds of pies to compare them and determine which type of pie was the unhealthiest based on sugar level.

For the Broadway dataset, I wanted to make a histogram to compare theater capacity for the Beauty and the Beast show for venue booking purposes if I was an organizer for the performance. This would tell show me how popular the show was and how big of a venue I would need to book to make the most money without losing too many seats.