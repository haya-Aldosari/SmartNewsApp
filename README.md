# News Recommendation System

This project is a content-based news recommender. The idea is simple: you type in a news title or short sentence, and the system finds the most relevant articles from a dataset using sentence similarity and keyword extraction.

## What it does

- Takes a short text input from the user (like a news headline)
- Extracts keywords using KeyBERT
- Computes semantic similarity using a Sentence Transformer model
- Recommends the most similar news articles
- Displays the results in a clean HTML interface

## Dataset

This project uses the MIND (Microsoft News Dataset) which contains thousands of news articles.

You can download the dataset from Kaggle:  
https://www.kaggle.com/datasets/arashnic/mind-news-dataset

> **Note:** The dataset is too large to upload directly to GitHub. Please download it manually from the link above and place it in the `data/` folder of the project.

## How it works

- The model used is `all-MiniLM-L6-v2` from Sentence Transformers
- Keywords are extracted from each article and the user input using KeyBERT
- Similarity is calculated using cosine similarity on sentence embeddings
- Flask is used to create a simple web interface
- ngrok is used to temporarily share the app online
