ACM Fall 2021 Research Coding Challenge

For this challenge, I calculated the overall sentiment score of the input text. To facilitate analysis, I edited the input.txt file so that each line is a sentence. I originally planned to replace the question mark and exclamation mark with a period and get rid of it. However, as will be explained later, they are too important. 
 
I used vaderSentiment. This library has a large data set already included. When you pass a sentence through the parser, it returns a dictionary with four keys. These keys are positive, neutral, negative and compound. Compound keys are used to determine the overall feeling of the sentence. A composite score greater than or equal to 0.05 can be considered a positive emotion. Less than or equal to 0.05 is negative and between the two it is neutral. 
 
My program reads the input file one line at a time and passes that line to the parser. Generate a dictionary with four keys and compare the composite punctuation with the previous punctuation. Based on the score, a positive score, a negative score, or a neutral score is increased by one. Also save the total. After reading all the lines, calculate the total percentage of positive, negative, and neutral scores. The highest of the three is the overall mood of the text. I also save the scores for each row in a separate file. 

The Resource I used - Simplifying Sentiment Analysis using VADER in Python 
https://medium.com/analytics-vidhya/simplifying-social-media-sentiment-analysis-using-vader-in-python-f9e6ec6fc52f
