📧 Email Spam Classification Using Machine Learning

Project Overview:
This project builds a machine learning system to classify emails as either spam or ham (non-spam). It uses Natural Language Processing (NLP) techniques for text cleaning and feature extraction, and evaluates different ML models to find the best-performing classifier. A user can input a custom email and get real-time predictions.

Dataset:
- Source: SMS Spam Collection Dataset
- Features:
  - v1: Label (ham or spam)
  - v2: Email text
- Preprocessing:
  - Dropped unused columns (Unnamed: 2, 3, 4)
  - Renamed columns: v1 to result, v2 to emails

Data Preprocessing:
- Removed null and duplicate entries
- Created additional features:
  - Length: Character count
  - num_words: Number of words
  - num_sentence: Number of sentences
- Text cleaning:
  - Lowercasing
  - Tokenization
  - Special character removal
  - Stopword removal using NLTK
  - Stemming using PorterStemmer
- Added a new column: transform_text

Exploratory Data Analysis:
- Visualized class distribution using pie chart
- Compared average lengths:
  - Spam: around 138 characters
  - Ham: around 70 characters
- Average words and sentences:
  - Spam: 27 words, 2.9 sentences
  - Ham: 17 words, 1.8 sentences
- Correlation matrix and heatmap between features
- Violin plot showing email length vs spam classification

Word Frequency Analysis:
- Used Counter to find most common words
- Generated WordCloud and bar graphs
Top 10 Spam Words:
call, free, 2, txt, u, text, ur, mobil, stop, repli

Top 10 Ham Words:
u, go, nt, get, 2, gt, lt, come, ok, got

Model Building:
- Text vectorized using TfidfVectorizer (3000 features)
- Models used:
  - Support Vector Machine (SVC)
  - Naive Bayes
- Evaluation metrics:
  - SVM: Accuracy 99%, Precision 100%
  - Naive Bayes: Accuracy 98%, Precision 100%

Model Comparison:
- Bar charts comparing accuracy and precision
- SVM performed best overall

Live Prediction:
- Function: predict_email(email)
- Example Predictions:
  "Get a free iPhone now!" → Spam
  "Hey, how's it going?" → Ham

Technologies Used:
- Python
- Libraries: pandas, matplotlib, seaborn, nltk, wordcloud, sklearn

Conclusion:
A reliable spam classifier using NLP and machine learning. The SVM model achieved the best performance with 99% accuracy and 100% precision. It is suitable for real-time spam detection applications.
