# imdb-bert-sentiment
Sentiment analysis on IMDB movie reviews using BERT embeddings and Logistic Regression.

# IMDB BERT Sentiment Analysis

In this project, I worked on sentiment analysis using IMDB movie reviews.

Instead of using the raw text directly in a machine learning model, I first converted each review into numerical features using BERT embeddings. These features were then used as input for a Logistic Regression classifier.

The general workflow is:

```text
IMDB review
→ BERT tokenizer
→ BERT embeddings
→ 768-dimensional feature vector
→ Logistic Regression
→ positive / negative

For the first experiment, I used a subset of 1,000 reviews to keep the computation time manageable.
Libraries Used
- pandas
- numpy
- torch
- transformers
- scikit-learn
Notes
BERT is not used as the final classifier in this project.
It is used as a feature extractor to generate embeddings from the review texts. The final sentiment classification is performed with Logistic Regression.
The IMDB Dataset.csv file is not included in this repository.
