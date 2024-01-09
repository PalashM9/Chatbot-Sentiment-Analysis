# Chatbot-Sentiment-Analysis

## Overview
This Jupyter notebook focuses on the development of a chatbot with emotion analysis capabilities. Utilizing advanced NLP techniques and models, this project aims to create a chatbot that not only interacts naturally with users but also understands and responds to their emotional context.

The project utilizes a dataset named `converse.csv` which consists of conversational excerpts annotated with sentiments. This dataset plays a crucial role in training and evaluating the chatbot's ability to understand and respond to various emotional contexts in human conversations.

## Structure
The dataset contains the following columns:
- `message`: Text of the conversation.
- `sentiment`: The sentiment associated with each message.

After initial processing, the `conversation_id` column was dropped, focusing on the `message` and `sentiment` columns.

## Sample Data
Here are a few examples from the dataset:

| message                                       | sentiment            |
| --------------------------------------------- | -------------------- |
| Are you a fan of Google or Microsoft?         | Curious to dive deeper|
| Both are excellent technology they are helpfu | Curious to dive deeper|
| I'm not a huge fan of Google, but I use it a  | Curious to dive deeper|
| ...                                           | ...                  |

## Sentiment Distribution
The sentiments in the dataset are diverse, ranging from curiosity and neutrality to various emotions like joy, anger, and fear. The distribution of these sentiments is as follows:

- Curious to dive deeper: 80888
- Neutral: 41367
- Surprised: 30638
- Happy: 29617
- Sad: 2533
- Anger: 2000
- Joy: 2000
- Fear: 1937
- Disgusted: 1433
- Fearful: 1026
- Angry: 876

## Preprocessing Steps
Several preprocessing steps were undertaken to refine the dataset:

1. Removal of the `conversation_id` column.
2. Stripping whitespace from the `sentiment` column.
3. Grouping similar sentiments together for a more generalized sentiment analysis.

## Sentiment Grouping
The sentiments were grouped into broader categories for simplicity and effectiveness in analysis. For instance, 'Curious to dive deeper', 'joy', and 'Happy' were all grouped under 'Interested' or 'Happy' categories.

## Final Dataset
After preprocessing and sentiment grouping, the dataset was structured as follows:

| message                                       | sentiment            | sentiment_grouped |
| --------------------------------------------- | -------------------- | ----------------- |
| I feel like that's what a vicious circle is   | anger                | Angry             |
| I travel I feel like men expect me to be neuro| fear                 | Fear              |
| ...                                           | ...                  | ...               |

## Visualization
A count plot was generated to visualize the distribution of grouped sentiments, providing a clear overview of the emotional landscape of the conversations in the dataset.

## Data Integrity
The dataset was checked for null values, ensuring its integrity for use in training and evaluation.

This dataset forms the backbone of our Chatbot Emotion Analysis project, enabling the development of a sophisticated AI that can understand and interact based on the emotional context of conversations.

## Features
- Sentiment analysis using pre-trained models.
- Conversational AI for interactive chat sessions.
- Integration of sentiment understanding in chatbot responses.
- Use of Hugging Face's Transformers library.

