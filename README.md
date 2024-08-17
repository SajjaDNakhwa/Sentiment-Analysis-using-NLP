# Sentiment Analysis using Natural Language Processing
#### This repository contains the code for a sentiment analysis done using Natural Language Processing and Classification models. It trains on a bunch on restaurant reviews, creates a bag of words model, and passes it through a classification model to get the predictions. 


## Table of Contents
- [Dataset](#dataset)
- [Dependencies](#dependencies)
- [Preprocessing](#preprocessing)
- [Bag of Words](#bag-of-words)
- [Training the Model](#training-the-model)
- [Learnings and Key Takeaways](#learnings-and-key-takeaways)
## Dataset
### Shape = [1000,2]
The dataset contains two columns. The first column contains restaurant reviews (in English), and the second column contains whether that review is tagged as a positive review(1) or a negative review(0).

## Dependencies
You would require the following libraries for it to run on your machine(for python or jupyter).
- NumPy
- Pandas
- re
- NLTK
- scikit-learn

## Preprocessing
Several steps have been used for preprocessing the reviews to get them in favourable format:-
- remove punctuation marks, numbers etc. (everything other than Latin letters)
- lower the case
- remove stopwords(words that do not have significant meaning or effect on the class of the review, for eg:- 'a', 'the', 'and' etc., although I have significant words such as 'not', 'no', 'doesn't' etc. which do affect the reviews)
- stem all the words to their roots(for eg:- 'love' and 'loved' should be considered the same word for processing)

## Bag of Words
The Bag of Words is a long vector which has each position set for a specific word, and it puts the number of occurences of the word in the position of that word.
The first, second and last position are resevered for the first word, second word and special words respectively. I have used the CountVectorization class from the scikit-learn.feature_extraction.text library, which creates the vector for each review. The length can be set as a parameter (here I have set it as 1500). Now we set the vectors as the X values, and the liked scores as the y-values. This can now be used in the classification models to identify the review as a positive or a negative review.

## Training the Model
After using several models, I decided to use Logistic Regression, as it gave the best accuracy metrics amongst the available classification models.
Here are some of the accuracy metrics that were calculated from my model:- 
- Confusion Matrix : [[81 16] [26 77]]
- Accuracy: 0.79
- Precision Score: 0.8279569892473119
- Recall Score : 0.7475728155339806
- F1 Score: 0.7857142857142857

## Learnings and Key Takeaways
Here are some of the most interesting things that I learnt while working on this project:-
- Basics of Natural Language Processing and the intuition behind it
- Various use cases of NLP (which I wish to work upon in the future!)
- Cleaning and formatting textual data
- Understanding the Bag Of Words model and its creation
  
Final Thoughts :- This was a really fun project that exposed me to the fascinating domain of Natural Language Processing. I wish to further improve my models after diving deep into it. Any feedback or criticism is gladly accepted. Contributions are readily welcomed, please fork the repository and send a pull request to do so.

  


