# Movie-Recommendation-System
CS680-Fall 2020 Project


## You can follow along using the Notebook File


As a final project for CS680 I had a chance to apply machine learning models on a real world problem. The problem statement was similiar to the famous netflix challenge. The goal of the problem is to come up with a recommendation system that recommends movie to both a new user or a existing user. Recommending movies to a new user can be tricky as we have no information of his taste whatsoever.

# stock_direction_predictor
Stock Market Direction Predictor

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
pip install pyqt5
pip install sklearn
pip install pandas
pip install numpy
pip install dbConnect
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
values. The genres were seperated with a special characters so we had to deal with that. A lot of the rows were empty as a result we had to either remove those columns(if they were insignificant) or had to perform certain .
We performed standard scaling to ensure that we normalize the data-set.
There were no missing values as the yahoo api does it's job exceptionally well.




## FEATURE-ENGINEERING

We extracted several features from the dataset. We extracted the year of the movie realeased from the title of the movie. We extracted the relationship of the movie having prequel or sequel from its title. After we finished with the feature extractions, we removed redudant features using pearson correlation.


## MODEL SELECTION


Our problem was a recommendation problem, so we used Collaborative Filtering and Context-Based Filtering. 


Write something about Collaborative filtering and context based filtering here:


## MODEL EVALUATION & COMPARISION

Out of these two, Naive Bayes Model preformed better.

Results:



## MODEL DEPLOYMENT

AS this was a school project and there was no requirement to push the model on a web application, I decided to leave it as a notebook file.

<!--
## This below block is for school's requirememt.

In getdata file we are creating a table data and storing the values from the dataset
also we are creating a dataset table to store 3 fields that we are using for prediction 
along with profit/loss. 
Then in prediction file we use bernoulie naive bayes algorithm to perform a binary 
classification, load the data from the data set that we created(dynamically) and 
based on the details of user input match for the similiar data point in dataset
give result.-->
