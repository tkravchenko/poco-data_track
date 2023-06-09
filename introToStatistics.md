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