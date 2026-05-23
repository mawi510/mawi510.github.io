## Dagmawi's Portfolio

---

### Does Affordable Housing Raise Local Housing Costs? A Bayesian Analysis

**Project overview:** Affordable-housing policy gets debated constantly with little hard evidence. I asked a focused, data-driven question: as a U.S. county builds more Low-Income Housing Tax Credit (LIHTC) units, what actually happens to its home values and rents?

I built two county-year panels by merging six messy public datasets (HUD's 54k-project LIHTC database, Zillow home & rent indices, three vintages of Census population estimates, and FRED inflation data) joined on county FIPS codes. I then fit a **Bayesian hierarchical model in PyMC** — county-level intercepts with state-varying slopes — so counties are treated as correlated within their state rather than as independent national samples.

After deflating prices for inflation and controlling for population growth, I find a modest positive association (+0.13% for home values, +0.32% for rents per 1% increase in LIHTC per capita) that **varies sharply by state** — strong evidence that housing policy is better addressed locally than nationally. Formal leave-one-out (LOO) model comparison decisively favors the inflation-adjusted hierarchical model.

The forest plot below shows each state's posterior LIHTC slope: some straddle zero while high-demand states like Hawaii, California, and Colorado are strongly positive — heterogeneity a single pooled model would erase.

<img src="https://github.com/mawi510/lihtc-bayesian-analysis/blob/main/reports/figures/housing_plot_forest.jpg?raw=true" width="480"/>

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
