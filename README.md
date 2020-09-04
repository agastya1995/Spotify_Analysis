# Readme #

Our objective is to make an artist recommendation system, based on the data available in [Kaggle's Spotify Dataset](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks?select=data_by_artist.csv).

The user will input an artist, and the program will return the 10 most similar artists. 

Methodology:
The recommendation system is based on 3 parts:
1. The genre of the artist
2. The artist's popularity
3. The artist's debut year

Steps:
1. We began by filtering the data based on the genre of the artist. All the other artists who don't share any genre in common are eliminated. Similarity is calculated using Jaccard Score.
2. Next, we calculated the similarity of the other artists to the input artist, by calculating the difference in the genre jaccard similarity score, the popularity and the debut years.
3. After scaling these differences (using the Min-Max scaler), we calculated the proximity of each artist to the main artist. The lower the final score, the closer the artist.
4. The top 10 closest artists are returned as the recommendations.
