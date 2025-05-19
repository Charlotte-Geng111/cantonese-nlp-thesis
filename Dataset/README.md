# README: Dataset Preprocessing for Cantonese Sentiment Analysis

## Project Overview

This project focuses on sentiment analysis of Cantonese restaurant reviews collected from the OpenRice platform. The primary objective is to preprocess the dataset to ensure its quality and consistency, providing a robust foundation for fine-tuning large language models (LLMs) for sentiment classification tasks.

### Dataset

The full Cantonese restaurant review dataset can be downloaded from:
[Google Drive Dataset Download](https://drive.google.com/drive/folders/1lk4qpUOqODdYLrO3QuU-sgPCi0ersBSl?usp=sharing)

---

## Data Preprocessing

### Objectives
- **Clean the raw dataset**: Remove unnecessary characters, special placeholders, and invalid data.
- **Handle emojis**: Process emojis based on different strategies for analysis.
- **Filter non-Cantonese text**: Ensure the dataset is exclusively Cantonese for consistent training.
- **Split the dataset**: Divide the data into training and testing subsets.
- **Convert to Alpaca format**: Prepare the dataset for fine-tuning in a structured format.

### Steps Completed

#### 1. Convert .txt File to .json Format

Transform the raw .txt data into structured .json format to facilitate model training.

#### 2. Dataset Splitting

After shuffling the data randomly, the dataset is divided into 90% training and 10% testing subsets to ensure a fair evaluation of model performance.

#### 3. Label Adjustment (Sentiment Simplification)

Convert the original multi-level sentiment labels into binary sentiment classes:

Negative Sentiment (Labels 1, 2)

Positive Sentiment (Labels 3, 4, 5)

#### 4. Sample Balancing (Training Set Only)

Balance the training set to ensure equal representation of positive and negative samples:

Calculate the number of positive and negative samples.

Randomly remove excess positive samples to match the count of negative samples.

Maintain the overall sample count and ensure balanced distribution.

#### 5. Data Cleaning and Filtering

Remove special characters and excessive whitespace to improve text quality.

Filter out non-Cantonese reviews to maintain language consistency, as non-Cantonese content can introduce noise during training.

Limit the length of each review to a maximum of 250 characters to reduce processing overhead.

#### 6. Emoji Handling

Implement three different strategies for processing emojis in the dataset:

No Emojis: Remove all emojis from the text.

With Emojis: Retain emojis in their original form.

Convert Emojis to Descriptions: Replace emojis with their corresponding Cantonese text descriptions (e.g., 😉 -> 眨眼咁笑, ❤️ -> 鍾意).

#### 7. Conversion to Alpaca Format

Structure the final processed data in the following JSON format:

{
    "instruction": "Classify the sentiment of this restaurant review.",
    "input": "<review_text>",
    "output": "<sentiment_label>"
}

This format is compatible with Alpaca models and supports efficient fine-tuning for Cantonese sentiment classification tasks.

