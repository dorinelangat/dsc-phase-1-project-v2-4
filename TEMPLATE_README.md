# Microsoft's New Movie Studio Pitch
By Dorine Langat

![Microsoft](microsoft.png)

## Overview

Microsoft has learnt that other big companies are creating video content and they want in on the fun too. However, they know nothing about creating movies. We are tasked with the responsibility of exploring the type of films currently doing best at box office and give actionable recommendations to Microsoft to venture into the film industry successfully.

The data method used in this project is exploratory data analysis, whereby we'll look into four different datasets and find relevant information that will help us provide clear recommendations.

Some of the results obtained from this analysis among others, show that the top 3 most profitable genres are Science Fiction & Fantasy, Action & Adventure, and Kids & family.

We therefore recommend Microsoft to create films along those genres as they are most likely to earn them more profits.


## Business Problem

Microsoft is inspred to start creating movies  like other big companies. However, Microsoft has no idea how to go about it. 

We are therefore tasked with the responsibility of exploring the type of films doing best currently to help Microsoft venture into this industry successfully. 

In order to objectively provide clear recommendations that will be beneficial to Microsoft, the following questions will act as a guide to drawing insights from our datasets.

     * Which film production studio made the highest total gross revenue in box office.

     * Is there a relationship between the prduction budget and the revenue made.

     * How does the original language of a film affect its popularity.

     * How is the trend of film runtime over the years.

     * What is the correlation between critics' score and the people's score.

     * What are the top ten most profitable genre.


## Data Understanding

 The for datasets we'll be working with here are 'bom.movie_gross.csv', 'tmdb.movies.csv', 'tn.movie_budgets.csv', and 'rotten_tomatoes_top_movies.csv'. 

    * The 'bom.movie_gross.csv' dataset is a box office dataset showing the domestic and foreign gross revenues of each movie.
  
    * The 'tmdb.movies.csv' dataset shows the original languages of different movies and their percentage popularity.
  
    * The 'tn.movie_budgets.csv' dataset shows production budgets and their corresponding worldwide gross revenue.
  
    *The 'rotten_tomatoes_top_movies.csv' dataset shows the box office performance of each movie and their genres in USA.

 These first three datasets can be found in a zipped file in [GitHub](https://github.com/learn-co-curriculum/dsc-project-template/tree/template-mvp/zippedData), and the fourth dataset can be found in [Kaggle](https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset).

 These datasets will help us answer the questions above.


## Methods

We analysed each dataset individually and visualised our results based on the contents of that dataset. The common steps for all the datasets were dropping missing values, changing columns to our desired datatypes, and dropping columns not needed in our analysis.

##### First_Dataset

In the first dtaset ('bom.movie_gross.csv'), our objective is to compare the average amount of the total gross revenue made by each production studio per film created.

We first created a column for the total gross revenue, which is a result of the sum between domestic and foreign gross.

We then grouped our data by the studio, and calculated the mean of the total gross revenue.

The next thing was to sort the results of the above step in a descending order and used the top 20 to plot a bar plot to represent the average amount of revenue a studio makes per film.

##### Second Dataset

In the second dataset ('tmdb.movies.csv'), our objective is to find out whether the original language for which a film was produced affects the film's popularity.

Same case to the first dateset, we grouped our data by the original language and calculated the mean of the popularity per language.

We then sorted the results of the above step in a descending order and used the top 30 outputs to plot a bar plot to represent the average popularity of an original language per film produced.

##### Third Dataset

In the third dataset ('tn.movie_budgets.csv'), our objective is to find out the relationship between the production budget and the corresponding worldwide gross revenue of films produced.

After converting our relevant columns to the desired datatype, we went ahead to plot a scatter plot to show the correlation between the production budgets and worldwide gross, and also calculated the correlation using pandas function .corr()

##### Fourth Dataset

In the foruth dataset ('rotten_tomatoes_top_movies.csv'), our objective was to find out the trend of film runtime over the years, find out the relationship between the people's and critics' scores, and to find out the top most profitable genres.

First, we converted the runtime column from hours and minutes to minutes alone, then plotted a line graph to show the trend over the years.

We then plotted a scatter plot to show the relationship between people's score and critics' score, and also calculated the correlation using pandas .corr() function.

Finally, we grouped our data by the film type and calculated the mean of their total worldwide gross per film produced, amd sorted the results in a descending order. Then we plotted a bar plot to represent the box office gross in usa per genre.


### Results, Conclusions & Recommendations.

##### Visual_1
![Studio Gross Revenue](studio_vs_gross.PNG)

From the results above, the top 5 five studios with the highest average gross per film are HC, P/DW, BV, GrtIndia, and WB. 

Based on these results, we can conclude that studios that make the highest revenue per film can act as a benchmark for Microsoft as they start to create video content.

Microsoft should therefore emulate what these top studios are doing different and even improve on some aspects to get ahead of the game.

##### Visual_2
![Language Popularity](popularity_vs_language.png)

From the results above, we can see that the popularity of a movie is not affected by the original language in which it was produced. This is beacause, despite English, French, and Spanish having the highest number of movies, some of their films are not as popular which explains why they don't appear among the top in the popularity list.

Based on these results, we can conclude that the popularity of a film is not determined by the language in which it is produced. 

Microsoft should therefore create films on the basis of the target audience rather than focusing on the language. Moreover, films can always be translated to different languages to suit the target audience. 

##### Visual_3
![Production Budget vs Gross Revenue](budget_vs_gross.PNG)

From the results above, we can see that the production budget of a film has a positive correlation with the worldwide gross revenue. 

Based on these results, we can conclude that the higher the production budget, the higher the quality of the film produced, which also translates to its popularity and eventually an increase in the worldwide gross revenue.

Microsoft should therefore allocate sufficient resources to the creation of video content in order to realize a high revenue stream. These resources could include hiring of competent crew to ensure quality production of movies.

##### Visual_4
![Runtime Trend](runtime_trend.PNG)

From the results above, the runtime of films over the years has no significant difference. The runtime ranges between 75 - 150 minutes. The only difference noted here is the increase in the number of movies produced over the years. This could also indicate a competitive industry, or an increase in demand for video content.

Based on the results, we can conclude that the normal film runtime lies between the range of 75 to 150 minutes.

Therefore, Micrrosoft should stick to creating video content within that range.

##### Visual_5
![People vs Critics Score](people_vs_critics.PNG)

From the results above, we can see that people's score has a positive correlation with critics' score. This indicates that the measure used by both categories are almost similar.

We can conclude that there are certain goals in film production that needs to be met for it to do well in the market.

Therefore, Microsoft should tailor their movie production in such a way that it meets the desired goals, in order to increase their scores, which increases its popularity and eventually the revenue.

##### Visual_6
![Most Profitble Genre](profitable_genres.PNG)

The results indicate that the most profitable genres in the film industry are Science Fiction & Fantasy, Action & Adventure, and Kids & Family. 

The conclusion here is that, most people's interests are in these genres. We can also say that creative movies such as Science Fiction & Fantasy and Action & Adventuer are popular because of their plot unpredictability and also takes viewers to an imaginary world. Films under Kids & Family are also profitable due to their popularity, in that, most people like to watch films with their families, hence the need for something family friendly.

Microsoft should therefore purpose to create movies along these lines, and more importantly, learn and understand the needs of their target audience.
