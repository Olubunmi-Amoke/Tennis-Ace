# Tennis Ace - Machine Learning
###I created a Linear Regression model that predicts the outcome for a tennis player based on their playing habits. I examined data of the top 1500 ranked men’s professional tennis league players from the Association of Tennis Professionals (ATP), spanning from 2009 to 2017. Provided in the dataset are service game (offensive) statistics, return game (defensive) statistics, and outcomes for each player, in each year. There were eighteen independent variables in total and one dependent variable. The independent variables consist of both the service game columns (offensive) and the return game columns (defensive). The service game columns are:
*Aces: number of legal serves by the player where the ball is not touched by the receiver
*DoubleFaults: number of times a player makes a mistake with both first and second attempts
*FirstServe: proportion of first serve attempts 
*FirstServePointsWon: proportion of first serve attempt won by a player
*SecondServePointsWon: proportion of second serve attempt won by a player
*BreakPointsFaced: number of times there was an opportunity for the player serving to lose and for the receiver to win the service game
*BreakPointsSaved: proportion of the time the player serving was able to stop the receiver from winning service game when they had the chance
*ServiceGamesPlayed: number of games where the player served
*ServiceGamesWon: number of games where the player served  and won
*TotalServicePointsWon: proportion of points in games where a player won when it is their service game

###The return game columns are:
*FirstServeReturnPointsWon: proportion of of opponent’s first serve points the player was able to win
*SecondServeReturnPointsWon: proportion of of opponent’s second serve points the player was able to win
*BreakPointsOpportunities: number of times there was an opportunity for the player to win the opponent’s service game
*BreakPointsConverted: proportion of the time there was an opportunity for the player to win the opponent’s service game and they won
*ReturnGamesPlayed:  number of games where the player’s opponent served
*ReturnGamesWon: number of games where the player’s opponent served and the player won 
*ReturnPointsWon:  number of points where the player’s opponent served and the player won 
*TotalPointsWon: proportion of points won by the player

After investigating and performing an exploratory analysis on the data, I found that there is a strong correlation between some of the features and the dependent variable, ‘Winnings’. The Winnings column contains the total winnings, in USD, of each tennis league player per year. I then proceeded to select features and values to predict based on this information. I splitted the data into eighty percent training set and twenty percent test set to be able to later evaluate the model’s accuracy. I created a linear regression model and fitted it to my training data to predict winnings.

I created a single-feature, two-feature and multiple-feature linear regression model and visualized their predictions in order to look closely at how independent variables impacted winnings. The DoubleFaults feature, ServiceGamesPlayed feature, ReturnGamesPlayed feature, BreakPointsOpportunities feature, and BreakPointsFaced feature all showed a strong positive correlation with the ‘Winnings’ outcome. To evaluate the model's accuracy, I printed out the coefficient of determination for each model built. Over seventy percent of the variation in winnings is explained by the variation in these independent features when I used all five features to build a model. We could say, non conclusively, that the multiple linear regression model built with the five independent variables mentioned above is a good fit. I am working to evaluate the model’s accuracy using other metrics to see if I need to rebuild it to get better results.
