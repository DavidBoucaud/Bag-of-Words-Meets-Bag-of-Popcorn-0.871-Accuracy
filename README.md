# Bag-of-Words-Meets-Bag-of-Popcorn-0.871-Accuracy-
This is a pretty basic NLP + Classification method. Basic text cleanning -> TfidfVectorizer -> MaxAbsScaler -> Logistic Regression model.

## Introduction
  For fun, I decided to attemp this classic Kaggle challenge (found here: https://www.kaggle.com/c/word2vec-nlp-tutorial). I included notes in the code file, which are a more inclusive walkthrough than what I will provide here.
  
 ## The process
  As described above, we begin by cleaning the data with a basic lemmatization process. I finalize the clean with Beautiful Soup which I really encourage as it is stronger and simpler than any re process. After that, the text is cast to a TfidfVectorizer, normalized, and cast into a logistic regression.
  If you can believe it, this code comes at the end of a ton of grid searching. I tried many normalizers, as well as classifiers (Kmeans Clustering, Random Forest). Although it isn't the "coolest" way to do things, Logistic Regression performed the best so I ran with it.
  
 ## Worth noting
  I would be a bad data science student if I don't mention that there are some obvious better ways to push this into 90% territory (I already made my submission, so I'm keeping my project as is). For one, setting a minimum threshold on Tfidf (ie. 2 words) cleans out a lot of noise and would certianly improve accuracy. Furthermore -I'd be willing to bet that Nearal Network techniques such as an RNN are far more capable at sentiment detection than this program.
  The big problem with sentiment analysis with Tfidf+Logistic Regression is that it does not consider the sequence of words. A phrase like "not very good" is interpreted as "good" rather than "bad". This is one of the strengths of RNN, which will pick up on negation effectively.
