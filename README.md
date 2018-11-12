# Twitter Hate Speech Classifier
Classifies tweets as containing offensive language or hate speech.

<!-- ### Motivation
Why make this repo? -->

### Install

This project requires **Python 3** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas (0.23.4)](http://pandas.pydata.org/)
- [PyTorch (0.4.1)](https://pytorch.org/)
- [NLTK (3.3)](https://www.nltk.org/)
- [matplotlib](http://matplotlib.org/)
- [Jupyter notebook](http://ipython.org/notebook.html)

### Dataset

The datasets is a collection of tweets labeled as offensive language and hate speech by CrowdFlower users.

https://github.com/t-davidson/hate-speech-and-offensive-language

This data was originally used for Thomas Davidson, Dana Warmsley, Michael Macy, and Ingmar Weber. 2017. "Automated Hate Speech Detection and the Problem of Offensive Language." ICWSM [[view paper]](https://aaai.org/ocs/index.php/ICWSM/ICWSM17/paper/view/15665)

### Data Preparation
Tweets were tokenized using NLTK's Twitter-aware [TweetTokenizer](https://www.nltk.org/api/nltk.tokenize.html#module-nltk.tokenize.casual). Rather than learning new embeddings, I used pre-trained embeddings from [GloVe's 200d Twitter word vectors](https://nlp.stanford.edu/projects/glove/).

### The Model
The embedded tweets were passed in batches into a bidirectional LSTM classifier.
