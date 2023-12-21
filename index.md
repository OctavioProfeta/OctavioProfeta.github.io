---
layout: page
title: Societal fears and movies
cover-img: /assets/img/path.jpg
---

{: style="text-align: justify;"}
Here, at WorkingTeam2023™, we want to know what are societal fears. So, what are we *afraid* of ? We are talking about societal fears, like the fear of a global pandemic or the fear of a nuclear war, not the fear of spiders or the fear of heights. [The Chapman University](https://www.chapman.edu/wilkinson/research-centers/babbie-center/survey-american-fears.aspx) conducts yearly studies based on surveys in the United States of America, giving us a starting point for an answer. By taking a look at the results of the surveys from 2018 to 2023, we have chosen to consider 7 majors global fears, which are the following :
*   War
*   Global Warming or Climate Change
*   Terrorism
*   Pandemics or Goblal Disease Outbreak
*   Economic Collapse
*   Technology Advancement
*   Aliens

We want to know whereas these subjects appears in the cinema industry, and whether the movies treating them know some kind of success, aswell as point geographical and temporal trends.

## The datasets

We will be using the [Movie Summary Corpus](https://www.cs.cmu.edu/~ark/personas/), which is a dataset containing more than 42'000 movie plot summaries, aswell as some other corresponding metadata. Added to that is the IMDb, which contains information about film's box office.

## Ready, set... analyse !

Hold on, hold on ! Let's first take a look at our data, and start by first seeing how many films have been produced through the years 

<img src="/assets/img/movie_release_years.png" alt="Movie Release Years">

We clearly see the trend here : The movie industry has grown largely during the recent years, more specificaly at the start of the 90s ! What about country movie production ? Which country is the more productive ?

<img src="/assets/img/top_10_countries.png" alt="Country Top 10">

No surprises here, the United States of America is by far the most productive country, followed by India with Bollywood and the United Kingdom, almost tied for second place. The USA are responsible for more than 39% percent of the movie produced ! We need to keep in mind that the analysis we will be doing will be biased towards the USA.

## Let's get down to business

Let's start by analysing which are the recurrent topic in movies. By using topic detection algorithms on the plot summaries, we can extract major subjects from the movie plots.

<iframe src="lda.html" width="750px" height="860px" frameborder="0" position="relative">Genre plot</iframe>

By setting λ to 0.5, we can interpret the following topics :

1. Drama and/or Relationships
2. Horror
3. Detective and/or Crime
4. War
5. Musical
6. Western
7. Supernatural
8. Undetermined, related to animals or creatures

War appears naturaly in the most reccurent topics. It is also on of the most salient terms, all topic cofounded. This indicate an interest for war in itself, but also for the consequences of war, such as the loss of loved ones, the destruction of the environment, etc. This implies that war is one of the most important societal fears.