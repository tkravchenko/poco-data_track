# Chapter 1
# Average
1. A **mean** is the sum of all observations in your population or sample divided by the number of observations in that population or sample.
*Example:*
- This is a sample of 10 Japanese ages. Summing the ages, you get 473. Therefore the mean average is 473 divided by 10 or 47.3. Mean reduces information from these 10 observations to one value. Let's compare Japan's average age, 47.3 to Uganda's average age.

2. The **median** is the middle number of a data set. When sorted from smallest to largest half the numbers are less than the median & half the numbers are above the median. 
- The median is more robust to outliers, unlike the mean. So if your dataset has a lot of outliers, the mean will be pulled in the direction of the outliers.
- Recall that for an odd number of observations, a median is the middle value in the data. With an even number of observations, the median is the mean of the two middle values. 
- To manually calculate a median, the data needs to be sorted (unlike if you are using the MEDIAN() function).

3. The **mode** is a number that appears most often in a dataset. This Japanese age sample has 48 listed twice. Thus, the mode average is 48.
- If every value is unique, then there is no mode, and if there is a tie, then the sample can have 2+ modes.

# How far from average?
1. **Variance** measures how dispersed a dataset is from its mean. The smaller the variance, the less spread the data is. Conversely, large differences between data points increase the variance.
- That is, how far from the mean each point is.
- As a reminder, to calculate the variance of a population:
    1. Calculate the mean of the entire dataset.
    2. Subtract each value from the mean.
    3. Square the differences to ensure positive and negative values don't cancel each other out.
    4. Take the average of the squared differences.

2. Next stop Standard Deviation! Keep in mind variance is the average of squared values. Thus the variance is different from the original sample values making it less intuitive! Most often you will need to make sense of the variation by putting it in the scale of the original data. This is done by taking the square root of the variance, called **standard deviation**
- Next stop Standard Deviation! Keep in mind variance is the average of squared values. Thus the variance is different from the original sample values making it less intuitive! Most often you will need to make sense of the variation by putting it in the scale of the original data. This is done by taking the square root of the variance, called standard deviation.
- Standard scores show you how a data point relates to the distribution. 

3. Another statistic for understanding a distribution is a **percentile**. Ordering a distribution & calculating the percentage of values below a specific point will tell you its percentile. 
- **Quartiles** are percentiles that segment the data into 4 chunks. 

4. The QUARTILE() function accepts an array of values followed by an integer 1 to 4 to declare the specific quartile.
- Quartile 4: The maximum value in the data.
- Quartile 3: 75% of the data is less than the third quartile.
- Quartile 2: The median of the data.
- Quartile 1: The smallest values 25% of the data.
- A useful statistic computed from the quartiles is the "interquartile range" (IQR), which lies between the Q1 and Q3 and represents the middle 50% of the data.

# Standardizing data
1. Why standardize?
- variables are measured on different scales. For example, height might be measured in feet, while weight might be measured in pounds. 
- harder to compare
- may lead you to misinterpret the importance of a particular column 
- The solution: standardize your data so that all your variables are on the same scale.

2. In statistics, standardization centers a dataset's distribution around the mean of the data and calculates the number of standard deviations away from the mean each point is. You can standardize your data **by calculating z-scores**, also known as standard scores. Z-scores are an extension of what you've already seen in this chapter. To calculate the z-score of a data point, subtract the mean and divide by the standard deviation.

________________________________________________________________________________________________
# Chapter 2
# Visualizing distribution
1. **Standard distribution**:
 - In both cases, the highest point is in the middle of the distribution. Put another way, the most frequent value is the highest point. 
 - The curve here is symmetrical meaning it flows to either side of the point. 
 - The resulting shape is similar to a bell so this distribution is often called a bell curve. In fact, a bell curve is so common it is technically called the "normal distribution".
 - As a result, not only is the distribution centered at the mean, median and mode but the frequencies of these values decrease symmetrically so other summary stats are affected like quartiles and standard deviations.

2. Other distributions:
- So in a **"skewed"** distribution, these values will differ, unlike the normal or symmetrical distribution where mean and median are very close. As you get more familiar with summary statistics you'll be able to spot a non-normal distribution by reviewing the stats instead of in a histogram.
- These aspects, leaning & trailing off, are measured in "skew" and "kurtosis". In sheets use `skew` &`kurt` along with the data range to get leaning and trailing off statistics.Перекос/Эксцесс

# Visualiying correlations

Its named **scatterplot** because each dot represents a row in your data and the points often appear to be scattered along the coordinates. A scatterplot is great because your brain can identify patterns among the two variables.

Recall that **correlation**, which you can calculate using CORREL(), ranges between -1 and 1.
- 0 correlation means there is no relationship between variables.
- Positive correlation indicate that as one variable increases, the other also increases.
- Negative correlation values signify that as one variable increases, the other decreases.

Spreadsheets have 3 formulas for calculating the y-intercept and slope given two variables.
- SLOPE() - will return the slope of a trend line or linear regression representing the linear change in one unit to another.//нахил
- INTERCEPT() - returns the value where the trendline will intersect the y-axis.
- LINEST() - calculates both the slope & the intercept of two variables using the least-squares method.

# Bar charts
Types of data:
- numeric;
- categorigal => use bar charts to visualize.

Types of bar charts:
- **Stacked**: helps you focus on the proportion of the total that is a particular class. You will visually understand the amount of the total that represents competitive online auctions.
- **Side-by-side**: lets the audience understand the values in relation to each other. You will visually interpret how similar each class values are

________________________________________________________________________________________________
# Chapter 3 Statistical Hypothesis Testing
# Central to Stats: Sampling!

In stats, a **population** is defined as an *entire* distribution of similar observations or events. Suppose you want to know how everyone riding trains feels about a rate hike. You could ask the *entire* population but this could be costly & time consuming. As a result, more often statisticians work with data samples.

A **sample** is a subset of the population's observations. It is meant to represent the characteristics of the population. As your sample increases, the statistical information will more closely approximate the population's stats.

**Central Limit Theorem (CLT)** :If a sample size from an independent, random variable is **large enough** then the sampling distribution will be normal or nearly normal.

 For some practical inferential statisticians, if the underlying population is normal they would say **a sample of 30 to 40** would be sufficient to make inferences about the population.

 **"Large enough"** is vague. The sample size is impacted by:
- How accurate you need to be. Since a sample is a representation, the resulting stats will be approximate. If you need a high degree of certainty, you will need more samples to more closely resemble the population.
- The more closely the population follows a normal distribution, the fewer sample points will be required.