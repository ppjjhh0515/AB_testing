# AB_testing

## Scenario
Imagine you work on the product team at a medium-sized online e-commerce business. The UX designer worked really hard on a new version of the product page, with the hope that it will lead to a higher conversion rate. The product manager (PM) told you that the current conversion rate is about 13% on average throughout the year, and that the team would be happy with an increase of 2%, meaning that the new design will be considered a success if it raises the conversion rate to 15%.

H0: p = p0
H1: p =/ p0
alpha: 0.05, confidence level = 95%

Dataset = https://www.kaggle.com/zhangluyuan/ab-testing?select=ab_data.csv

## Result:
Z stat: -2.01
P-value: 0.044
confidence interval 95% for control group: [0.106, 0.125]
CI 95% interval for treatment group: [0.119, 0.139]

## Conclusion
Since p-val = 0.044 is lower than a=0.05 threshold, we will reject the null hypothesis H0. Which means that our new design did perform significantly different (let alone better) than the old one.

Reject H0: p = p0 H1: p =/ p0

Additionally, the CI for treatment group is 11.9~13.9%.

It includes our baseline value of 13% conversion rate.
It does not include target value of 15%
This means that it is more likely that the true observation rate of the new design is not similar to our baseline. It concludes our foundings to reject the null hypothesis might be a rare instance of random state. Hence, it better to test more on different random state (set as 42).
