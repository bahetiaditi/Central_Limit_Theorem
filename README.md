\documentclass{article}
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{caption}
\usepackage{hyperref}

\title{Central Limit Theorem: A Case Study using the Titanic Dataset}
\author{Aditi}

\begin{document}

\maketitle

\section{Introduction}
The Central Limit Theorem (CLT) is one of the most fundamental concepts in statistics. It states that the sampling distribution of the sample mean (or sum) will tend to follow a normal distribution, regardless of the distribution of the population, provided the sample size is sufficiently large. This case study aims to explore the practical implications of CLT using the Titanic dataset, specifically focusing on the `Fare` feature.

\section{Dataset Overview}
The Titanic dataset contains information about passengers on the Titanic. For this study, we focus on the `Fare` column, which represents the fare paid by each passenger. This variable is not normally distributed, as demonstrated by the initial Kernel Density Estimate (KDE) plot of the `Fare` distribution.

\section{Original Fare Distribution}
The first step was to visualize the original distribution of the `Fare` feature. As can be seen from the KDE plot (Fig. 1), the distribution is right-skewed with most passengers paying relatively lower fares, while a few outliers paid very high fares. This distribution is clearly non-normal.

\begin{figure}[h!]
\centering
\includegraphics[width=0.7\textwidth]{file-5YetnEMahcYliEcJLiFqyTtd}
\caption{KDE Plot of Original Fare Distribution}
\end{figure}

\section{Sampling Distribution of Means}
According to the Central Limit Theorem, if we repeatedly take random samples of a fixed size from this population and calculate the sample means, the distribution of these means will approximate a normal distribution, even if the original data is not normally distributed.

For this case study, we took 100 random samples of size 50 from the `Fare` column. Each sample's mean was calculated and plotted alongside the original `Fare` distribution (Fig. 2). 

\begin{figure}[h!]
\centering
\includegraphics[width=0.7\textwidth]{file-1algz5PboBOubbXwKYTUywq6}
\caption{Sampling Distribution of Means vs Original Fare Distribution}
\end{figure}

As the figure shows, the distribution of sample means is much narrower and appears to follow a normal distribution, as predicted by the CLT. The original distribution remains skewed (blue dashed line), but the sample means follow a bell-shaped curve (green solid line).

\section{Histogram of Sample Means}
To further validate the CLT, we plotted a histogram of the sample means (Fig. 3). This plot confirms that the distribution of the sample means is approximately normal, centered around the average fare, with less spread compared to the original fare distribution.

\begin{figure}[h!]
\centering
\includegraphics[width=0.7\textwidth]{file-HsxDiwgQTGvpVpmzGKYqK0jU}
\caption{Histogram of Sample Means}
\end{figure}

\section{Statistical Insights}
From the generated sampling distribution, we computed several key statistics:
\begin{itemize}
    \item \textbf{Mean of Sampling Distribution:} The mean of the sample means is approximately equal to the population mean of the original `Fare` data, which aligns with the CLT prediction.
    \item \textbf{Standard Error:} The standard deviation of the sample means (also called the Standard Error) is much smaller than the standard deviation of the original fare distribution. This reflects the reduced variability in the sampling distribution.
    \item \textbf{Confidence Interval:} A 95\% confidence interval for the mean fare was calculated based on the standard error. The interval suggests that if we repeatedly sampled from this population, the true mean would fall within this range 95\% of the time.
\end{itemize}

\section{Confidence Interval Visualization}
Figure 4 shows the sampling distribution of the means with the 95\% confidence interval marked by red and purple vertical lines. This visualization highlights the range within which we expect the true mean to lie with 95\% confidence.

\begin{figure}[h!]
\centering
\includegraphics[width=0.7\textwidth]{file-fsUEnMmdBO8uEwOlUPkJJgTE}
\caption{Sampling Distribution with Confidence Interval (95\%)}
\end{figure}

\section{Discussion and Conclusion}
The results of this case study reinforce the Central Limit Theorem:
\begin{itemize}
    \item Despite the original `Fare` distribution being highly skewed, the distribution of sample means follows a normal distribution when sufficient samples are taken.
    \item The standard error is lower than the population standard deviation, indicating reduced variability in the sampling distribution.
    \item The confidence interval provides a range where we expect the true population mean to fall, offering insights into how reliable the sample mean is as an estimator of the population mean.
\end{itemize}

The Central Limit Theorem is incredibly powerful for inferential statistics because it allows us to make predictions about the population mean using sample means, even when the population distribution is non-normal. This study demonstrates the practical implications of CLT using real-world data from the Titanic dataset.

\end{document}
