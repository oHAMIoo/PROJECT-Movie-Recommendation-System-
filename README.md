# PROJECT-Movie-Recommendation-System-
Data Mining, Data Exploration, Logistic Regression, Classification Tree, Tree Path. 

Movies are considered the primary way of entertainment around the world.
So for my project, I decided to study and analyze the ratings, reviews data from users' behaviors and personal preferences to give them more accurate movie recommendations. The main objective is to predict the probability of a movie being successful, allowing the movie recommendation system to determine whether a movie will be successful or not with viewers. The system will be using two predictive models: A logistic regression and a classification tree to get the most accurate predictions for the accuracy score of the logistic regression analysis.
I am specifically interested in recommending movies that have become more relevant, in other words, movies with ratings that are above the average rating:</br>  
**A movie title is successful when it has a rating above 8 points. Any title in this bracket would be considered a high-quality outcome, therefore i will focus this model to predict the probability of a movie title achieving a rating above 8.0 rating points.**

IMDB website is an online database of information related to films, television programs, home videos, and streaming content online. I used Beautiful Soup, a Python library, to get data out of HTML, XML to crawl raw text data from IMDB and including variables such as userid, rating, reviews, genres, and run time. I crawled about 220000 records from IMDb, containing about 220000 reviews and user ratings from about 100000 users and information of about 11055 movies and the corresponding information such as movie certifications (R, PG-13), movie runtime (98min, 150 min), overall ratings, and genres.</br>  
**To better fit the models, I did some cleaning work to remove some missing values, dummies coding, and variable transformation into binary data. Moreover, I used a heatmap to detect relevance between the dependent variable, the numerical variables, and the categorical variables, accordingly.**

The logistic regression's coefficient estimator, ROC curve (true positive rate with the false positive rate), and accuracy score have proven to be very useful in determining the most important movie variables. Moreover, by reducing the number of predictors from 20 predictors to only 6 predictors, I was able to make better decisions. 
The 6 most important predictors: [Drama],[Comedy],[Romance], [Action],[Animation] and [Sport] which were determined using their coefficient and ranks.

After dropping all the irrelevant movie genres from the preprocessed dataset in the logistic regression, I then used the classification tree to get a more straightforward meaning and read the data output. All movie names that have a rating greater than 8 points are most likely to generate a positive outcome and a positive sentiment for the viewers. 

The classification tree generated a list of movies to recommend using its path and leaf nodes structure.</br>  An example: **Leaf node ID = 13, sample = 8,  value = [0, 8], class =  1
Path = ['Drama <= 0.5', 'movieGenre_Action, Adventure > 0.5', 'movieName_Batman <= 0.5', 'movieName_Indiana Jones and the Temple of Doom <= 0.5', 'movieName_Rambo III <= 0.5']**</br> 
Reading: **If 8 viewers fall in the category where the genre ‘Drama’ is not really important where its probability is less or equal to 0.5. In addition, these viewers like the movie genre Action and Adventure combined. We can conclude that there is a 100 percent chance that all 8 viewers will rate the movie Titles: “Batman”, “Rambo 3” and “Indiana Jones and the Temple of Doom” greater than 8.0 points**</br>


These translations using the classification tree’s English rules were made easier using the Tree’s path which I have attached screenshots ("Tree Path & Leaf Nodes") in this repository. It is important to note that for this model I have only kept the class outcome of my interest where: **Overall Movie Ratings that are greater than 8.0 points are represented by class =1.</br> Class = 0 are considered 'NOT successful' movies to recommend**</br>

Finally, I exported to a CSV file, the output of movie titles from the classification that are considered titles that new viewers are most likely to enjoy.



 
