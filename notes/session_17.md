# Inferential Statistics

## Why do we need Inferential Statistics? 
- Correlation Vs. Causation
- Controlled Experiment
    - Examples 
        - A/B Testing
        - Medical Trials

## Population
## Sample
### Why do we need sampling ?
#### Sampling bias
#### Types of sampling
### Sampling Distribution
- Probability distribution
- Area under the curve
- Gaussian distribution and Normal distribution
- Sampling Distribution of the Mean
- Central Limit Theorem (CLT)
    - [Online stats visualization](https://onlinestatbook.com/stat_sim/sampling_dist/)
    - If you take many samples from a population and calculate their averages, those averages will form a bell-shaped curve (normal distribution), even if the original data isn’t bell-shaped. This is useful because it lets us make predictions about the population.

## Hypothesis Testing
### Null Hypothesis
### Alternate Hypothesis
### Significance Level (α)
- Typically used values are 0.05 (e.g. e-commerce  ) and 0.01 (e.g in fileds like medicine)
### P-value

# Major Statistical Tests
## Z-test
A Z-test is used to compare means when the sample size is large $n>30$ and the population variance is known. It follows the standard normal distribution ($Z$-distribution).
The steps to do this as follows
1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your Z-test Statistic

$Z=\dfrac{\bar{x}-\mu}{\left(\frac{\sigma}{\sqrt{n}}\right)} \nonumber$

- $\bar{x}$ = sample mean
- $\mu$ = population mean
- $\sigma$ = population standard deviation
- $n$ = sample size

5. Find p-value using [Z-Table](https://math.arizona.edu/~rsims/ma464/standardnormaltable.pdf) and Z-test statistic computed
6. if p-value > $\alpha$, then we fail to reject null Hypothesis
7. There are one-tailed and two-tailed tests

## Z-test Practice Problem
A particular companies chocolate bars are supposed to have an average weight of 50 grams according to the maufacturer.
We want to test if a sample of chocolate bars deviates significantly from this weight.
Data: 50.8, 49.5, 50.2, 51, 49.7, 50.3, 49.8, 50.5, 49.6, 50.1
Population standard deviation: 1.5 grams (assumed based on production tolerance)

## T-test
- We need T-test because population standard deviation $\sigma$ is not always available
- Here we will be computing T-test statistic (based on the problem statement and type of t-test)


| **Type of T-test**        | **Null Hypothesis**                                        | **Alternate Hypothesis**                                       | **Degrees of Freedom** |
|---------------------------|------------------------------------------------------------|----------------------------------------------------------------|------------------------|
| One Sample t-test         | The sample mean is equal to the reference value            | The sample mean is not equal to the reference value            | $df = n-1$             |
| Independent Sample t-test | The mean values in both groups are the same                | The mean values in both groups are not equal                   | $df = n_1+n_2-2$       |
| Paired Samples t-test     | The mean value of the difference between the pairs is zero | The mean value of the difference between the pairs is not zero | $df = n-1$             |

### One Sample T-test
Compares the sample mean to a known population mean

The steps are as follows

1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your T-test Statistic

$t=\dfrac{\bar{x}-\mu}{\left(\frac{s}{\sqrt{n}}\right)} \nonumber$

- $\bar{x}$ = sample mean
- $\mu$ = population mean
- $s$ = sample standard deviation

$s = \sqrt{\frac{1}{n-1} \sum_{i=1}^N (x_i - \overline{x})^2}$
- $n$ = sample size
5. Find the critical t-value from [T-Table](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf) using significance ($\alpha$) level
6. if t-statistic < critical t-value, we fail to reject Null Hypothesis

### Independent Sample T-test

Compares means of two independent groups

The steps are as follows

1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your T-test Statistic

- $t = \dfrac{\overline{x_{1}}-\overline{x_{2}}}{\sqrt{(\dfrac{s_{1}^2}{n_{1}}+\dfrac{s_{2}^2}{{n_{2}}}})}$; for one tailed
- $t = \dfrac{\overline{x_{1}}-\overline{x_{2}}}{S_p\sqrt{(\dfrac{1}{n_{1}}+\dfrac{1}{{n_{2}}}})}$; for two tailed
  - $S_p = \frac{(n_1-1){s_1}^2+(n_2-1){s_2}^2}{n_1+n_2-2}$; known as pooled standard deviation

- $\bar{x_1}$ = sample mean of group 1
- $\bar{x_2}$ = sample mean of group 2
- $s_1$ = sample standard deviation of group 1
- $s_2$ = sample standard deviation of group 2
- $n_1$ = sample size of group 1
- $n_2$ = sample size of group 2

5. Find the critical t-value from [T-Table](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf) using significance ($\alpha$) level
6. if t-statistic < critical t-value, we fail to reject Null Hypothesis

Sample Data 
- Brand A: 49.5, 50.1, 49.8,50.3, 50
- Brand B: 50.4, 49.9, 50.6, 50.2, 50.1

### Paired Sample T-test
- Compares means from the same group at different times (before/after)

## F-Distribution

## Reference 
1 . [Data Lab Tutorial](https://datatab.net/tutorial/hypothesis-testing)
2.  [T.TEST Google Sheets] (https://support.google.com/docs/answer/6055837?hl=en)
