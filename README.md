# A-B-test-Cookie-cats
A/B test Cookie-cats from Kaggle
### About Dataset
Source [Kaggle A/B test Cookie-cats](https://www.kaggle.com/datasets/zahrazolghadr/ab-test-cookie-cats/data)

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

The study encompasses the following steps:
1. Analysis of Cookie Cats dataset
2. Clean up the Dataframe
3. Check that the sample size is sufficient for the A/B test
4. Check if the 'sum_gamerounds' column is a normal distribution
5. Check the hypothesis that test group 'gate_40' is different from control group 'gate_30' by using the Mann-Whitney U statistic
6. Check the hypothesis that test group 'gate_40' is different from control group 'gate_30' by using the z-test
7. Check metrics

