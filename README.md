## Fine-Tuning Result

In the final experiment, `bert-base-uncased` was fine-tuned directly on the IMDB sentiment classification task.

The dataset was split into training, validation, and test sets. Validation data was used during training to select the best model, while the test set was kept separate for the final evaluation.

The best validation performance was reached around the second epoch. After that, validation loss started to increase while training loss continued to decrease, which indicated the beginning of overfitting.

Final test results:

- Accuracy: 91.5%
- Precision: 90.0%
- Recall: 92.8%
- F1-score: 91.4%

Compared with using BERT only as a feature extractor together with Logistic Regression, fine-tuning BERT directly for sentiment classification produced a clear improvement in performance.

# IMDB BERT Sentiment Analysis 1st version 

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
