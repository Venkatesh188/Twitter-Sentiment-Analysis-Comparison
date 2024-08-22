# Twitter Sentiment Analysis: XGBoost vs. LSTM

## Project Overview

This project focuses on comparing the performance and development effort of a traditional NLP model (XGBoost) with a deep learning model (AWD_LSTM) for sentiment analysis. The dataset used in this project was sourced from Kaggle and includes Twitter sentiment analysis data. The primary goal of this project is to evaluate which model is more suitable for productization, considering factors such as accuracy, complexity, and resource requirements.

## Data Selection and Business Applications

### Data Source
The dataset was selected from Kaggle due to its relevance and the broad applicability of sentiment analysis across various industries. Sentiment analysis is a valuable tool for businesses to understand customer opinions, feedback, and experiences.

### Business Problems Solved
1. **Customer Service Improvement**: Analyzing customer reviews to identify common issues and enhance products or services.
2. **Market Research**: Gauging public opinion on new products, marketing campaigns, or brand perception through analysis of social media posts and comments.
3. **Competitive Analysis**: Identifying competitors' strengths and weaknesses by examining sentiments around their products, allowing businesses to adjust strategies accordingly.

## Data Preparation

To prepare the dataset for modeling, several preprocessing steps were performed:
- **Data Cleaning**: Removal of special characters, web links, and extra spaces.
- **Handling Class Imbalance**: Techniques like oversampling minority classes and adjusting training processes to balance the data.
- **Text Preprocessing**: Tokenization, lowercasing, stopword removal, and text normalization.
- **Train-Test Split**: Splitting the dataset to prevent overfitting and ensure the model generalizes well.
- **Numerical Encoding**: Converting sentiment labels into numerical values for model input.
- **Sequence Length Adjustment**: Ensuring that text sequences are of appropriate length for the models used.
- **Batch Preparation**: Ensuring each training batch has a balanced mix of different sentiments.

## Model Comparison

### Accuracy Comparison
- **Traditional NLP Model (XGBoost)**
  - Overall Accuracy: 74%
  - Precision and recall across various sentiment classes, with generally better performance in classifying tweets compared to AWD_LSTM.

- **Deep Learning Model (AWD_LSTM)**
  - Overall Accuracy: 67%
  - Better at capturing nuanced language but with a trade-off in overall accuracy.

### Development Effort
- **XGBoost**
  - Simpler text processing and faster training times, suitable for those with limited computational resources.
  - Easier model tuning with straightforward parameter adjustments.
  - Suitable for quick deployment and easy maintenance in production environments.

- **AWD_LSTM**
  - More complex development process, requiring advanced tools like fastai and PyTorch.
  - Higher resource requirements, including GPUs for efficient training.
  - Greater flexibility in handling complex language patterns, making it ideal for more detailed language analysis tasks.

## Recommendation for Productization

For productization, the XGBoost model is recommended due to its simplicity, lower resource requirements, and ease of deployment and maintenance. It provides good performance and reliability, making it a practical choice for real-world applications where efficiency is critical.

## References

Twitter_Sentiment_Analysis_xgboost.ipynb

Twitter_Sentiment_Analysis_LSTM.ipynb
