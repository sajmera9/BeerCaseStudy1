# Doing Data Science - Case Study 01: Using the Beer and Breweries Datasets
## By: Satvik Ajmera and Rob Burigo

[Link to Github Repository](https://github.com/sajmera9/BeerCaseStudy1)


## Answers to Analysis Questions


### 1.   How many breweries are present in each state?

For this question, we decided to focus on the top ten states with the most breweries. We found that Colorado has the most breweries with 47, followed by California with 39 breweries, and Michigan with 32 breweries. Here is the plot we created:

![Top Ten States with the Most Breweries!](Visualizations/Top10BreweriesPerState.png)

### 2.   Merge beer data with the breweries data. Print the first 6 observations and the last six observations to check the merged file.  (RMD only, this does not need to be included in the presentation or the deck.)

 To successfully merge the `beer.csv` and `breweries.csv` , we merged on the unique identifier columns that were in both datasets called `Brewery_id` and `Brew_ID`. Lastly, we concatenating first and last six observations into one dataframe called `head_tail_merge`. Here is a screenshot of what that dataframe looks like:

![First and Last Six Observations!](Visualizations/MergeFirstAndLast6.png)


### 3.   Address the missing values in each column.

Using the `naniar` library in R, we found that there are 62 missing values for ABV and 1005 missing values for IBU after merging the both datasets. Going forward, we decided to drop all these NA values. We created a visualization of the missing values in column to visually compare them.

![Missing Values Plot!](Visualizations/MissingValuesPlot.png)



### 4.   Compute the median alcohol content and international bitterness unit for each state. Plot a bar chart to compare.

Using a `group_by()`, and `summarize()` we were able to compute the median ABV and median IBU per state. For our visualization, we wanted to focus on the top ten states with greatest median ABV. We found the top 9 states have a median ABV over **5.5%**
![Top Ten Median ABV!](Visualizations/MedianABVPerState.png)


### 5.   Which state has the maximum alcoholic (ABV) beer? Which state has the most bitter (IBU) beer?

### 6.   Comment on the summary statistics and distribution of the ABV variable.

###  7.   Is there an apparent relationship between the bitterness of the beer and its alcoholic content? Draw a scatter plot.  Make your best judgment of a relationship and EXPLAIN your answer.

### 8.  Budweiser would also like to investigate the difference with respect to IBU and ABV between IPAs (India Pale Ales) and other types of Ale (any beer with “Ale” in its name other than IPA).  You decide to use KNN classification to investigate this relationship.  Provide statistical evidence one way or the other. You can of course assume your audience is comfortable with percentages … KNN is very easy to understand conceptually.

### In addition, while you have decided to use KNN to investigate this relationship (KNN is required) you may also feel free to supplement your response to this question with any other methods or techniques you have learned.  Creativity and alternative solutions are always encouraged.  

### 9. Knock their socks off!  Find one other useful inference from the data that you feel Budweiser may be able to find value in.  You must convince them why it is important and back up your conviction with appropriate statistical evidence. 
