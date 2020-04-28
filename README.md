# "Real or NOT" : NLP to Identify Public Emergency Related Tweets (Part 1)


## Introduction

Being able to predict which Tweets are about real Public Emergencies (*eg Earthquakes, Floods, Terrorist Events*) and which ones are not. 

(The words 'Pubic Emergency' and 'Disasters' have been used interchangeably)

> Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

> But, it’s not always clear whether a person’s words are actually announcing a disaster. 

<BR>

*Source: [Real or Not? NLP with Disaster Tweets, A Kaggle Competition](https://www.kaggle.com/c/nlp-getting-started/overview)*

<BR>

The dataset has the contents of the Tweet (`text` variable), the location from where the Tweet was posted (`location` variable), and a keyword associated with the Tweet (`keyword` variable). 

The model will be built based on the contents of the Tweet, as from a domain standpoint, the location and the keyword information may not always be available (in the situation this algorithm is actually deployed) 


<BR>

### Goal

This is the second exploration of the dataset. In the 1st attempt, I had used an ML based approach *(an ensemble of ensemble methods)* yielded 80% accuracy on the test data. 

The goal is to get a better model (~83%) using one or an ensemble of multiple Deep Learning models.


<BR>

### Approach & Results

In this notebook, I have tried out two variants of LSTM based approaches - one with pretrained embeddings and one without. The model which incorporate pre-trained embeddings from the Glove model had an accuracy of 83% on the test set.

I have also created a set of helper functions for data preprocessing, vocabulary building and creating embedding matrix from pre-trained embeddings.

The best performing model had an accuracy of 83% in the test data

<BR>

### Next Steps

The next step is to get better results by trying out a few more approaches which have been listed below. **These will be incorporated in the Second edition (Part 2) of the notebook.**

1. An `Ensemble` model (dense - word focussed + lstm - sequence focussed)
2. An `N-GRAM` model (especially n = 2)
3. Using `Attention` based frameworks
4. (Optional) A `Functional` model (using Keras functional API)
