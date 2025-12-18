# 🐦 Real-Time Twitter Sentiment Analysis

A Python-based tool that streams real-time tweets using the Twitter API v2, cleans the data, and performs sentiment analysis using natural language processing (NLP) models.

## 🚀 Features
* **Real-Time Data Fetching:** Uses `Tweepy` to stream live tweets based on hashtags (e.g., `#crypto`).
* **Text Preprocessing:** Automatically cleans tweets by removing handles, URLs, special characters, and "RT" tags.
* **Sentiment Analysis:** * Primary: Uses **Flair** (`en-sentiment` model) for fast and accurate polarity detection.
    * Alternative: Includes code for **RoBERTa** (`cardiffnlp/twitter-roberta-base-sentiment`) from Hugging Face for advanced sentiment scoring.
* **Rate Limit Handling:** Intelligent error handling that automatically sleeps and retries when Twitter API rate limits are hit.

## 🛠️ Tech Stack
* **Python 3.x**
* **Tweepy** (Twitter API Client)
* **Flair** (NLP Framework)
* **Transformers** (Hugging Face)
* **Regular Expressions (Re)**

## 📋 Prerequisites
1.  **Python 3.10+** installed.
2.  **Twitter Developer Account:** You need to apply for a Twitter Developer account to get your API keys.

## ⚙️ Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/realtime-twitter-sentiment.git](https://github.com/Dhruv2845/Realtime-Twitter-Sentiment-Analysis.git)
    cd realtime-twitter-sentiment
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## 🔑 Configuration
**Important:** Never share your API keys publicly.

1.  Open the script/notebook.
2.  Locate the authentication section:
    ```python
    bearer = "<<KEY>>"
    consumer_key = "<<KEY>>"
    consumer_secret = "<<KEY>>"
    access_token = "<<KEY>>"
    access_token_secret = "<<KEY>>"
    ```
3.  Replace the placeholders with your actual Twitter API credentials.

## 🏃‍♂️ Usage

1.  Run the Jupyter Notebook or Python script.
2.  The script will start fetching tweets containing the query `#crypto` (modifiable in the code).
3.  It will print the original tweet followed by its sentiment:
    ```text
    ------------------------Tweet-------------------------------
    Bitcoin is looking bullish today! 🚀 #crypto
    ------------------------------------------------------------
    Sentiment: POSITIVE
    ```

## ⚠️ API Limitations
This project uses the Twitter API Basic/Free tier.
* **Rate Limits:** You are limited to a certain number of requests per 15-minute window.
* **Handling:** The script is designed to print "Rate limit hit! Sleeping for 15 minutes..." and pause execution automatically to respect these limits.

## 🤝 Contributing
Feel free to fork this project and submit pull requests.
