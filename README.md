# Spam Detection Project

This project focuses on building a spam detection model using machine learning techniques. The goal is to accurately classify text messages as either "spam" or "ham" (non-spam).

## Dataset

The dataset used for this project is stored in a CSV file called `spam.csv`. It contains 5572 text messages labeled as either "ham" or "spam". The dataset has five columns: `label`, `sms`, `num_characters`, `num_words`, and `num_sentence`.

Here is a preview of the dataset after preprocessing:

| label | sms                                               | num_characters | num_words | num_sentence |
|-------|---------------------------------------------------|----------------|-----------|--------------|
| 0     | Go until jurong point, crazy.. Available only ... | 111            | 24        | 2            |
| 0     | Ok lar... Joking wif u oni...                     | 29             | 8         | 2            |
| 1     | Free entry in 2 a wkly comp to win FA Cup fina... | 155            | 37        | 2            |
| ...   | ...                                               | ...            | ...       | ...          |

## Data Exploration

To gain insights into the dataset, various visualizations were performed:

- A pie chart was created to show the distribution of "ham" and "spam" messages. The dataset was found to be imbalanced, with a higher proportion of "ham" messages.

!![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/117982d8-8e9c-4bec-bb27-4011ac485439)

- The number of characters, words, and sentences in each message was analyzed. Descriptive statistics were calculated for these features. It was observed that spam messages tend to have more characters and words but fewer sentences compared to ham messages.

!![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/1cb68fae-fa22-4481-84f2-030bc74290ae)
![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/1be8f68b-1a3b-4a7c-8ea7-c4dbbf18e5ed)
![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/4d5feba3-4df5-45d3-af59-91bb85ea8c5c)


- Pair plots and a correlation heatmap were used to visualize the relationships between the different features. It was found that there is high correlation between every column, indicating multicollinearity.

!![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/efed5a62-a877-4196-863e-6740bec952cf)

!![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/6c410f86-2aad-447f-9282-d70036954a2e)


- Word clouds were generated to display the most common words in spam and ham messages.

!![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/834b9c4c-1693-45b4-8ff7-d4cddf54d951)



## Data Preprocessing

Before building the machine learning model, the text messages underwent several preprocessing steps:

1. Lowercasing: All text was converted to lowercase to ensure consistency.
2. Tokenization: Each text message was split into individual tokens.
3. Special characters removal: Special characters and symbols were removed from the text.
4. Stop words and punctuation removal: Stop words (commonly occurring words with little semantic meaning) and punctuation marks were eliminated.
5. Stemming: Words were stemmed using Porter stemming to merge different variations of the same word.

## Feature Extraction

Two feature extraction techniques were employed:

1. Count Vectorizer: It converts a collection of text documents into a matrix of token counts, representing the frequency of each word in the text.
2. TF-IDF Vectorizer: It calculates the Term Frequency-Inverse Document Frequency (TF-IDF) value for each word, which represents its importance in the text corpus.

## Model Training and Evaluation

Two classification algorithms were applied to the preprocessed dataset:

1. Gaussian Naive Bayes
2. Multinomial Naive Bayes

The models were trained using the transformed features and labels. The accuracy and precision scores were computed to evaluate their performance.

- Gaussian Naive Bayes Accuracy: 85.5%
- Gaussian Naive Bayes Precision: 48.0%

#### Confusion Matrix - Gaussian Naive Bayes
![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/51c2fba6-7788-47e0-8b40-4104438d441c)

- Multinomial Naive Bayes Accuracy: 96.99%
- Multinomial Naive Bayes Precision: 1.00
#### Confusion Matrix - Gaussian Naive Bayes
![image](https://github.com/TejaswiniNikumbh/Ham-or-Spam/assets/92621668/9eb64dea-64d1-4f15-afba-9ac28a5f8937)


