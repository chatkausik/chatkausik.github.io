### Movie Recommender System ###

## Business Overview: ##

Using the small MovieLens data set, create a recommender system that allows users to input a movie they like (in the data set) and recommends ten other movies for them to watch. 

## About Dataset used ##

MovieLens 100K dataset has been used for this project. MovieLens is a rating dataset from the MovieLens website, which has been collected over some period. Stable benchmark dataset. 100,000 ratings from 1000 users on 1700 movies. Released on 4/1998. 

## A little about the dataset: ##

MovieLens data sets were collected by the GroupLens Research Project at the University of Minnesota.
This data set consists of:

* 100,000 ratings (1-5) from 943 users on 1682 movies. Each user has rated at least 20 movies. Simple demographic info for the users (age, gender, occupation, zip) About few components loaded from the package which are used in this project:

* u.data -- The full u data set, 100000 ratings by 943 users on 1682 items. Each user has rated at least 20 movies. Users and items are numbered consecutively from 1. The data is randomly ordered. This is a tab separated list of user id | item id | rating | timestamp.

* u.info -- The number of users, items, and ratings in the u data set.

* u.item -- Information about the items (movies); this is a tab separated list of movie id | movie title | release date | video release date | IMDb URL | unknown | Action | Adventure | Animation | Children's | Comedy | Crime | Documentary | Drama | Fantasy | Film-Noir | Horror | Musical | Mystery | Romance | Sci-Fi | Thriller | War | Western | The last 19 fields are the genres, a 1 indicates the movie is of that genre, a 0 indicates it is not; movies can be in several genres at once.The movie ids are the ones used in the u.data data set.

* u.genre -- A list of the genres.

## Process Flow ##

1. Load libraries
2. Load the ratings dataset and preview the first 10 rows
3. Load the movie titles dataset and preview the first 10 rows
4. Merge the two dataframes into one
5. Preview the first 10 rows of the new dataframe
6. Create a new dataframe that displays average rating (mean) for each movie in the data
7. Dreate a dataframe that shows the total ratings cast for each movie
8. Calculating the Correlation by making a pivot table (rows=userID, columsns=Movie Title)
9. Preview the first ten rows pivot dataframe
10. Create a correlation value using the 'corrwith' function in conjunction with a movie choice
11. Display the first five rows of computed pairwise correlation between rows and columns
12. Create a new variable named 'recommend' and drop all the empty values
13. Merge the ratings to the correlation table
14. Filter all movies that are correlated to 'Godfather, The (1972)' using the sort_values function
15. Merge the original movie dataset to show all fields
16. Display the recommended list dataframe to include the movie selection and ten recommended movies (Nair, 2019)

## Conclusion ##

After following the 16 steps above, I was able to produce a list of impressive movies after I selected my favorite movie of all time “The Godfather”. The list is as follows:
* Godfather: Part II, The (1974) 
* Schindler's List (1993)
* Fight Club (1999) 
* Saving Private Ryan 
* Goodfellas (1990)
* Inception (2010)
* Star Wars: Episode V - The Empire Strikes
* Back (1980)
* Reservoir Dogs (1992)
* Outbreak (1995)
* Clockwork Orange, A (1971)

To my present surprise, the recommender system actually produced 10 movies that I actually really enjoyed, with the exception of Clockwork Orange. So I guess I have a new movie
to watch this weekend.