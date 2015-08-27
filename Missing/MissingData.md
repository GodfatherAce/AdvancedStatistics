Missing Data
===================================== 
Missing data are a part of almost all research, and we all have to decide how to deal with it from time to time. There are a number of alternative ways of dealing with missing data, and this document is an attempt to outline those approaches. The original version of this document spent considerable space on using dummy variables to code for missing observations. That idea was popularized in the behavioral sciences by Cohen and Cohen (1983). However, that approach does not produce unbiased parameter estimates (Jones, 1996), and is no longer to be recommended--especially in light of the availability of excellent software to handle other approaches. 

###1.1 The nature of missing data

#### Missing completely at random

There are several reasons why the data may be missing. They may be missing because equipment malfunctioned, the weather was terrible, or people got sick, or the data were not entered correctly. Here the data are missing completely at random (MCAR). When we say that data are missing completely at random, we mean that the probability that an observation (Xi) is missing is unrelated to the value of Xi or to the value of any other variables. Thus data on family income would not be considered MCAR if people with low incomes were less likely to report their family income than people with higher incomes. Similarly, if Whites were more likely to omit reporting income than African Americans, we again would not have data that were MCAR because missingness would be correlated with ethnicity. However if a participant's data were missing because he was stopped for a traffic violation and missed the data collection session, his data would presumably be missing completely at random. Another way to think of MCAR is to note that in that case any piece of data is just as likely to be missing as any other piece of data.

Notice that it is the value of the observation, and not its "missingness," that is important. If people who refused to report personal income were also likely to refuse to report family income, the data could still be considered MCAR, so long as neither of these had any relation to the income value itself. This is an important consideration, because when a data set consists of responses to several survey instruments, someone who did not complete the Beck Depression Inventory would be missing all BDI subscores, but that would not affect whether the data can be classed as MCAR. 

This nice feature of data that are MCAR is that the analysis remains unbiased. We may lose power for our design, but the estimated parameters are not biased by the absence of data.

#### Missing at random

Often data are not missing completely at random, but they may be classifiable as missing at random (MAR). For data to be missing completely at random, the probability that Xi is missing is unrelated to the value of Xi or other variables in the analysis. But the data can be considered as missing at random if the data meet the requirement that missingness does not depend on the value of Xi after controlling for another variable. 

For example, people who are depressed might be less inclined to report their income, and thus reported income will be related to depression. Depressed people might also have a lower income in general, and thus when we have a high rate of missing data among depressed individuals, the existing mean income might be lower than it would be without missing data. However, if, within depressed patients the probability of reported income was unrelated to income level, then the data would be considered MAR, though not MCAR.

The phraseology is a bit awkward here because we tend to think of randomness as not producing bias, and thus might well think that Missing at Random is not a problem. Unfortunately is is a problem, although in this case we have ways of dealing with the issue so as to produce meaningful and relatively unbiased estimates. But just because a variable is MAR does not mean that you can just forget about the problem.

#### Missing Not at random

If data are not missing at random or completely at random then they are classed as Missing Not at Random (MNAR). For example, if we are studying mental health and people who have been diagnosed as depressed are less likely than others to report their mental status, the data are not missing at random. 

Clearly the mean mental status score for the available data will not be an unbiased estimate of the mean that we would have obtained with complete data. The same thing happens when people with low income are less likely to report their income on a data collection form.

When we have data that are MNAR we have a problem. The only way to obtain an unbiased estimate of parameters is to model missingness. In other words we would need to write a model that accounts for the missing data. That model could then be incorporated into a more complex model for estimating missing values. This is not a task anyone would take on lightly. See Dunning and Freedman (2008) for an example.

<hr>
### 1.2 The simplest approach--listwise deletion.

By far the most common approach is to simply omit those cases with missing data and to run our analyses on what remains. Thus if 5 subjects in group one don't show up to be tested, that group is 5 observations short.  Or if 5 individuals have missing scores on one or more variables, we simply omit those individuals from the analysis. This approach is usually called listwise deletion, but it is also known as complete case analysis. 

Although listwise deletion often results in a substantial decrease in the sample size available for the analysis, it does have important advantages. In particular, under the assumption that data are missing completely at random, it leads to unbiased parameter estimates. Unfortunately, even when the data are MCAR there is a loss in power using this approach. And when the data are not MCAR, bias results. 

(For example when low income individuals are less likely to report their income level, the resulting mean is biased in favor of higher incomes.) The alternative approaches discussed below should be considered in as a replacement for listwise deletion, though in some cases we may be better off to "bite the bullet" and fall back on listwise deletion.

### 1.3 A poor approach--pairwise deletion

Many computer packages offer the option of using what is generally known as pairwise deletion but has also been called "unwise" deletion. Under this approach each element of the intercorrelation matrix is estimated using all available data. If one participant reports his income and life satisfaction index, but not his age, he is included in the correlation of income and life satisfaction, but not in the correlations involving age. 

The problem with this approach is that the parameters of the model will be based on different sets of data, with different sample sizes and different standard errors. It is even quite possible to generate an intercorrelation matrix that is not positive definite, which is likely to bring your whole analysis to a stop.

It has been suggested that if there are only a few missing observations it doesn't hurt anything to use pairwise deletion. But I would argue that if there are only a few missing observations that it doesn't hurt much to toss those participants out and use complete cases. If there are many missing observations you can do considerable harm with either analysis. In both situations the approaches given below are generally preferable.

 <hr>




