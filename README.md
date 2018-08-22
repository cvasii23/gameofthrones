# How to fake you have watched Game of Thrones using a Fake News Classifier, Sentiment Analysis and some heuristical considerations on psychology
In this project, we want to make the psychological portrait of the GOT chracters based only on how are they talked about. In this notebook, we are performing analytics on tweets abot  GOT characters. Our choice for describing the psychological type is the [Myers-Briggs Indicator](https://en.wikipedia.org/wiki/Myers%E2%80%93Briggs_Type_Indicator)
The Myers-Briggs Indicator takes into accout four axes:
* __E__ xtraversion <-> __I__ ntroversion
* __S__ ensing <-> i __N__ tuition
* __T__ hinking <-> __F__ eeling
* __J__ udging <-> __P__ erceiving

![Briggs-Myers Personality Types of GOT Characters](images/analysis.png)

The repository contains:
* __download_tweets.py__ script for downloading tweets about Game of Thrones characters, following the method described by Marco Bonzanini on his blog. Strongly suggest to buy [his book](https://www.amazon.de/Mastering-Social-Mining-Python-English/dp/1783552018)
* __Sentiment_LSTM-GloVe.ipynb__ is a classifier for Sentiment Analysis, with LSTM on top of GloVe pretrained embedding. We have used the _imdb_full_ dataset and got 88.5% accuracy
* __FakeNews-logistic regression.ipynb__ is a classifier to detect fake news consisting of a lLogistic Regression classifier with Naive Bayes TF-IDF features. It is a bit overfitting, nevertheless we got 95% accuracy on the test set, while using the same method as we used for the sentiment analysis has provided 93% accuracy. I learned about the fact there is a dataset from a [blogpost by Katherine Jarmul](https://blog.kjamistan.com/comparing-scikit-learn-text-classifiers-on-a-fake-news-dataset/)
* __analysis.ipynb__ is the notebook where all the magic is done. Based on the results from the Sentiments Analysis and Fake News Classifier. as well as some exploratory analysis on things like the retweeting rate, we draw all th conclusions on the Briggs-Myers profiles of the GOT characters.

* Arya: ESxx - can be Provider, Supervisor, Performer, Provider
* Bran: INTP -Architect
* Cersei: ENxx - can be Champion, Teacher, Inventor, Fieldmarshal
* Daenerys: ENFJ -Teacher
* Euron: ENxx - can be Champion, Teacher, Inventor, Fieldmarshal
* Jaime: ENTP -Inventor
* Jon: INxx - can be Counselor, Architect, Mastermind, Healer
* Sansa: ENTP - Inventor
* Tyrion: ESFJ -Provider
