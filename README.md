# Twitter Sentiment Analysis using Support Vector Machines (SVM)

A Natural Language Processing (NLP) and machine learning project focused on classifying tweets into positive and negative sentiment categories using Support Vector Machines.

## Academic Achievement

**Grade: Distinction**

Awarded a **Distinction for this individual NLP project** as part of my MSc Data Science programme at Queen Mary University of London.

The project involved developing a sentiment classification pipeline, implementing text preprocessing and feature extraction techniques, training an SVM classifier, conducting cross-validation and analysing model errors.

## Project Overview

The objective of this project was to build a machine learning model capable of identifying sentiment expressed in tweets and classifying each tweet as either positive or negative.

The project explored how text preprocessing, feature engineering, binary word representations and model optimisation can improve sentiment classification performance.

The work was organised into two stages:

1. **Baseline development and evaluation:** Implementing text preprocessing, binary feature extraction, Linear SVM classification, cross-validation and error analysis.
2. **Model optimisation:** Improving text preprocessing and feature extraction, experimenting with n-grams, sentiment lexicon features and SVM parameter tuning.

## Dataset

The project used a labelled Twitter sentiment dataset containing positive and negative tweets.

Dataset details from the executed baseline notebook:

- Total records: 33,540
- Training samples: 26,832
- Test samples: 6,708
- Training/test split: 80:20
- Classification categories: Positive and Negative

The dataset was loaded from a local TSV/CSV file. The original dataset is not included in this repository.

## Methodology

### 1. Text Preprocessing

The initial preprocessing pipeline included:

- Tokenisation
- Lowercasing
- Removal of special characters and non-alphabetic symbols

The optimisation stage further explored:

- Stopword removal
- Lemmatization
- Improved text normalisation

### 2. Feature Extraction

The baseline model used binary word-presence feature vectors.

Each word was represented as a binary feature:

- 1: Word appears in the tweet.
- 0: Word does not appear in the tweet.

The baseline feature space contained 104,038 features.

The optimisation stage explored richer representations, including:

- Word n-grams (bigrams and trigrams)
- Sentiment lexicon features
- Improved linguistic preprocessing

### 3. Model Development

A Linear Support Vector Machine (Linear SVM) classifier was implemented using Scikit-learn.

The classifier was trained to distinguish positive and negative sentiment based on the extracted text features.

### 4. Cross-Validation

10-fold cross-validation was implemented to evaluate baseline model performance.

The dataset was divided into ten folds. In each iteration, nine folds were used for training and one fold for validation.

The evaluation metrics included:

- Precision
- Recall
- F1-score

### 5. Error Analysis

A separate error analysis was conducted to examine false positives and false negatives.

The baseline test evaluation identified:

- Total test samples: 5,367
- Incorrect predictions: 875
- Accuracy: 83.7%
- False positives: 515
- False negatives: 360

The analysis highlighted challenges involving sarcasm, mixed sentiment and ambiguous expressions.

### 6. Model Optimisation

Several improvements were explored to enhance the classifier:

- Stopword removal and lemmatisation
- Bigram and trigram feature extraction
- Sentiment lexicon-based features
- SVM regularisation parameter tuning
- Class-weight adjustments

These improvements aimed to make the feature representation more informative and improve the model's ability to classify ambiguous and mixed-sentiment tweets.

## Model Evaluation

### Baseline Performance

The baseline model was evaluated using 10-fold cross-validation.

| Metric | Score |
|---|---:|
| Precision | 0.8287 |
| Recall | 0.8305 |
| F1-score | 0.8289 |

The separate baseline error analysis reported an accuracy of 83.7% on 5,367 test samples.

### Improved Model Performance

The project report documented the following results after model improvements:

| Metric | Score |
|---|---:|
| Precision | 0.863 |
| Recall | 0.864 |
| F1-score | 0.863 |

The report describes improvements in classification performance following preprocessing, feature engineering and SVM optimisation.

## Key Findings

- Binary word-presence features provided a useful baseline for sentiment classification.
- Text preprocessing helped improve the quality of extracted features.
- N-grams offered a way to capture additional contextual information from tweet expressions.
- Sentiment lexicon features provided additional sentiment-related signals.
- SVM parameter tuning and class-weight adjustments were explored to improve classification.
- Error analysis highlighted the difficulty of interpreting sarcasm, ambiguous expressions and tweets containing mixed emotions.

## Limitations and Future Improvements

Although the project demonstrated improvements through feature engineering and model optimisation, traditional statistical NLP techniques have limitations.

Potential future improvements include:

- Exploring TF-IDF-based feature representations.
- Experimenting with more advanced word embeddings.
- Evaluating transformer-based models such as BERT.
- Improving sarcasm and context detection.
- Exploring more robust approaches to mixed-sentiment classification.
- Conducting further hyperparameter optimisation.

## Technologies and Tools

- Python
- Jupyter Notebook
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Linear Support Vector Machines (SVM)
- Natural Language Processing (NLP)
- Text Preprocessing
- Feature Engineering
- Cross-Validation
- Model Evaluation

## Repository Structure

```text
social-media-sentiment-classification/
│
├── twitter_sentiment_analysis_baseline.ipynb
├── twitter_sentiment_analysis_optimisation.ipynb
└── README.md
```

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/anvithasubramani/social-media-sentiment-classification.git
   ```

2. Navigate to the project directory:

   ```bash
   cd social-media-sentiment-classification
   ```

3. Install the required libraries:

   ```bash
   pip install pandas numpy scikit-learn nltk matplotlib scipy
   ```

4. Download and place the original labelled Twitter dataset in the appropriate location.

5. Update the dataset file paths in the notebooks to match your local directory.

6. Open the notebooks using Jupyter:

   ```bash
   jupyter notebook
   ```

7. Run the baseline notebook followed by the optimisation notebook.

## Author

**Anvitha Priyaa Vellal Subramani**

MSc Data Science | Queen Mary University of London
