# ContentBased_RecommenderSystem

  This repository explores different techniques of word embeddings and how they differ in performance on a content based recommendation task. More specifically, the task involved is recommending a number of songs based off of a list of track names inputted by the user, essentially a playlist. The content being used is the lyrics of the song itself, disregarding any audio features. Two of the word embedding techniques (TFIDF with Truncated SVD applied for dimensionaliy reduction) were tested with different vector dimension sizes, to explore how dimensions impact performance. Also, each model was tested with different playlisy sizes in order to see the impact of input and output size on performance.
 
  Two datasets are used, one for the lyrics word embeddings, and another to evaluate the performance of the model. The first dataset has 18000 songs, 11000 of them being unique and usable. The second dataset (spotify dataset) consists of 1 million playlists with 2 million unique songs. We extracted playlists that had atleast 10 intersecting songs with the first dataset. For each playlist, the song set was split 70/30, th the larger portion being the input for the recommender system and the small portion being the y_true value that is compared to the recommenmded songs of the input playlist. The evaluation metric we used was the average cosine similarity of a given model tested on 100 playlists. 

  The word embedding techniques used were reduced tfidf, doc2vec and sbert. These three techniques vary in terms of methodology and mathematical background. 

  Results indicate sbert performs best, compared to non significant average cosine similarities for reduced tf_idf and sbert.  
  
  Song_Recomemnder notebook displays most of the code, showing how the recommender class works and how evaluation is done.
  
  Evaluation_Dataset notebook displays how the evaluation dataset was processed by finding the intersecting songs, while retaining the playlist structure. 
