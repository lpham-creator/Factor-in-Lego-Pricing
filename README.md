# Factors in Lego Pricing
Our group sets up a primary hypothesis about the relationship between a Lego set's recommended price and its number of pieces, and a supplementary one about how Lego themes affect the recommended price of a set.
## Libraries used:
- ggplot2
- infer
- tidyverse
- openintro
## Cleaning and Preprocessing
- Fetched and loaded data from [Peterson and Ziegler (2021)](https://www.tandfonline.com/doi/full/10.1080/26939169.2021.1946450) website.
- Cleaned data by
removing columns that didn't affect airport efficiency based on our findings
removing all missing values (565 observations).
- Preprocessed data by
grouping 40 Lego themes into 10 larger theme buckets to fit in to linear model
percentiles, rates, and positions (reported in Table 1).
## Our Hypothesis
### Primary Hypothesis
- $H_0: \beta_1 = 0$: the mean number of pieces in Lego sets affects the lego sets' mean recommended price.
- $H_A: \beta_1 \neq 0$: there is no association between mean number of pieces and mean price of lego sets.
### Secondary Hypothesis
- $H_0$: The mean price is the same for each level of LargerThemes $\mu_1 = \mu_2 = ... = \mu_{10}$.
- $H_A$: The mean price is not the same for each level of LargerThemes, i.e. at least one mean is different from the others.
## Statistical Methods
- Conducted two hypothesis tests using a linear regression model and the Analysis of Variance (ANOVA).
- Fit a linear regression model into the relationship between Price and Pieces.
- Used an ANOVA F-test on the relationship between Price and Themes.
## Results
- For both tests we get our p-value = 0. We think that R rounds it to this value, meaning that the p-value is smaller than 0.05. Hence, we reject the null hypothesis and are able to conclude that the mean recommended price and the number of pieces in a Lego set has a statistically significant relationship with each other.
- Our analysis finds statistically significant evidence of an association between pieces and price, and between theme and price, with theme not found to be a confounder in the first relationship.
- View the [report](https://github.com/lpham-creator/Factor-in-Lego-Pricing/blob/main/group-L-report.pdf) to see a more complete version of our study.
## Application
- This project opens new ways for LEGO to alter their price based on characteristics of the set, and helps customers predict the expense of a Lego set.
## Limits
- Due to missing values, we excluded about 40% of the observational units in the original data set from our analysis, which affects the generalizability of our findings.
- The analysis could be improved by using a different method to deal with missing values, and by further refining our regression models for our primary hypothesis, which were somewhat limited by the methods of analysis we have learned so far.
