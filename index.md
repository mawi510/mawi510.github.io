## Dagmawi's Portfolio

---

### Does Building Affordable Housing Raise Local Rents? A Bayesian Analysis

**Project overview:** Housing debates throw around the claim that building Low-Income Housing Tax Credit (LIHTC) units pushes local home values and rents up. There's almost no data behind it, so I went and checked.

State coefficients vary so much that the "national effect of LIHTC" framing turns out to be the wrong question. Housing policy is local, and the model surfaces that directly. After adjusting for inflation (CPI-less-shelter) and population growth, I find a small positive association: 0.13% for home values and 0.32% for rents per 1% more LIHTC per capita. Hawaii, California, and Colorado run hot. Ohio and Oklahoma sit on zero. Leave-one-out cross-validation picks the inflation-adjusted hierarchical model over every alternative I tried.

To get there, I pulled six public datasets (HUD's 54k-project LIHTC database, Zillow home and rent indices, three vintages of Census population estimates, and FRED inflation data) and joined them on county FIPS into two county-year panels. Then I fit a Bayesian hierarchical model in PyMC with county intercepts and state-level slopes, so each county borrows strength from its state instead of collapsing into one national average.

The positive sign is the part worth sitting with. More rental supply should lower rents, so the result more likely reflects where credits get allocated (high-demand markets) than a price effect of the units themselves.

<img src="https://github.com/mawi510/lihtc-bayesian-analysis/blob/main/reports/figures/housing_plot_forest.jpg?raw=true" width="480"/>

<em>Each row is a state's posterior LIHTC slope on home values, 95% HDI. Several states sit on zero, others run well past it.</em>

***Technical skills:*** Bayesian Hierarchical Modeling, MCMC, Partial Pooling, LOO Model Comparison, Data Engineering (multi-source ETL)

***Tools:*** Python, PyMC, ArviZ, pandas, NumPy

[![Read Report](https://img.shields.io/badge/Read-Full_Report_(PDF)-blue?logo=adobeacrobatreader)](https://github.com/mawi510/lihtc-bayesian-analysis/blob/main/reports/LIHTC_Bayesian_Analysis_Report.pdf)
[![Open Code](https://img.shields.io/badge/Jupyter-Open_Files-red?logo=Jupyter)](https://github.com/mawi510/lihtc-bayesian-analysis)

---

### NFL Betting Spread Prediction

__(Soon to be updated for the 2025 season!) Interact with this model and view historical performance data for your favorite team <a href="http://promatchpredict.com/" target="_blank" rel="noopener noreferrer">here</a>__


**Project overview:** As an avid sports fan, I looked for opportunities to incorporate both my fandom and my technical skillsets.

I scraped historical performance data, historical betting spreads, and historical weather to create a dataset to train a random forest classifier, which flows into the website listed above. This was a great project to construct an ETL pipeline, train/test an ML model, and then deploy said model to the cloud so others could interact with it.

The diagram below details how the website is powered and where data comes from

<img src="https://github.com/mawi510/projects/blob/f2591ef992a979b873d3ceb14e7eaefedb044214/PredictingNFLGames/ProMatchPredict%20Diagram.png?raw=true"/>

***Technical skills:*** Random Forests, Cloud Computing, CI/CD Pipeline, ETL

***Tools:*** Python, Sci-kit Learn, Docker, EC2, Github Actions

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
