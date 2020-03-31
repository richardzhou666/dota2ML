# ML Project: Predict Dota 2 Game Outcome
This is my personal machine learning project. The goal of the project is to predict the outcome of dota2 game.

# Introduction
![](dota.jpg)
_Dota 2_ is a famous video game with a large esports scene in the world. _Dota 2_ has an annual esports world championship tournament with over $34 million US dollars prize pool in the recent one. The ability to predict the out come of a specific game is extremely crucial not only in the sports tournament but also in regular game pubs. Knowing the winning factor of game will help player to analyze the game and strategy. 

# Data
## Data overview
The data set comes from a public [_kaggle competition_](https://www.kaggle.com/c/mlcourse-dota2-win-prediction/overview). This competition is organized by [_mlcourse.ai_](mlcourse.ai) in collaboration with [_GOSU.AI_](GOSU.AI) which is a company specialized using artificial intelligence to help player improve skills and strategies. The publisher already provides `train_features.csv` and `test_features.csv` sets as training and test data sets. However since this is a kaggle competition, the true result of the `test_features.csv` set is not released at this point. Therefore I will create my own test sets from the `train_features.csv` set. The `train_targes.csv` data set is the results for games from the training set, _i.e._ whether team Radiant eventually won. I will combine two data sets for easier data manipulation. The descriptive variable we are interested in is `radiant_win` which indicates `True` or `False`. Now we create our own dataframe by combining data sets. 

## Variables overview
Here is the short list of definitions of explanatory variables that I am going to use in my analysis:

* `towers_killed`: number of enemy team's towers killed
* `K/D/A`: kills, deaths, assists
* `lh`: last hits, number of enemy creeps killed
* `denies`: number of friendly creeps killed to deny enemy's gold and experience
* `gold`: gold player earned
* `xp`: player's experience
* `level`: player's level
* `stuns`: total duration of stun, which immobilize enemy players
* `firstblood`: first player to complete a kill, which has better gold rewards
* `obs_placed`, `sen_placed`: the number of observation and sentry wards placed by a player

# Machine Learning
The project implemented the following ML algorithms:

* Logistic Regression
* Random Forests
* Support Vector Machine (SVM)

# Conclusion
![](test_error)
