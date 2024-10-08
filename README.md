# Central Limit Theorem: A Case Study using the Titanic Dataset

## Introduction
The **Central Limit Theorem (CLT)** is one of the most fundamental concepts in statistics. It states that the sampling distribution of the sample mean (or sum) will tend to follow a normal distribution, regardless of the population's original distribution, provided the sample size is sufficiently large. 

This case study explores the practical implications of CLT using the Titanic dataset, focusing on the `Fare` feature.

## Dataset Overview
The Titanic dataset contains information about passengers on the Titanic. For this study, we focus on the `Fare` column, representing the fare paid by each passenger. Initially, we visualize the distribution of fares to understand its characteristics.

## Original Fare Distribution
The KDE plot below shows the original distribution of the `Fare` feature. It is heavily right-skewed, meaning most passengers paid relatively low fares, while a few paid much higher amounts. This distribution is clearly **non-normal**.

![KDE Plot of Original Fare Distribution](Images/KDE_Fare_Dist.png)

## Sampling Distribution of Means
According to the Central Limit Theorem, if we repeatedly take random samples from a population and calculate their means, the distribution of these means will approximate a **normal distribution**. 

For this study, we took 100 random samples of size 50 from the `Fare` column and calculated their means. The plot below compares the **sampling distribution of means** (green line) with the original fare distribution (blue dashed line).

![Sampling Distribution of Means vs Original Fare Distribution](file-1algz5PboBOubbXwKYTUywq6)

As shown, the distribution of sample means is narrower and approximates a **normal distribution**, even though the original data is skewed.

## Histogram of Sample Means
To visualize the Central Limit Theorem further, we plotted a histogram of the sample means. As seen below, the distribution of the sample means is approximately normal and centered around the population mean.

![Histogram of Sample Means](file-HsxDiwgQTGvpVpmzGKYqK0jU)

## Statistical Insights
From the sampling distribution, we calculated key statistics:
- **Mean of the Sampling Distribution**: The mean of the sample means is close to the population mean, as expected according to the Central Limit Theorem.
- **Standard Error**: The standard deviation of the sample means, or standard error, is much smaller than the population standard deviation, reflecting reduced variability.
- **Confidence Interval (95%)**: Using the sample means, we calculated a 95% confidence interval for the mean fare. This interval represents the range where we expect the true population mean to fall 95% of the time.

## Confidence Interval Visualization
In the plot below, we visualize the 95% confidence interval for the mean fare, showing the lower and upper bounds with vertical lines (red and purple, respectively). This highlights the range where we expect the true population mean to fall.

![Sampling Distribution with Confidence Interval](file-fsUEnMmdBO8uEwOlUPkJJgTE)

## Discussion and Conclusion
The results of this case study reinforce the Central Limit Theorem:
- Even though the original `Fare` distribution is heavily skewed, the **distribution of sample means** is **approximately normal** when enough samples are taken.
- The **standard error** is lower than the population's standard deviation, meaning there is less variability in the sample means.
- The **confidence interval** provides a range where we expect the true population mean to lie, offering a reliable estimate of the population mean.

The Central Limit Theorem is fundamental to inferential statistics as it allows us to make predictions about the population mean using sample means, even when the population distribution is non-normal. This case study demonstrates the practical implications of the CLT using real-world data from the Titanic dataset.

