### Youtube Viral Video Forecasting 
This repository contains the code written by Aleksandra Jacewicz, Alyssa Rodriguez, Kamillah Ismail, and Trina Dang through out our time working as AI Fellows with Google on a project where we pre-processed real world Youtube data, engineered features that are powerful and can realistically be used, and eventually built supervised, regression-based models that can predict how many views a video labeled as viral by Youtube will get. 


### Data Processing & Feature Engineering
We pre-processed around 50k data instances as part of this project. In doing so, we replaced missing data with average values (for ‘dislikes’ and ‘comments’, on a channel basis when possible), combined data tables to have access to a full representitive dataset, removed exact duplicates in dataset (≈ 160), extracted information from time based columns (‘publishedAt’, ‘trending_date’) and taking difference between them to be able to do per day based calculations for numeric columns and did one hot encoding for relevant columns (ex. categoryID -> Film & Animation, News & Politics, etc). 

We also processed text based data to allow for natural language processing to take place and then persued that. This included cleanin, tokenization, building vocabulary, training embeddings and getting vectorized results.

### Models and Results 
We built several models across the course of this project, with every member of our team taking on a different model. We've uploaded our final project presentation here, so feel free to look at it to find out more! As a general overview:

- Aleksandra worked on building a neural network based model, and was able to get an MSE (mean squared error) of .1069. 

    The code used while doing so can be found at [`Model_Development/Neural_Network.ipynb`](https://github.com/a-jacewicz/google-3e/blob/main/Model_Development/Neural_Network.ipynb)


### Dataset 
We used the [Youtube Trending Video Dataset](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset/data), and specifically the `US_category_id.json` and `US_Youtube_trending_data.csv` files found in it while training our models. 


The `US_Youtube_trending_data.csv` file contains around 50k snapshots of information about viral Youtube videos across times, with the columns it has including: 
* `video_id`
* `title`
* `publishedAt`
* `channelID`
* `channelTitle`
* `categoryId`
* `trending_date`
* `tags`
* `view_count`
* `likes`
* `dislikes`
* `comment_count`
* `thumbnail_link`
* `comments_disabled`
* `rating_disabled`
* `description`
