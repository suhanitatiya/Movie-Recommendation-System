
# Movie Recommendation System
Recommendation Systems are statistical algorithms that recommend products based on similarities between the 'buying trends of various users' or similarities between 'products' termed as Collaborative Filtering .

Collaborative Filtering types:-
1] User based 
2] Item based

This project is performed by suggesting other movies that are most similar to a particular movie (CORRELATION).



## Install and Import Libraries
Libraries installed and imported : numpy, pandas, matplotlib, seaborn.

To install libraries 

```bash
  !pip install numpy
  !pip install pandas

```
To import libraries 
```bash
 import numpy as np
 import pandas as pd
 import matplotlib.pyplot as plt
 import seaborn as sns
 sns.set_style('white')
 %matplotlib inline

```
Then, we merge the movie tiltles with the info.

## Datasets
```bash
1)movies_titles.csv   (contains title of movies and ids)
2)info.csv                 

```


## Exploratory Data Analysis (Histograms)
Explore the data a bit and get a look at some of the best rated movies. from the provided dataset.
Ratings dataframe with average rating and number of ratings:

```bash
ratings['num of ratings'] = pd.DataFrame(df.groupby('title')['rating'].count())
ratings.head()

```
HISTOGRAMS:-

we plot three different  histograms.




















## Recommending Similar Movies (Create matrix)

Create a matrix that has the user ids on one access and the movie title on another axis. Each cell will then consist of the rating the user gave to that movie.

```bash
moviemat = df.pivot_table(index='user_id',columns='title',values='rating')
moviemat.head()
```
Hence, matrix is created and displayed.

## Correlation between Starwars and Liar Liar  
```bash
corr_starwars.sort_values('Correlation',ascending=False).head(10)

```
## corrwith() 

Grab the user ratings for those two movies:starwars, a sci-fi movie. And Liar Liar, a comedy.
Use corrwith() method to get correlations between two pandas series.
Now if we sort the dataframe by correlation, we should get the most similar movies, however note that we get some results that don't really make sense. This is because there are a lot of movies only watched once by users who also watched star wars (it was the most popular movie).
Fix this by filtering out movies that have less than 100 reviews (this value was chosen based off the histogram from earlier).





## Environment Variables
We set the MOVIE_API_KEY environment variable to store the API key.

`MOVIE_API_KEY`



# Github profile: Suhani Tatiya


## Skills
Artificial Intelligence,  Machine  Learning , Natural Language Processing...

