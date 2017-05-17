# Twitter-data-mining
Retrieve tweets from Twitter via Rest API and assign them a class label using a Support Vector Machine

training_set.txt is a pre made training set to use with the Support Vector Machine. It contains tweets mostly relating to automobiles or what you would expect to find in car queries. To collect tweets, run carQuery(num) where num is the number of tweets you want to collect per car, per city. The tweets will be written to four files, each corresponding to one of Albany, New York, San Fransico, and Miami.

Using the Support Vector Machine, you can predict the class label of your tweets by running the SVM like so:

  svmModel("training_set.txt", "alb.txt", "output.txt")
  
where alb.txt is the testing set and can be swapped for any of the other input tweet files. This function will score your tweets using the training set as a reference and write the positive ones to the output file. A class label of 1 is positive, while a class label of 0 is negative. 
