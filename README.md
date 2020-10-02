# Clustering my songs on Spotify and  mood prediction
# Detailed Information
If you want to know more about the process, please make time to read an article I wrote explaining some crucial steps:
https://medium.com/@chingisoinar/cluster-your-liked-songs-on-spotify-into-playlists-of-similar-songs-66a244ba297e
# About:

I am going to cluster my saved songs on Spotify. Clusters are going to be derived due to KMeans clustering model, which was trained with Spotify Dataset 1921-2020 found on Kaggle. Spotify Dataset 1921-2020 contains more than 160 000 songs that were released during the period of 1921-2020. Aditionally, all the clusters derived will represent a certain mood I have while listening to my music. Furthermore, I am going to get my Spotify recommendations and classify recommended songs using a trained classifier. Finally, it can be used to predict my mood and suggest new songs that fit my current mood.

Get started:[https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks)

## Clusters

- Cluster 0 is tourned out to be very high in terms of speechiness since the mean value over all songs is 0.87. If the speechiness of a song is above 0.66, it is probably made of spoken words, a score between 0.33 and 0.66 is a song that may contain both music and words, and a score below 0.33 means the song does not have any speech. Moreover, it is low in instrumentalness but pretty high in danceability. I assume there are mostly rap songs.
- Cluster 1 is relatively high in danceability and energy but low in instrumentalness. I expect to see a lot of energetic songs there.
- Cluster 2 is very high in acousticness but low in instrumentalness and loudness. Moreover, it has quite high danceability magnitude. Therefore, I expect to see more calm, perhaps sad, songs. 
- Cluster 3 is the highest in acousticness and instrumentalness but the lowest in speechiness.
- Cluster 4 is quite high in instrumentalness and energy and average in danceability.

![Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/Clusters.png](Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/Clusters.png)

## Classifiers

There are four models compared in terms of accuracy, which are KNeighborsClassifier,RandomForestClassifier, Support Vector Classifier and Naive Bayes. Support Vector Classifier turned out to be the best model in terms of accuracy, which made up roughly 0.998, hence we will be using it for future classification.

![Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/SVC_confusion_matrix.png](Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/SVC_confusion_matrix.png)

## My saved songs

The following figure sums up my preference in terms of features provided 

![Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/mean_features.png](Clustering%20my%20songs%20on%20Spotify%20and%20mood%20prediction%2064955a851fe849f8864f6b4047c1b582/mean_features.png)

> I concluded that the vast majority of my saved songs are energetic meaning that they are high in danceability and energy. I also like calm/romantic songs from time to time.
## Links to my playlists created
- CLuster 0(rap):https://open.spotify.com/playlist/6dL6xOCcema8DUSzYLfx06
- Cluster 1(Energetic/dancing):https://open.spotify.com/playlist/0LlIHqBd2zOHemZ3c7j6Ov
- Cluster 2(Calm/Romantic):https://open.spotify.com/playlist/4mF1KkRP5YITPTf1dakXJP
- Cluster 3(Studying/Thinking):https://open.spotify.com/playlist/4xRgEf6Y4iBs3I3WNNofMr
- Cluster 4(Chill):https://open.spotify.com/playlist/5FtCtZ5QrpQDlXxIB9DMEi
