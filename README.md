# Is your Pitcher Predictable?

You could say pitching is one of the most important aspects of Baseball. They are involved in every defensive play, and based on ERA their performance makes a big difference in the flow of a game. But how can you tell how effective a pitcher is? 

This study will take a look at each pitcher in Major League Baseball and attempt to predict whether or not they are predictable. 
Using Pitch data from the 2015-2018 season we will predict the next pitch for each pitcher and depending on how well we are able to do so, we will determine how effective each pitcher is. 

### Table of Contents

1. [Goals](#goals)
2. [Pipeline](#pip)
3. [Analysis](#ana)
4. [Models](#model)
5. [Conclusion](#conclusion)
6. [Contact Information](#contact)

<a name="goals"></a>
## 1. Goals

One of the biggest goals of this project was to classify if a pitcher is predictable or not, and come up with clear answers to interpret that "predicatability" aspect of each pitcher. This was really difficult because a first I did not have much to go on in terms of predictability and what makes a pitcher predictable or not. Lets take a look at the pipeline to see the steps I took to come up with this metric. 

<a name="pip"></a>
## 2. Pipeline

<p align="center">
<img src="Graphics/pipeline.png">
</p>

The data preprocessing dealt a lot with imputing missing values, finding stats for each pitcher, and lots of visualization for understanding. After that I took a Supervised Learning route and found accuracy scores for each pitcher, and an unsupervised learning route that found relationships between pitchers based on the distribution of pitches that they continually throw. In the end I combined these two findings for a very interesting look at the predictability of each pitch.

Due to a lot of unknown at the beginning of this project, the pipeline can look somewhat intimidating. Here is the general overview about what I did and why:

The main goal that I set out was to find a relationship between a pitcher’s performance and how predictable their pitches are. Using Supervised Learning I used a multi-classification model to classify the pitch type on each given pitch using, the count, runners on base, the batter, and several other features for each individual pitcher. This model provided an accuracy score for each pitcher that threw over 2,000 pitches which we can interpret as their “predictability”. I also used dimensionality reduction techniques to perform unsupervised learning Clustering on each pitcher and their new “features” that can be interpreted as a combination of the percentages of each pitch type that they threw. By clustering each pitcher using Kmeans with 3 clusters, we were able to find impressive results between their individual “predictability” and their distribution of pitches that they throw. 


<a name="ana"></a>
## 3. Analysis

This Project involved a lot of EDA. This dataset was provided on Kaggle and contained Major League Pitching data from 2015-2018. The data was contained into separate csv's:

| CSV's | Contents | Number of Rows | Number of Columns |
|--------------------------|------------------------------|-------------|----------|
|`atbats.csv`| count, outcome, batter name, pitcher name, inning, etc. of each atbat|740,389 | 11|
|`player_names.csv`|first name, last name|2,218 | 3|
|`games.csv`| team, location, weather, score, etc. for each game|9,718|17|
|`pitches.csv`| speed, location, live game stats, etc. for every pitch thrown|2,867,154 |40|
|`ejections.csv`| name, time, game, etc. of every ejection|761 |10|


<a name="model"></a>
## 4. Modeling

I was extremely excited about the 2.8 million pitches I would be able to work with. This excitement slowly turned to difficulty as I ran into problems using this amount of data. I wanted to initially build a model that could classify the next pitch that could be throw but due to the time constraints of this project it was not achieveable. The next best alternative was to build a model for each pitcher and classify how "predictable" they are using the score of that model. 

<a name="conclusions"></a>
## 5. Conclusions

<a name="contact"></a>
## 6. Contact Information
