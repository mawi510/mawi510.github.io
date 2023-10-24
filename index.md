## Dagmawi's Portfolio

---


### NFL Betting Spread Prediction

**Project overview:** As an avid sports fan, I looked for opportunities to incorporate both my fandom and my technical skillsets.

I scraped historical performance data, historical betting spreads, and historical weather to create a dataset to train both a gradient boosted regression and a random forest classifier. 

The dataset looked at 3 game rolling averages of various metrics including offensive total yards, defensive turnovers, and opponent strength (measured as total point spread / total games played). 

What was most surprising was that weather variables had small coefficients. Not surprisingly, the strength of the opponent had the highest coefficient.

<img src="https://github.com/mawi510/projects/blob/main/PredictingNFLGames/regressor_importance_chart.png?raw=true"/>

The gradient boosted regression had a RMSE of ~10, which isn't great, and has a lot of room for improvement. The random forest classifier has a precision of ~70%, and recall of ~59%, meaning the model tends to over-classify which teams will cover the spread. The ROC Curve below shows that, while the model is better than random chance, there's still room to improve

<img src="https://github.com/mawi510/projects/blob/main/PredictingNFLGames/classifier_roc_curve.png?raw=true"/>



***Technical skills:*** Multi-Linear Regression, Random Forests

***Tools:*** Python, Sci-kit Learn, Matplotlib

[![Open Code](https://img.shields.io/badge/Jupyter-Open_Files-red?logo=Jupyter)](https://github.com/mawi510/projects/tree/main/PredictingNFLGames)

---
### Is The Powerball Rigged?

**Project overview:** I wanted to see if the powerball lottery was truly a fair lottery. If it wasn't, I would take advantage

The powerball lottery selects 5 random numbers between 1 and 69 without replacement. If the lottery was fair, the distribution of these numbers should match that of random distribution for numbers picked between 1 and 69 without replacement.

Unfortunately, the lottery is indeed a fair game, meaning I won't become a billionaire anytime soon. The QQ plot shows that the two distributions line up nearly perfectly, proving the powerball is indeed selecting the numbers at random, and there isn't any preference towards smaller or larger numbers.

<img src="https://github.com/mawi510/projects/blob/main/Powerball%20Distribution/powerball_qqplot_image.png?raw=true"/>



***Technical skills:*** QQ Plot, Random Simulation

***Tools:*** Python, Statsmodels

[![Open Code](https://img.shields.io/badge/Jupyter-Open_Files-red?logo=Jupyter)](https://github.com/mawi510/projects/tree/main/Powerball%20Distribution)

---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
