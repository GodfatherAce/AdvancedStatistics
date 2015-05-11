Non Parametric Statistics with R
======================================
A statistical method is called non-parametric if it makes no assumption on the population distribution or sample size.

This is in contrast with most parametric methods in elementary statistics that assume the data is quantitative, the population has a normal distribution and the sample size is sufficiently large.

In general, conclusions drawn from non-parametric methods are not as powerful as the parametric ones. 
However, as non-parametric methods make fewer assumptions, they are more flexible, more robust, and applicable to non-quantitative data.

### Sign Test

A sign test is used to decide whether a binomial distribution has the equal chance of success and failure.

#### Example
A soft drink company has invented a new drink, and would like to find out if it will be as popular as the existing favorite drink. For this purpose, its research department arranges 18 participants for taste testing. Each participant tries both drinks in random order before giving his or her opinion.

#### Problem
It turns out that 5 of the participants like the new drink better, and the rest prefer the old one. At .05 significance level, can we reject the notion that the two drinks are equally popular?

#### Solution
The null hypothesis is that the drinks are equally popular. Here we apply the binom.test function. As the p-value turns out to be 0.096525, and is greater than the .05 significance level, we do not reject the null hypothesis.

<pre><code>
> binom.test(5, 18) 
 
        Exact binomial test 
 
data:  5 and 18 
number of successes = 5, number of trials = 18, 
p-value = 0.09625 
alternative hypothesis: true probability of success is not equal to 0.5 
95 percent confidence interval: 
 0.09695 0.53480 
sample estimates: 
probability of success 
               0.27778
</code></pre>               
#### Answer
At .05 significance level, we do not reject the notion that the two drinks are equally popular.

### Wilcoxon Signed-Rank Test

Two data samples are matched if they come from repeated observations of the same subject. Using the Wilcoxon Signed-Rank Test, we can decide whether the corresponding data population distributions are identical without assuming them to follow the normal distribution.

#### Example
In the built-in data set named immer, the barley yield in years 1931 and 1932 of the same field are recorded. The yield data are presented in the data frame columns Y1 and Y2.
<pre><code>
> library(MASS)         # load the MASS package 
> head(immer) 
  Loc Var    Y1    Y2 
1  UF   M  81.0  80.7 
2  UF   S 105.4  82.3 
    .....
</code></pre>    
Problem
Without assuming the data to have normal distribution, test at .05 significance level if the barley yields of 1931 and 1932 in data set immer have identical data distributions.

#### Solution
The null hypothesis is that the barley yields of the two sample years are identical populations. To test the hypothesis, we apply the wilcox.test function to compare the matched samples. For the paired test, we set the "paired" argument as TRUE. As the p-value turns out to be 0.005318, and is less than the .05 significance level, we reject the null hypothesis.
<pre><code>
> wilcox.test(immer$Y1, immer$Y2, paired=TRUE) 
 
        Wilcoxon signed rank test with continuity correction 
 
data:  immer$Y1 and immer$Y2 
V = 368.5, p-value = 0.005318 
alternative hypothesis: true location shift is not equal to 0 
 
Warning message: 
In wilcox.test.default(immer$Y1, immer$Y2, paired = TRUE) : 
  cannot compute exact p-value with ties
</code></pre>     
#### Answer
At .05 significance level, we conclude that the barley yields of 1931 and 1932 from the data set immer are nonidentical populations.

### Mann-Whitney-Wilcoxon Test

Two data samples are independent if they come from distinct populations and the samples do not affect each other. Using the Mann-Whitney-Wilcoxon Test, we can decide whether the population distributions are identical without assuming them to follow the normal distribution.

#### Example
In the data frame column mpg of the data set mtcars, there are gas mileage data of various 1974 U.S. automobiles.

> mtcars$mpg 
 [1] 21.0 21.0 22.8 21.4 18.7 ...
Meanwhile, another data column in mtcars, named am, indicates the transmission type of the automobile model (0 = automatic, 1 = manual). In other words, it is the differentiating factor of the transmission type.

> mtcars$am 
 [1] 1 1 1 0 0 0 0 0 ...
In particular, the gas mileage data for manual and automatic transmissions are independent.

#### Problem
Without assuming the data to have normal distribution, decide at .05 significance level if the gas mileage data of manual and automatic transmissions in mtcars have identical data distribution.

#### Solution
The null hypothesis is that the gas mileage data of manual and automatic transmissions are identical populations. To test the hypothesis, we apply the wilcox.test function to compare the independent samples. As the p-value turns out to be 0.001817, and is less than the .05 significance level, we reject the null hypothesis.

> wilcox.test(mpg ~ am, data=mtcars) 
 
        Wilcoxon rank sum test with continuity correction 
 
data:  mpg by am 
W = 42, p-value = 0.001871 
alternative hypothesis: true location shift is not equal to 0 
 
Warning message: 
In wilcox.test.default(x = c(21.4, 18.7, 18.1, 14.3, 24.4, 22.8,  : 
  cannot compute exact p-value with ties
Answer
At .05 significance level, we conclude that the gas mileage data of manual and automatic transmissions in mtcar are nonidentical populations.

