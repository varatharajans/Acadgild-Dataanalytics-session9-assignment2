# Acadgild-Dataanalytics-session9-assignment2
DATA ANALYTICS WITH R, EXCEL AND TABLEAU SESSION 9ASSIGNMENT 2

Assignment 9.2
1.	Calculate the P Value for the test in Problem 2. 
2.	How do you test the proportions and compare against hypothetical props?    Test Hypothesis: proportion of automatic cars is 40%.

 HYPOTHESIS TESTING Or do we? Clearly, for some significance levels we reject, and for some significance levels we do not. Where is the boundary?
 That is, what is the significance level for which we would reject at any significance level bigger, and we would fail to reject at any significance level smaller? This boundary value has a special name: it is called the p-value of the test. 
 1-sample proportions test without continuity correction data: 1755 out of 1755 + 2771, null probability 0.4 X-squared = 2.8255, df = 1, p-value = 0.04639 3
pnorm(-1.680919)
## [1] 0.04638932
Bickel and Doksum [7] state the definition particularly well: the p-value is “the smallest level of significance α at which an experimenter using [the test statistic] T would reject [H0] on the basis of the observed [sample] outcome x”.
 ONE SAMPLE TESTS FOR MEANS AND VARIANCES 235
 alternative hypothesis: true p is less than 0.4 99 percent
 confidence interval: 0.0000000 0.4047326 
sample estimates: p 0.3877596 
prop.test(1755, 1755 + 2771, p = 0.4, alternative = "less", conf.level = 0.99, correct = FALSE)
## 
##  1-sample proportions test without continuity correction
## 
## data:  1755 out of 1755 + 2771, null probability 0.4
## X-squared = 2.8255, df = 1, p-value = 0.04639
## alternative hypothesis: true p is less than 0.4
## 99 percent confidence interval:
##  0.0000000 0.4047326
## sample estimates:
##         p 
## 0.3877596

Do the following to make the plot.
 > library(IPSUR) > library(HH)
 > temp <- prop.test(1755, 1755 + 2771, p = 0.4, alternative = "less", + conf.level = 0.99, correct = FALSE) > plot(temp, "Hypoth")
## library(IPSUR)
library(HH)
plot(prop.test(1755, 1755 + 2771, p = 0.4, alternative = "less", conf.level = 0.99, correct = FALSE), 'Hypoth')
 

x <- rnorm(37, mean = 2, sd = 3)
library(TeachingDemos)
z.test(x, mu = 1, sd = 3, conf.level = 0.90)
## 
##  One Sample z-test
## 
## data:  x
## z = 2.8126, n = 37.0000, Std. Dev. = 3.0000, Std. Dev. of the
## sample mean = 0.4932, p-value = 0.004914
## alternative hypothesis: true mean is not equal to 1
## 90 percent confidence interval:
##  1.575948 3.198422
## sample estimates:
## mean of x 
##  2.387185

library(HH)
plot(prop.test(1755, 1755 + 2771, p = 0.4, alternative = "less", conf.level = 0.99, correct = FALSE), 'Hypoth')

 

 Use Yates’ continuity correction when the expected frequency of successes is less than 10. You can use it all of the time, but you will have a decrease in power. For large samples the correction does not matter. With the R


