## Sentiment Analysis

Sentiment analysis, often referred to as opinion mining, is a powerful technique that leverages natural language processing and machine learning to extract and evaluate the sentiment or emotional tone expressed in written texts, such as reviews, comments, or social media posts. It plays a crucial role in understanding public opinion, customer feedback, and market trends.

### Positive Sentiment
Positive sentiment in reviews reflects a favorable or contented opinion about a product, service, or experience. When sentiment analysis identifies positive sentiments, it often implies that customers or users are satisfied and happy with their interactions. These reviews typically highlight the strengths and advantages of the subject matter.

**Positive sentiment examples:**

- "I absolutely love this product! It exceeded my expectations."
- "The service at this restaurant was outstanding, and the food was delicious."
- "The customer support team was incredibly helpful and responsive."

### Negative Sentiment
Negative sentiment, on the other hand, indicates dissatisfaction or disappointment with a particular aspect of the subject being reviewed. These reviews may express frustration, annoyance, or unhappiness and often pinpoint areas where improvement is needed.

**Negative sentiment examples:**

- "The quality of this item is terrible; it broke after just one use."
- "I had a terrible experience at this hotel; the staff was rude and unhelpful."
- "The software constantly crashes, making it impossible to work efficiently."

This sentiment analysis can be applied to the reviews in our project to categorize them into "happy" and "not happy" sentiments based on the content and tone of the text.


## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Data Loading and Text Cleaning](#data-loading-and-text-cleaning)
- [Data Visualization](#data-visualization)
- [Model Training and Building](#model-training-and-building)
- [5-Fold Cross-Validation](#5-fold-cross-validation)
- [Model Testing](#model-testing)
- [Conclusion](#Conclusion)


## Introduction

This project focuses on sentiment analysis, which involves the task of classifying text-based data into different sentiment categories, such as 'Not Happy' and 'Happy.' In this README, we'll walk you through the various stages of sentiment analysis, including data loading, text cleaning, data visualization, model training, cross-validation, and model testing.

## Prerequisites

Before running the code, make sure you have the following Python libraries installed:

- pandas
- numpy
- re
- string
- nltk
- nltk.sentiment.vader
- wordcloud
- matplotlib
- seaborn
- sklearn

You can install these libraries using pip command.



## Data Loading and Text Cleaning

We start by loading our dataset and performing text cleaning to prepare the data for analysis. The code in this section includes the following steps:

1. Loading the dataset from a CSV file.
2. Removing unnecessary columns ('User_ID', 'Browser_Used', 'Device_Used').
3. Applying text cleaning functions to preprocess the review descriptions.

For a detailed explanation of text cleaning functions and code, refer to the code provided in the Data Loading and Text Cleaning section.

## Data Visualization

Understanding the distribution of sentiment classes ('Not Happy' and 'Happy') is crucial. We employ data visualization techniques to visualize this distribution using a count plot. This helps us grasp the balance of positive and negative sentiments in the dataset.

We also visualize the sentiment score distribution using a histogram. Sentiment scores represent the overall sentiment polarity of each review.

For code and visualizations, refer to the Data Visualization section.

## Model Training and Building

In this section, we build a sentiment analysis model using machine learning techniques. The code includes the following steps:

1. Preparing the data for modeling.
2. Splitting the data into training and testing sets.
3. Creating a TF-IDF vectorizer and a logistic regression classifier.
4. Creating a pipeline for model training.
5. Fitting the model to the training data.
6. Making predictions and evaluating the model's performance.

For code and evaluation metrics, refer to the Model Training and Building section.

## 5-Fold Cross-Validation

To ensure the robustness of our sentiment analysis model, we perform 5-fold cross-validation. This technique helps us assess the model's performance across different subsets of the dataset.

For code and cross-validation results, refer to the 5-Fold Cross-Validation section.

# Model Testing

In the Model Testing phase, we evaluate the sentiment analysis model's performance using the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analyzer. VADER is a lexicon and rule-based sentiment analysis tool that assigns sentiment scores to text.

## VADER Sentiment Analysis

Incorporating the VADER sentiment analyzer:

1. We download the VADER lexicon, which is a prerequisite for using VADER.

2. Initialize the VADER sentiment analyzer.

3. Create a function to calculate the VADER sentiment score (compound score) for each review description.

4. Compute VADER sentiment scores for the cleaned review descriptions and store them in a new column.

## Visualizing VADER Sentiment Scores

We visualize the distribution of VADER sentiment scores using a histogram, providing insights into the sentiment polarity of the reviews. This visualization helps us understand the distribution of positive, negative, and neutral sentiments within the dataset.

## Conclusion

In this sentiment analysis project, we conducted a comprehensive analysis of customer reviews. We began by loading the dataset and performing text cleaning to prepare the data for analysis. The visualization of sentiment class distribution and sentiment score distribution provided valuable insights into the dataset.

Our machine learning model, built using TF-IDF vectorization and logistic regression, demonstrated strong performance in classifying reviews into sentiment categories. The 5-fold cross-validation results confirmed the model's reliability and consistency.

Additionally, we integrated the VADER sentiment analyzer for fine-grained sentiment analysis of individual reviews, which allowed us to categorize them as 'happy,' 'not happy,' or 'neutral.'

Overall, this project equips us with powerful tools for understanding sentiment within textual data, offering valuable insights into customer feedback and sentiment trends.
