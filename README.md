BERT Sentiment Analysis

This repository contains a sentiment analysis project using BERT (Bidirectional Encoder Representations from Transformers). The model is trained on the carblacac/twitter-sentiment-analysis dataset to classify text as positive or negative.

Overview

This model processes text input and determines whether the statement expresses a positive or negative sentiment. It is trained using a dataset of labeled tweets and fine-tuned to accurately classify new text inputs. The model can be used to analyze customer feedback, social media posts, and other textual data to understand sentiment trends.

Installation

Before running the project, install the required dependencies:

pip install datasets torch transformers pandas numpy seaborn matplotlib

Dataset

The dataset is loaded from the Hugging Face datasets library:

The dataset is split into training, testing, and validation sets.

Data Preprocessing

Removal of URLs and mentions (@username).

Filtering out short texts (<4 characters).

Checking for missing or duplicate values.

Visualizing sentiment distribution.

Model Training

The model is fine-tuned using BertForSequenceClassification from transformers.

Optimization is performed using AdamW, and training is managed with a learning rate scheduler. Accuracy and loss are monitored throughout training.

Model Evaluation

A validation function is used to evaluate the model’s performance.

Saving and Loading the Model

After training, the model is saved for later use.

The model can be reloaded for inference.

Sentiment Prediction

This model can classify new text inputs as positive or negative.

Example Usage

The model analyzes text and provides sentiment classification:

"I am a winner" → Positive

"I hate you" → Negative
