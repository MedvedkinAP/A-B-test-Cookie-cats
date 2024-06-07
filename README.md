# A-B-test-Cookie-cats
A/B test Cookie-cats from Kaggle
### About Dataset
Source [Kaggle A/B test Cookie-cats](https://www.kaggle.com/datasets/zahrazolghadr/ab-test-cookie-cats/data)

(https://github.com/MedvedkinAP/A-B-test-Cookie-cats/blob/main/dataset-cover.png)

#### This dataset comprises A/B test outcomes for Cookie Cats, investigating the impact of relocating the initial gate in the game from level 30 to level 40. Upon installing the game, players were randomly assigned to either gate_30 or gate_40.
#### The data we have is from 90189 players that installed the game while the AB-test was running.  The variables are: 
- userid: A unique number that identifies each player
- version: Whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40)
- sum_gamerounds: the number of game rounds played by the player during the first 14 days after install
- retention_1: Did the player come back and play 1 day after installing?
- retention_7: Did the player come back and play 7 days after installing?

### AB-test checks two hypotheses:
1. HO: There is not sufficient difference between values in the 'sum_gamerounds' column for levels 30 and 40
2. H1: There is sufficient difference between values in the 'sum_gamerounds' column for levels 30 and 40
3. Term of test:
- Effect size calculation: 3% of the mean of the control group
- Perform power analysis to determine the required sample size:
 alpha = 0.05 (Significance level),
 power = 0.80 (Power)

The study encompasses the following steps:
1. Analysis of Cookie Cats dataset
2. Clean up the Dataframe
3. Check that the sample size is sufficient for the A/B test
4. Check if the 'sum_gamerounds' column is a normal distribution
5. Check the hypothesis that test group 'gate_40' is different from control group 'gate_30' by using the Mann-Whitney U statistic
6. Check the hypothesis that test group 'gate_40' is different from control group 'gate_30' by using the z-test
7. Check metrics

### Tools
Python

### Results/Findings
The analysis results are summarized as follows:
1. The data distribution of 'sum_gamerounds' column is not normal and contains significant outliers
2. The sample size is sufficient for the A/B test
3. The difference between the two groups is not statistically significant. HO is true.
4. Retention metrics significantly worsened

### Recommendations
Based on the analysis, we recommend not changing gate_30 to gate_40

### Limitations
I had to remove all outlier values from the'sum_gamerounds' column for more than three standard deviations.

### References

