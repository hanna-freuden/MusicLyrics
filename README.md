# Chart rank prediction using song lyrics and musical features      

## Problem statement
Most would agree that lyrics are an important part of pop songs. However, are they also predictive of the chart ranking of the song? And if so, what are text features that are most predictive? And are they more or less predictive than the music itself? This project aims at answering these questions.
 
Artists or record companies might want to predict sales of their newly produced songs or even produce songs using the proven characteristics of successful songs. In terms of musical features, [research has shown what makes a successful song](https://royalsocietypublishing.org/doi/10.1098/rsos.171274), for instance, top 100 ranked songs were more likely to be rated ‘happy’ and sung by a female voice. However, success in terms of lyrics has seldom been explored. 
 
## Data sources and methods
First, I use lyrics of pop songs contained in the Billboard Year-End Hot 100 between 1965 and 2015 by Kaylin Pavlik ([link](https://github.com/walkerkq/musiclyrics)) as well as musical features for the corresponding songs obtained from the [Spotify API](https://developer.spotify.com/), containing 12 audio features for each track, including acousticness, liveness, speechiness and instrumentalness, energy, loudness, danceability and valence (positiveness), and descriptors like duration, tempo, key, and mode. I use NLP techniques, including word2vec and tf-idf vectorization to generat text features. Then, I apply ML classification algorithms (Logistic regression, Random forests, Boosted trees, SVM) with tuned hyperparameters and 3-fold cross-validation to predict class membership, where class refers to the top 50 ranked songs. 



<p align="center">
  <img src="https://user-images.githubusercontent.com/51961909/137318776-5aa0bc7a-e76c-4af5-88a6-add8cd7d9800.png" />
</p>
