# kaggle_spaceship_titanic
My attempt at the kaggle spaceship competition. The objective is to determine which passengers were transported to an alternative dimension (binary classification problem).

## My Pipeline
### Feature Engineering
I used PPScores to determine what relationships exist amoung features. PPScores are favourable over a simple correlation matrix as they capture non-linear relationships.

I was able to fill in some missing values based on the relationships discovered.

For values that remained missing, the were patched with median and 'NONE' for numerical and categorical features, repsectively.

### Modelling
The best performing model turned out to be a Support Vector Machine. It narrowly beat out the XGBClassifier. The third best model turned out to be an ensemble with equal weights applied to linear regression, XGBClassifier, K Nearest Neighbours, SVM and a neural net (multi-perception algo).

### Final Score
The SVM model had an accuracy score of 0.80266 which was good enough for a top quartile result on the leaderboard.
