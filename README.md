# classifying_genres
Classifying Genre of Popular Songs - a comparison of different models - Assignment of the MachineLearning class in my Computer Science Master at IE Univeristy

There are plenty of articles online in which people attempt to predict the popularity of a song based on a range of metrics. We thought it would be interesting to try and predict the genre of a song based on these metrics. One would expect that songs from a genre share similar characteristics. This could help to categorise songs from unknown artists with those characteristics. The dataset that we used is provided by Spotify, it contains ~40.000 tracks from 1921 to 2020 with 20 columns that include information about musical compositions. The genres the songs come from are Pop, Rock, R&B, Latin, Rap and Edm.


In the analysis we compared the most common supervised classification models (KNN, LogRes, SVC, Random FOrrest) and add in a multilayer perceptron.

The best performing model has been the random forest without any scaling of data.

The models were evaluated based on their accuracy score. All models were trained on the training data and tested against the test data. 
The best KNN accuracy is: 0.895 and was achieved with scaled data Grid Search using the following parameters: {'metric': 'manhattan', 'n_neighbors': 21, 'weights': 'distance'}. 

The best SVC accuracy tuned with Grid Search and using scaled data is: 0.987, with the following parameters {C: 10, kernel: linear}. 

The best Random Forest accuracy is 0.9997 and was achieved with unscaled data and using Grid search with the following parameters {'n_estimators': 600, 'min_samples_split': 5, 'min_samples_leaf': 1, 'max_features': 'auto', 'max_depth': 80, 'bootstrap': True}


The best Neural Network accuracy was 0.999 using scaled data with the following settings {neuron hidden layer: 100, solver: adam, learning rate : adaptive, unit function: rectified linear}
