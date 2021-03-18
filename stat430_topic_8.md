# Topic 8a Confidence Intervals
## 1. Theory
$\alpha$ = probability of error (Type I)

1 - $\alpha$ = confidence level = probability that a random interval will capture the true value of the population $\mu$

## 2. Two-sided Interval
### Central Limit Theorem
- As the sample size n increases, or as the number of trials n approaches infinite, the shape of a sampling distribution becomes increasely like a normal distribution
- The mean of a sampling distribution =  the mean of population =  $\mu$
- The standard deviation of a sampling distribution = $\sigma(x) = \frac{\sigma_x}{\sqrt(n)}$

$Z_{\alpha/2} = \frac{X-\mu}{\sigma/\sqrt(n)}$ 

Explaination : 100(1-$\alpha$)% of the possible sample means surround $\mu$ in the middle
### Margin of error
margin of error = (upper_bound - lower_ bound)/2

### Sample size n
$n = (\frac{Z_{\alpha/2}(\sigma)}{w})^2$

## 3. SAS commands

### Proc means
| Option     | Description |
| ----------- | ----------- |
| CLM      | Lower and upper two-sided 95% confidence interval (CI) for the mean      |
| LCLM   | Lower one-sided 95% CI for the mean.         |
| UCLM   | Upper one-sided 95% CI for the mean.         |

Notes: If both LCLM and UCLM are requested, a two-sided CI is computed; otherwise, this option gives you a one-sided interval.
# Topic 8b

