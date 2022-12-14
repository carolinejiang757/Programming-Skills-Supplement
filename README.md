# Programming-Skills-Supplement
This piece of code is an individual part of a collaborated project studying the fluctuation in the outcome of pre-trained Natural Language Processing models


## Project Objective:
Pre-trained language models are models that are trained with one task but the result parameters can be used in other tasks. Some popular pre-trained language models include BERT and RoBERTa. One application is to use language models to analyze intrinsic gender bias by predicting the possibility of “he” or “she” in a particular masked sentence describing a certain occupation. For example, the higher probability of “He is a doctor” than “She is a doctor” shows a gender bias associated with one’s occupation. 

However, the bias metrics designed for the RoBERTa model are based only on one single checkpoint that was made public. When analyzing other intermediate checkpoints, we find significant fluctuation in the bias metrics, which causes concern for the fairness of the comparison between pre-trained checkpoints. Our project wants to further study the range and cause of the fluctuation to evaluate the reliability of the models across different checkpoints. 

## What this piece of code does:
This piece of code is my independent work and focuses on identifying the prior of gender bias in the pre-trained model. The RoBERTa model is trained using a large corpus that includes articles, stories, news, and any other forms of text available on the internet. Regardless of occupation, there is an intrinsic inequality between the total numbers of “he” and “she” mentioned in the training text. In order to offset this bias in the training set, we need to determine the prior and separate its effect from the actual gender bias we want to focus on. This piece of code determines the prior by taking the pre-trained RoBERTa model and calculating the ratio between the probability scores of two gender pronouns in template sentences with masked occupation.
