#### Problem
By use of the logistic regression equation of vehicle transmission in the data set mtcars, estimate the probability of a vehicle being fitted with a manual transmission if it has a 120hp engine and weights 2800 lbs.

#### Solution
We apply the function glm to a formula that describes the transmission type (am) by the horsepower (hp) and weight (wt). This creates a generalized linear model (GLM) in the binomial family.

<pre><code>
> am.glm = glm(formula=am ~ hp + wt, 
+              data=mtcars, 
+              family=binomial)
</code></pre>
We then wrap the test parameters inside a data frame newdata.

<pre><code>
> newdata = data.frame(hp=120, wt=2.8)
</code></pre>
Now we apply the function predict to the generalized linear model am.glm along with newdata. We will have to select response prediction type in order to obtain the predicted probability.
<pre><code>
> predict(am.glm, newdata, type="response") 
      1 
0.64181
</code></pre>
#### Answer
For an automobile with 120hp engine and 2800 lbs weight, the probability of it being fitted with a manual transmission is about 64%.

#### Note
Further detail of the function predict for generalized linear model can be found in the R documentation.
<pre><code>
> help(predict.glm)
</code></pre>
