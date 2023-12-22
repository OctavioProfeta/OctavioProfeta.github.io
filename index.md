---
layout: page
title: Societal fears and movies
cover-img: /assets/img/banniere3.png
---

{: style="text-align: justify;"}
Here, at WorkingTeam2023™, we want to know what are societal fears. So, what are we *afraid* of ? We are talking about societal fears, like the fear of a global pandemic or the fear of a nuclear war, not the fear of spiders or the fear of heights. [The Chapman University](https://www.chapman.edu/wilkinson/research-centers/babbie-center/survey-american-fears.aspx) conducts yearly studies based on surveys in the United States of America, giving us a starting point for an answer. By taking a look at the results of the surveys from 2018 to 2023, we have chosen to consider 7 majors global fears, which are the following :
*   War
*   Climate Change
*   Terrorism
*   Pandemics
*   Economical Collapse
*   Technological Advancement
*   Aliens

{: style="text-align: justify;"}
We also want to know whereas these subjects appears in the cinema industry, and whether the movies treating them know some kind of success, aswell as point geographical and temporal trends.

## The datasets

{: style="text-align: justify;"}
We will be using the [Movie Summary Corpus](https://www.cs.cmu.edu/~ark/personas/), which is a dataset containing more than 42'000 movie plot summaries, aswell as some other corresponding metadata. Added to that is the IMDb, which contains information about film's box office.

## Ready, set... analyse !

{: style="text-align: justify;"}
Hold on ! Let's first take a look at our data, and start by first seeing how many films have been produced through the years 

<p align="center">
<iframe src="movie_release_years.html" width="750px" height="400px" frameborder="0" position="relative">Genre plot</iframe>
</p>

{: style="text-align: justify;"}
We clearly see the trend here : The movie industry has grown largely during the recent years, more specificaly at the start of the 90s ! What about country movie production ? Which country is the more productive ?

<p align="center">
<iframe src="top_10_countries.html" width="750px" height="400px" frameborder="0" position="relative">Genre plot</iframe>
</p>

{: style="text-align: justify;"}
No surprises here, the United States of America is by far the most productive country, followed by India with Bollywood and the United Kingdom, almost tied for second place. The USA are responsible for more than 39% percent of the movie produced ! We need to keep in mind that the analysis we will be doing will be biased towards the USA.

## Let's get down to business

{: style="text-align: justify;"}
Let's start by analysing which are the recurrent topic in movies. By using topic detection algorithms on the plot summaries, we can extract major subjects from the movie plots. Looking for 8 topics yields the best results :

<iframe src="lda.html" width="750px" height="860px" frameborder="0" position="relative">Genre plot</iframe>

{: style="text-align: justify;"}
By setting λ to 0.5, we can interpret the following topics :

1. Drama and/or Relationships
2. Horror
3. Detective and/or Crime
4. War
5. Musical
6. Western
7. Supernatural
8. Undetermined, related to animals or creatures

{: style="text-align: justify;"}
War appears naturaly in the most reccurent topics. It is also on of the most salient terms, all topic cofounded. This indicate an interest for war in itself, but also for the consequences of war, such as the loss of loved ones, the destruction of the environment, etc. This implies that war is one of the most important societal fears.

## War, war never changes...

{: style="text-align: justify;"}
...or does it ? Let's do a topic detection on the plot summaries of movies which can be classified as war movies, by having the 'war' term appearing in the genre list. Looking for 4 topics yields the best results :

<iframe src="lda_genre_war.html" width="750px" height="860px" frameborder="0" position="relative">Genre plot</iframe>

{: style="text-align: justify;"}
Here, again by setting λ to 0.5 we can distingish 4 topics :

{: style="text-align: justify;"}
* The first one represent the pacific theather of the second World War. We can tell by terms such as '*japanese*', being the most frequent term within the topic, '*american*', '*hitler*' or '*boat*'. 
* The second topic represent mostly the Vietnam War, with terms such as '*vietnam*' or '*vietnamese*'. 
* The third topic seems to englobe war in general, with mostly generic war terms. 
* The forth topic represents the european theater of the second World War. This is clearly seen with terms such as '*jew*', '*jewish*' or '*nazi*'. 

{: style="text-align: justify;"}
We can see that the second World War is the most represented war in movies, with 2 topics out of 4. This is not surprising, as the second World War can be considered the most important war in the history of mankind.

We'll take a more specific look on war as a societal fear in movies later on.
## Make movies, not war

{: style="text-align: justify;"}
Alright, alright, we get it, war is not good. Let's talk about something happier; let's take a look at the rest of the movies which are not considered as war movies. Again, we apply a topic detection algorithm on the plot summaries. Looking for 4 topics yields the best results :

<iframe src="lda_genre_not_war.html" width="750px" height="860px" frameborder="0" position="relative">Genre plot</iframe>

## *insert funny phrase about lexicons*

{: style="text-align: justify;"}
Okay, let's get specific then. Since we already know which themes we want to explore in the plot summaries, we'll create adapted and representative lexicons for each of them. We will then use these lexicons to extract the frequency of each theme in the plot summaries. Here are some examples of the lexicons we created :

{: style="text-align: justify;"}
*   War : '*war*', '*conflict*', '*battle*', '*combat*'
*   Climate Change :'*global_warming*', '*greenhouse_gas*', '*carbon_footprint*', '*renewable_energy*'
*   Terrorism : '*terrorism*', '*extremism*', '*radicalization*', '*terrorist_attack*'
*   Pandemics : '*pandemic*', '*epidemic*', '*outbreak*', '*virus*'
*   Economical Collapse : '*economic_crisis*', '*financial_collapse*', '*recession*', '*depression*'
*   Technological Advancement : '*robotics*', '*artificial_intelligence*', '*automation'*, '*data_science*' (yes, very scary indeed!)
*   Aliens : '*extraterrestrial*', '*alien*', '*UFO*', '*alien_abduction*'

{: style="text-align: justify;"}
This way, each movie gets assigned with a frequency metric which measures the proximity of that movie to each one of the themes. Let's see how those frequencies vary throughout the decenies :

<p align="center">
<iframe src="evolution_of_frequency.html" width="750px" height="500px" frameborder="0" position="relative"></iframe>
</p>

<!-- <p align="center">
<iframe src="test_map2.html" width="600px" height="500px" frameborder="0" position="relative"></iframe>
</p> -->


<p align="center">
<img src="assets/img/graph.png">
</p>

## Case study : War movies

{: style="text-align: justify;"}
As seen in our first topic detection, war seems to be is the most represented societal fear in movies. Let's take a closer look at it. For this category, we can take a look at both the lexicon of war we've created earlier, and war-related genres. This is only possible for the war theme, since it's the only fear category which has genres associated with it.

### Analysis on the war lexicon

{: style="text-align: justify;"}
In the introduction, we pointed out that the USA and India are the two most productive countries in the movie industry. Let's see how the frequency of the war theme varies in the movies produced by these two countries, by starting with the USA :

<p align="center">
<iframe src="usa_war.html" width="750px" height="500px" frameborder="0" position="relative"></iframe>
</p>

{: style="text-align: justify;"}
We observe quite directly that the frequency of the war lexicons is related to major wars in which the USA was involved. For both the first and second World War, peaks in frequency are observable. One should take into account that the peaks are shifted towards the left since we calculate the mean frequency for 5-year periods. We can also observe that the freqency drops at the end of each major war. Concerning the Vietnam war, the peak is less present than for the other wars. However, the frequency declines more gently during this period.

{: style="text-align: justify;"}
These findings suggest that a ongoing war may impact the content and number of war-related movies that are being produced. This is not surprising, since the movie industry is a reflection of the society. We also see that the end of a war is followed by a decline in the frequency of the war lexicon. This could be explained by the fact that the public is not interested in war themed movies anymore and directors have less interest in producing them. It is also interesting to see the smoother decline of the frequency during the Vietnam War, which could be explained by the long duration of this war.
Finally, we can also observe that the frequency of the war lexicon is not null during periods of peace. This could be explained by the fact that the war theme is not only related to the war itself, but also to the consequences of war.

{: style="text-align: justify;"}
Let's now take a look at the frequency of the war lexicon in the movies produced by India :

<p align="center">
<iframe src="india_war.html" width="750px" height="500px" frameborder="0" position="relative"></iframe>
</p>

{: style="text-align: justify;"}
It seems that the main wars in which India was directly involved in had less impact on the frequency of the war lexicon than for the USA. We can still se that the major increase of the frequency of the war lexicon happens after World War 2, which might be explained by the fact that India was a British colony during this period, and that the war had a major impact on the country. One explaination for the lower frequency of the war lexicon could be that the major movie producer for India, Bollywood, is more focused on the production of musicals and comedies.

### Analysis on war-related genres

{: style="text-align: justify;"}
Let's continue the analysis based on war-related genres. To do so, we've selected movies that have an assigned genre which contains the term 'war'. 

#### Sentiment analysis

{: style="text-align: justify;"}

{: style="text-align: justify;"}
Okay, war is bad, we've said it before. But is it really ? Let's take a look at the compound sentiment of the movies that have a war-related genre, compared to all other movies :

<p align="center">
<iframe src="compound_sentiment.html" width="750px" height="500px" frameborder="0" position="relative"></iframe>
</p>

{: style="text-align: justify;"}
Okaaaaay... it *is* really bad. We can first point out that, generaly, movies tend to have a more negative compound sentiment to them. However, we can cleary see that war-related movie perfom worse than other movies when it comes to happy stuff. Not only do they have less possitve sentiment in general, they also have more movies that are extremely negative. Fair enough, war is not a happy subject. Bummer.

#### Ratings

{: style="text-align: justify;"}
So, we've seen war is not a postive subject. But is it a good subject ? Let's take a look at the ratings of war-related movies, compared to all movies :

<p align="center">
<iframe src="boxplot_average_rating.html" width="1000px" height="500px" frameborder="0" position="relative"></iframe>
</p>

We see that on average, war-related movies are better rated than the average movie. akjsdhkjasdh