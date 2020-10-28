# Begginers-guide
Idea is to going back to basics and understand the fundamentals. I have made an attempt to simplify the concepts which can help the beginners in learning fast.



---

The art of Exploratory data analysis (EDA)

What is Exploratory Data Analysis (EDA)?
As the name suggest, it is a technique to analyse the data by exploring it. EDA is one of the key as well as indispensable step in data analysis. This can be understood as a general checkup of patient (data) by the doctors (data enthusiast), before doing any surgery (analysis, modeling, prediction, classification, etc.).
What are the goals of EDA?
EDA is done for two major underlying reasons, firstly to understand the data and secondly to identify faults or peculiar events (data points) in the dataset. Let's try to understand what is meant by understanding and peculiar data points in detail.
- To understand the data characteristics → Understanding the data means answering following preliminary questions that generally pops up in the mind of data person on first encounter with a particular dataset:
Where is this data coming from? (What population group or subject)
What is the high level contained information? (e.g cost data, revenue, budget, employee salaries, customer data, usage data and so on.)
What are the variables available?
What does their value mean? (e.g average time per page would mean that out of all the time spent by user on the website in one session, how much time was spent on a every particular page)
What population segment data belong to? (e.g The data of cancer patient would meant that out of all patients the collected data is of cancer patients only.
What is the Sample distribution?
What is the strength and direction of the relationships among input variable and outcome variable?
What is the Central tendency of the data?
What is the spread of the data?

- To identify discrepancies in the data → Discrepancies in data means
Presence of incorrect values
Missing values
Outliers (probable outliers or possible outliers)
Assumption violations

Based on the findings during EDA, a preliminary selection of the data can be done or the further course of actions can be decided to treat discrepancies.
Part I - Categorical variables EDA
How EDA is carried out?
As we have seen what and why of EDA, it time to answer how EDA is done? In this post we are going to focus on EDA techniques for categorical variables which includes ordinal, dichotomous and nominal variables. You can find details of types of variable here.
EDA can be graphical or quantitative depending on what are we trying to find. Following previous analogy of patient, reports like x-ray, MRI, scans, can be seen as graphical method which provides overall picture of data and involves qualitative analysis. Whereas blood reports, dimensions of tumour can be understood as quantitative method which are objective.
In general data is constitute of several columns and rows. Now one can choose to explore one variable at a time (uni+variate=univariate), two variables at a time (bi+variate=bivariate), or multiple variables at same time (multi+variate= multivariate).
Tips data frame

---

Univariate categorical EDA
Univariate-Quantitative EDA:
The most useful information that can be extracted from this analysis in context to the categorical variable, is to know the categories, frequency of occurrence, proportion or percentage of data falls under each category. Frequency tables are the most popular way of doing this analysis.
Frequency Table of Total number of smokers and non-smokersUnivariate-Graphical EDA:
When we think graphs, bar plots are one of the most widely used graphs. A similar information from frequency tabulation can also be attained in form of bar plots, which are more useful in presenting the analysis. Having able to present the information in visual form is one of the key element in effectively presenting the analysis.
Bar plot to show total number of reservation on particular weekday

---

Multivariate Categorical EDA
Multivariate-Quantitative EDA:
Cross tabulation: Cross-tabulation is the basic bivariate non-graphical EDA technique. However, it is not limited to the bivariate, but can be extended further. Reason why more than 5-way cross tables are not very popular is because it becomes a little hard to apprehend as the cross tabulation grows.

3-way cross tabulation2. Univariate statistics per category: In case we have one categorical input variable and one quantitative outcome variable, generally the outcome variable statistics are calculated for each category and after that compare the statistics across the categories. The comparison is done using statistical tests such as anova.
Multivariate-graphical EDA:
Side-by-Side Box-plots: In case we want to explore categorical input variable and quantitative output variable, the approach is to separate all the cases based on categories and then make box plots of output variable. Side by side box-plots are useful in investigating the relationship between categorical and quantitative variable. In addition to it, distribution of outcome variable can also be seen at each categorical variable level.

EDA can bring enough understanding and knowledge to make aware decisions. However, one should not mistake EDA as an initial phase or one step process. As we progress with the data science cycle, one might need to do some EDA again after obtaining the results to analyse why the model is behaving in certain way or why a certain kind of output is seen. It wouldn't be wrong to see EDA as process than as a phase. 
Part I describes Categorical variable EDA in depth.


---

Part I I - Quantitative variables EDA
The sample statistics are accessed using the quantitative variables, which can be used to paint initial picture of population distribution. The distribution of population is characterised by the central tendency, dispersion, asymmetry, peakedness. In addition to that strength and direction of direct relationship between input variables and outcome variable, outliers, covariance, and correlation are also checked.
Univariate Quantitative EDA
Univariate-Quantitative EDA: 
Exploratory data analysis for quantitative variable majorly evaluation the distribution of variable in a given dataset. To do so, one might be interested in center of mass of data, variance in data, variable relationships, etc.
Tips datasetDescriptive statistics of the datasetMeasure of central tendency: When we measure the central tendency of a sample, we essentially are trying to identify the "center of mass" of values. In simple terms around what point most of the middle value resides. To measure central tendency arithmetic mean(generally), median and mode is calculated.
Mean: In most of the case arithmetic mean is of interest. By calculating mean, we try to find out the number which can smooth the fluctuation in the dataset. 
Let's solve a quick puzzle: if we have three jars filled with {6,9,3} liters of water respectively, How to redistribute the water so that each jar have same liters of water. One simple and quick way is to take 3 ltr of water from second jar and add it to the third jar, so that every jar will have 6 ltr of water. This is relatively easy! The easy problem gets tougher when the dataset size increases massively and therefore we need a formula.

Bar plot of water quantity in each jar
Mean/Average=sum of all data points/count of all data points
Mean and data distributionSo what we did by redistribution or calculating average, is that even the individual numbers were varying a lot from each other, when we redistribute the values, 6 is the value that will remove the fluctuations. Two important points to note here, firstly, the mean tell more about the whole data set than individual values and secondly, mean is directly and highly influenced by the outlier values.
Median: This is the point which divides the data set into two equal half such that one set of the values will always be smaller than the median and other half will be bigger than the median. This means that median is unaffected by the outliers and hence better measure of central tendencies in case the data is highly skewed (asymmetric distribution). In case of normal distribution the mean and median values coincides.
Mode: Mode measure the most frequent values from the dataset. Mode is more useful when the interest is in knowing which categories are more frequent and is of little use in case of continuous dataset (reason → multi-modal distribution)

Mean, Median, Mode change as per distribution. sourceTo summarise the central tendency, the mean is most preferred as it represents the characteristics of entire dataset . In case of data skewed left or right( shown in above image) median is preferred. 
A quick formula:
Mean=Median=Mode → Normal distribution
Mean > Mode → positive skewed distribution
Mean<Mode → Negatively skewed distribution
Measure of central tendency of dataset TipsMeasure of dispersion: Measure of dispersion/spread describes the variance in the data, which means how far away from mean, the data points are spread . In association with measure of central tendency, the measure of variance is of great value. It shows how well the measure of central tendency is representative of the data. 
Range: It is one of the basic and most intuitive measure of spread. Range is the difference between lowest and highest value from the data set which defines the boundary of the data. It has limited use unless there are some critical boundary violation check is of interest.
Variance: To represent the spread of data, variance uses squared absolute deviation ,divided by the sample size. As a result only positive number is achieved. 
If datapoints is spread out wide → Variance will be higher (large number)
If datapoints are close to mean →Variance will be smaller (small number).
However, variance can be tricky in presence of outliers. Firstly, due to squared absolute deviation outliers/extreme values gets more weight. Secondly, the squared unit causes variance to appear arbitrary number and hard to interpret.
Standard variance/deviation: The second problem of variance is solved by taking the square root of variance and result is standard deviation. Low standard deviation means that data points are closer to the mean and high standard deviation signify the data points are spread across the wide range.
Interquartile Range: Similar to idea of median, the data set is first divided into 4 quartiles and difference between third and first quartile is calculated. Quartiles are interesting measure as they are robust to outliers/skewed data unlike variance, standard deviation and mean.

Graphical representation of IQR. sourceSkewness and Kurtosis: Skewness and kurtosis describes the given data distribution's asymmetry (skewness) and peakiness (kurtosis), in context to Gaussian distribution or the bell curve.
Graphical representation of skewed and kurtotic distribution. sourceDensity graph of variable total_billUnivariate-Graphical EDA:
Histograms: One of the quickest and most popular way to access the distribution of data is histograms. Below is the histogram of tip from the tips dataset. As can be seen from the histogram the data is positively skewed.
Histogram of the variable (total_bill)Box-plots: Box plots are extremely useful to identify the outliers, symmetry, central tendency, and skewness. It applies the same principle of interquartile range (IQR). For a dataset with normal distribution, the median divides the box in approximately equal sizes. However in case of skewed data, size of box will not be equal. Size of box tells the story, if right side box (upper box) from median is bigger, data is positive skewed. Box-plots are good measure of variability in case of skewed data as IQR takes account of data between Q1 and Q3 and ignore the part having outliers. 
Boxplot for variable total_billQuantile -Quantile Plot: Q-Q plot compares the data distribution against the normal distribution and helps in identifying non-normality, skewness, kurtosis, multimodality. The plot looks similar to scatter plot which is plotted between the observed or recorded value against expected/theoretical values (as per normal distribution).


---

Multivariate Quantitative EDA
Multivariate-Quantitative EDA:
Correlation: Correlation evaluates the direction as well as strength of a relationship between continuous variables. Correlation coefficient can range from -1 to +1, which signifies strong negative to strong positive relation between the variables. Correlation=0, suggests that two variables are independent of each other. A positive correlation point towards the positive relationship between two variables, which means if one variable a changes the second variable also changes is same direction(increase or decrease).
Graphical representation of Correlation between two variables. source


Correlation matrix of dataframe tips
Correlations direction and magnitude are very important while selection variable. As for every strong correlation the causation should be investigated. Additionally, in case of modeling strongly correlated variables should be treated appropriately.
Multivariate-Graphical EDA:
Scatter plots: Scatter plots are generally plot between the input variable (x-axis) vs outcome variable (y-axis). Scatter plots visually gives idea of how two variables are changes with respect to each other. Additionally, one can also add categories which can be represented by various colours as well as shapes of points.
pair plot of all quantitative variables.

