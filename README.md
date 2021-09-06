This program creates a sentiment score for a body of text stored in a dataset and returns the score both to the user as a percentile.

The program scores the text in three different ways:

As it is presented in the dataset as one big body of text
As one big body of text with stop words removed
Each sentence individually
Libraries:
Natural Language Toolkit
Matplotlib

How it Works & Results:
The program first reads in the input data and formats and stores it in three ways:

As a raw string
As a string without stop words, this is done by pulling a dictionary of stop words from the Natural Language Toolkit data library and comparing this to the input string as a list of words to remove all matches.
As a list of sentences, this is done by using PunktSentenceTokenizer which runs an unsupervised algorithm to detect and seperate sentences. In many cases you can't just split the data along periods since in many cases including this one there may be instances where periods don't denote the end of a sentence ("Dr., Mr., etc") so a tokenizer is required.
The actual calculation of sentiment score is done using nltk's VADER(Valence Aware Dictionary for Sentiment Reasoning) model.
Vader uses heuristics such as punctutation, capitlization, impact sentiment, negation, and conjunctions to calculate the tone and sentiment of text.

Four doubles are returned as the sentiment score for the data. The first three are the negative, neutral, and positive numbers.
These all add up to 1 and can be displayed as a percentage graphically.

The fourth metric is the compound score which is the aggregated score. This is calculated by summing the valence score(positive, negative, and neutral scores) for each word and the normalizing it between -1 and 1. The higher a compound score the more positive the text is overall.
