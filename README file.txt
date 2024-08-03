README file

Next To Be Read

Book recommendation system
	We all run in to the question of what is next to be read. Either we have a stack or about to go to the library/bookstore or download a new audiobook. There are currently a few recommender systems out there but personally they have brought me frustration. So here is my whack at it to help those like me. 

1. Data
	Goodreads is a book application. With one hundred thousand books in the file from Kaggle there was sufficient information to work with. The dataset can be found- https://www.kaggle.com/datasets/mdhamani/goodreads-books-100k.

2.Method
There are three main types of recommenders used today:

Content-based filter: Recommending future items to the user that have similar innate features with previously "liked" items. Basically, content-based relies on similarities between features of the items & needs good item profiles to function properly.

Collaborative-based filter: Recommending products based on a similar user that has already rated the product. Collaborative filtering relies on information from similar users, and it is important to have a large explicit user rating base (doesn't work well for new customer bases).

Hybrid Method: Leverages both content & collaborative based filtering. Typically, when a new user comes into the recommender, the content-based recommendation takes place. Then after interacting with the items a couple of times, the collaborative/ user based recommendation system will be utilized.

We will be doing a Content based filter for this rendition. In the future would like to evolve to hybrid to get a large variety pool. This will have us focusing on the genre more than ratings. 

3. Data Cleaning

The columns that we will want to really focus on are the genre, rating, title and description. This allows us to focus on recommending based on the genre with those ratings. 

So first we need to normalize and clean up the columns. We dropped the columns not relevant.

Dropped any rows with missing title as this is not helpful(it was only one record so no impact). Also dropped the rows with missing genre information. This was about 10% still leaving a large amount of data to work with. Also dropped any duplicates. 

We filled in missing descriptions with 'No description available.'.

Cleaned up the genre column to standardize the spelling and language.

4. EDA

Now we are going to visualize everything so it isn't just data. We look at the rating distribution, genre frequency and a correlation matrix. Next Checking the ratings by genre as this information is important to us. This is also where we have broken out the genre column in to a genre hierarchy to handle the large amount of options input. 

5. Algorithms & Machine Learning

Now we look at two different models. First we look at the content based recommendations. Second we look at collaborative. From here we see what works best right now. We created some simulated user data for better understanding. 

6. Which dataset to choose

We have selected the content based recommendations model. This is the best one for right now. It shows a great success rate. 

8. Predictions

Now we can see the predictions that model presents us with top 10 based on previous ratings.

9.Future Improvements

In the future we can make this a hybrid recommender taking the collaborative information along with the content from the individual. 


	