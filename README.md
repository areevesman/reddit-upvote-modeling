
# Predicting Reddit Comment Upvotes

Contributors: 

* Adam Reevesman
* Gokul Krishna Guruswamy
* Hai Le
* Maximillian Alfaro
* Prakhar Agrawal

## Resources in this repository

The code for this project is divided into several notebooks, each of which regards a part of the workflow.

The finalized notebooks that combine into our entire work includes:

* Step 1: [Extracting data](data_processing/extract_Data.ipynb) and [scraping extra data](scraping/Scrape.ipynb) (reddit api keys needed)
* Step 2: [Data processing and feature engineering](data_processing/data_processing.ipynb). At the end of this process, we arrive at this [list of final features](data_processing/features.md) which we used to fit our models.
* Step 3: [Model fitting and model comparison](model_fitting/model_fitting.ipynb). In this notebook, we fitted different linear and non-linear models to the dataset, evaluate and compare their performance. The models were originally fit on data that differed slightly from the data obtained after the included data processing notebook. Therefore, an [updated notebook](model_fitting/model_results_v3_data.ipynb) is included to show the new results on some of the models using the updated dataset.

## Objective

Original: To predict how many __upvotes__ a comment will get, given the comment text, user history, sub-reddit and thread details.

Next Step: Improve current model performance.

## Data Source

We use 2 sources of data: 

* Comments Dataset [available here](https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w)
* Threads Dataset scraped using Reddit API using [this code](/scraping/Scrape.ipynb)

## Models and Metrics

We attempted linear and nonlinear regression models and compared their Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R<sup>2</sup> values. The Random Forest had the lowest MAE, around 8, which suggests that on average, the model is off by about 8 upvotes.

RMSE penalizes large errors more heavily. The magnitudes of RMSE among our models suggests that they have lots of large errors.

<img src="/images/mae.png" width="600" height="400" />

<img src="/images/rmse.png" width="600" height="400" />

<img src="/images/r2.png" width="600" height="400" />


## Reference Papers/Write-ups

* [Predicting Comment Karma on Internet Forums](http://cs229.stanford.edu/proj2014/Daria%20Lamberson,Leo%20Martel,%20Simon%20Zheng,Hacking%20the%20Hivemind.pdf)
* [Predicting Comment Karma by Subreddit](http://yoavz.com/reddit_karma.pdf)
   - github link concerning [this paper](https://github.com/yoavz/predict_reddit_comments) 
   
## FAQ about reddit

* [what is karma](https://www.reddit.com/r/NoStupidQuestions/comments/2idfhk/what_is_link_karma/)
* [what is reddit](https://www.reddit.com/wiki/faq)
