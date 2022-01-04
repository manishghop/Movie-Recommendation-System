# Movie-Recommendation-System
CS680-Fall 2020 Project


## You can follow along using the Notebook File


As a final project for CS680, I had a chance to apply machine learning models on a real world problem. The problem statement was similiar to the famous Netflix challenge. The goal of the problem is to come up with a recommendation system that recommends movies to both a new user or an existing user. Recommending movies to a new user can be tricky as we have no information of his taste whatsoever. Overall, I had fun in solving this problem as I got to learn several things.


## PACKAGES
<h1>You need to install following packages first</h1>
<ul><li> tqdm</li>
<li>sklearn </li>
<li>pandas </li>
<li> numpy </li>
<li> scikit-surprise </li>
<li> scipy </li>
<li> pylab </li>
</ul>
<p>Go ahead and pip install above packages.</p>

```
pip install sklearn
pip install pandas
pip install numpy
pip install tqdm
pip install scikit-surprise 
pip install scipy 
pip install pylab 
```


<h2>To run the file simply run the notebook, it is highly recommended that you run it on google colabatory. </h2>





## DATA-GATHERING

We gathered the data from the kaggle dataset which lets us access movies listed on imdb website from any time-period.
The dataset was open-source and was downloaded from kaggle dataset. The dataset was named imdb listed movies.




## DATA PRE-PROCESSING

In this step we look for any discrepancies in the dataset. After proper analysis, many missing values were found in different columns. The
first attempted solution was to fill these values with the data interpolation techniques and the data was just enough to perform accurate filling of
values. The genres were seperated with a special characters so we had to deal with that. A lot of the rows were empty as a result we had to either remove those columns(if they were insignificant) or had to perform certain pre-processing techniques.
We performed standard scaling to ensure that we normalize the data-set.



## FEATURE-ENGINEERING

We extracted several features from the dataset. We extracted the year of the movie realeased from the title of the movie. We extracted the relationship of the movie having prequel or sequel from its title. After we finished with the feature extractions, we removed redundant features using pearson correlation.


## MODEL SELECTION


Our problem was a recommendation problem, so we used Collaborative Filtering and Context-Based Filtering. 


Write something about Collaborative filtering and context based filtering here:

## Collaborative Filtering:

The technique is called **Collaborative Filtering**, which is also known as User-User Filtering.
As hinted by its alternate name, this technique uses other users to recommend items to the
input user. It attempts to find users that have similar preferences and opinions as the input
and then recommends items that they have liked to the input.

- this method involves taking the view of a group of users.
  For the implementation, I shown it for the userid=1(I'm making recommendation for user-1), similarly we can recommend the movies to anyone.

## Context-Based Filtering:

A content based recommender works with data that the user provides, either explicitly
(rating) or implicitly (clicking on a link). Based on that data, a user profile is generated,
which is then used to make suggestions to the user. As the user provides more inputs or
takes actions on the recommendations, the engine becomes more and more accurate.

- It is recommended that we have a pre-existing profile for a user. This algorithm doesn't recommends movies to a new user. In content based filtering we have to know the content of both user and item. Usually we construct user-profile and item-profile using the content of shared attribute space. For example, for a movie, you represent it with the movie stars in it and the genres. For user profile, you can do the same thing based on the users likes some movie stars/genres etc.



- let's assume that user 1 has watched these 100 movies and we try to recommend him more movies and try to see if our recommendation matched his watched movies.
Here we made and assumption that if he gave a rating that means he watched the movie
Here we took userid=1, that is we make recommendation for user-1. We can make recommendation to any user.


## MODEL EVALUATION & COMPARISION

We can observe from the above graph that RMSE of content-based filtering is smaller than the RMSE of collaborative-based filtering.
And it can be proved in general that individual preferences are always better than the group preference.

 

## Results:

Out of the two content based filtering and collaborative filtering, content based filtering out-
performed collaborative filtering by a huge margin as the RMSE(Root Mean Square Error)
of the content-based filtering was much smaller than the RMSE of the collaborative-based
filtering. This makes sense, as items predicted by content based filtering are more similiar
to users likings as they make more sense since they are based on user’s preferences. On the
other hand collaborative filtering underperforms as it’s based on a group’s choice. There
might be cases when an item liked by a user is never recommended to him by collaborative
filtering.For reference,the code can be found on the notebook attached with this report


## MODEL DEPLOYMENT

A this was a school project and there was no requirement to push the model on a web application, I decided to leave it as a notebook file.

<!--
## This below block is for school's requirememt.

In getdata file we are creating a table data and storing the values from the dataset
also we are creating a dataset table to store 3 fields that we are using for prediction 
along with profit/loss. 
Then in prediction file we use bernoulie naive bayes algorithm to perform a binary 
classification, load the data from the data set that we created(dynamically) and 
based on the details of user input match for the similiar data point in dataset
give result.-->
