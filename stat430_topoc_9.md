# Topic 9 Statistical Testing
## 1. Introduction
Hypothesis testing is the process of using sample data to test a claim about the value of a population parameter
## 2. P-value and alpha
- If p_value <= $\alpha$, we reject H0
- If p_value >= $alpha$, we fail to reject h0

### notes:
The P-value is a statement about the probability that the sample mean takes on specific values.

It is not a statement about the probability that the population mean has a certain value.

It is not a statement about the probability that the null hypothesis is true.
## Type I and II error
### Type I error: Reject H0 while H0 is true

If the null hypothesis is true and alpha = 0.05
- There really is no relationship and the extremity of the test statistic is due to chance.
- About 5% of all samples from this population will lead us to wrongly reject chance and conclude significance.

### Type II error: Fail to reject H0 while H0 is false
- This is an incorrect decision only if Ha is true.
- The probability of this incorrect decision $\beta$ is computed as 1-Power(test)