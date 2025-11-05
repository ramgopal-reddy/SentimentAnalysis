# Sentiment Analysis App

## Overview

The Sentiment Analysis App is a simple yet efficient tool for analyzing the sentiment of text-based input using machine learning. Whether it's a tweet, a review, or some other form of text, this application can determine whether the sentiment is positive or negative.

---

## Features

- **Text-based Sentiment Analysis**: Input text and receive an instant sentiment analysis—positive or negative.
- **Tweet Sentiment Analysis**: Fetch and analyze tweets for specified usernames.
- **Interactive Interface**: Powered by Streamlit for a user-friendly and responsive experience.
- **Machine Learning-based Approach**: Utilizes pre-trained models to ensure efficiency and reliability.

---

## How Sentiment Analysis Works

### 1. Text Preprocessing

All input text undergoes preprocessing to:

- Remove non-alphabetic characters.
- Convert to lowercase.
- Remove stop words (frequent, less informative words like "and", "the").
- Stem words to their basic form (e.g., "running" → "run").

### 2. Model and Vectorizer

- The pre-trained **Sentiment Analysis Model** (`modelSentiment.pkl`) is used to classify the sentiment.
- A **Vectorizer** (`vectorizer.pkl`) transforms text into a machine-readable format for the model.

### 3. Prediction

Each input text is processed and fed into the machine learning model. The output is either:

- **Positive**
- **Negative**

### Example Workflow:

- Input: "This is an amazing app!"
- Preprocessed: `['amazing', 'app']`
- Prediction: Positive Sentiment

---

## Technical Details

### Dependencies

- **Python Libraries**: `streamlit`, `nltk`, `numpy`, `pandas`, `pickle`.
- **Web Scraping Utility**: `ntscraper` for fetching tweets via the Nitter service.

### Core Functionalities

#### Text Classification

- Input texts are preprocessed using NLTK's stop words and Porter Stemmer.
- Preprocessed text is vectorized and passed into the pre-trained sentiment model.

#### Twitter Integration

- Fetch tweets using the Nitter API and analyze them for sentiment.

#### Results Display

- Sentiment results are elegantly displayed with clear visual indicators:
  - **Green for Positive**
  - **Red for Negative**

---

## How to Run the Application

1. Clone the repository:
   ```bash
   git clone https://github.com/ramgopal-reddy/SentimentAnalysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd SentimentAnalysis
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Ensure the following files are in the same directory:
   - `modelSentiment.pkl` (ML Model File)
   - `vectorizer.pkl` (Vectorizer for Text Input)
5. Run the application:
   ```bash
   streamlit run main.py
   ```
6. Open the app in your browser:
   - Default URL: `http://localhost:8501`

---

## Future Improvements

- Add more sentiments for multi-class analysis (e.g., neutral).
- Enhance the model to analyze large documents.
- Optimize web scraping for faster results.

---

## Credits

This application uses the [Nitter](https://nitter.net) API for secure and anonymous Twitter data scraping, making it reliable and API-keyless.

```bash
Stay Positive! 😁
```
