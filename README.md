# search_engine_movie_recommendation
A search engine content-based recommender system that recommends movies similar to the movie the user likes and analyses the sentiments of the reviews given by the user.

## Overview
The movies are recommended based on the content of the movie you entered or selected. The main parameters that are considered for the recommendations are the genre, director, and top 3 casts. The details of the movies, such as title, genre, runtime, rating, poster, casts, etc., are fetched from https://www.themoviedb.org/documentation/api . The reviews of each individual movie given by the users are "web-scraped" from the IMDB website with the help of `beautifulsoup4` , and the reviews are subjected to sentiment analysis, where the model predicts whether the review is positive or negative.

## How To get API Key?

Create an account in https://www.themoviedb.org/. Once you successfully created an account, click on the API link from the left hand sidebar in your account settings and fill all the details to apply for an API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your API sidebar once your request has been approved.

## How to Run The Project 

1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the requirements.txt file with the command pip install -r requirements.txt
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
4. Replace YOUR_API_KEY in both the places (line no. 15 and 29) of static/recommend.js file and hit save.
5. Open your terminal/command prompt from your project directory and run the file main.py by executing the command python main.py.
6. Go to your browser and type http://127.0.0.1:5000/ in the address bar.
7. Tdaaaa That's it



## Application Demo:-
![image](https://user-images.githubusercontent.com/86946068/200770920-8c7b7e0e-c711-4586-9f45-a2d2d65e94a0.png)

![image](https://user-images.githubusercontent.com/86946068/200771049-63f27596-0662-4cff-8230-e5baf7c85273.png)
![image](https://user-images.githubusercontent.com/86946068/200771135-1836f145-e4fc-44f5-9b33-14a572d116ba.png)
![image](https://user-images.githubusercontent.com/86946068/200771595-2ffaf98e-04e2-4520-9a9c-d4a749ae685e.png)
![image](https://user-images.githubusercontent.com/86946068/200771664-d62bbe26-f81d-4067-84d3-a8e6103781de.png)
![image](https://user-images.githubusercontent.com/86946068/200771818-97717e40-7279-4792-bd1c-b8f29adef795.png)
![image](https://user-images.githubusercontent.com/86946068/200772060-1cccbf7c-7307-455a-9b33-783774b265cb.png)


## Similarity Score:
How does it decide which item is most similar to the item user likes(or selects in our case)? Here comes the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

## How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.


![70401457-a7530680-1a55-11ea-9158-97d4e8515ca4](https://user-images.githubusercontent.com/86946068/200774400-73ef61f3-6b7b-4811-ae48-22fa9d93cea4.png)

More about Cosine Similarity : https://www.machinelearningplus.com/nlp/cosine-similarity/ <br/>

#### Sources of the datasets
1. https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset
2. https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset
3. https://en.wikipedia.org/wiki/List_of_American_films_of_2018
4. https://en.wikipedia.org/wiki/List_of_American_films_of_2019
5. https://en.wikipedia.org/wiki/List_of_American_films_of_2020
6. https://en.wikipedia.org/wiki/List_of_American_films_of_2021
7. https://en.wikipedia.org/wiki/List_of_American_films_of_2022

