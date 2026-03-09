
## Email-Spam-Ham 

This project is a Machine Learning based email classification system that detects whether an email message is Spam or Ham. The model is trained on an email dataset using TF-IDF feature extraction and machine learning algorithms to analyze the text and make predictions. Includes an interactive web app built with Streamlit for real-time predictions.

---
## Project Overview

Spam emails are a common problem in email communication. They often contain advertisements, scams, or malicious content.

This project solves that problem by building a machine learning model that automatically detects spam emails.

The system works in three main stages:

* Data preprocessing – Clean and prepare the email text.
* Feature extraction – Convert text into numerical data using TF-IDF.
* Model prediction – Classify the message as Spam or Ham.

---
## 🧠 How the Model Works

## 1. Dataset

The model is trained on an email dataset containing two types of messages:

 * Spam → Unwanted emails  
 * Ham → Normal emails  

Dataset file used in the project is ('spam_ham_dataset.csv').Which is also given in github repository.

---
## 2. Data Cleaning

Before training the model, the text is cleaned using the following steps:

- Convert text to **lowercase**
- **Tokenization** (split sentence into words)
- Remove **stopwords** like *the, is, and*
- Remove **numbers and special characters**
- Apply **lemmatization** to convert words to their base form

Example:

```
Original Text:
"Congratulations! You have WON a free prize!!!"

Processed Text:
"congratulation win free prize"
```

---
## 3. Feature Extraction

The cleaned text is converted into numbers using:

**TF-IDF (Term Frequency – Inverse Document Frequency)**

This technique helps the model understand which words are more important in a message.

The project uses:

- **Max Features:** 3000  
- **N-grams:** Unigrams and Bigrams  

---

## 4. Model Training

Two machine learning models are trained and compared:

- Logistic Regression  
- Support Vector Machine (SVM)

Both models are trained and evaluated, and the **best performing model is automatically selected**.

## Screenshots

![App Screenshot](https://github.com/rohitvirdi5rv-crypto/Email-Spam-Ham/blob/00343762ac85b4fec3ea9f93c6ca1325b32468dc/best%20model.png)

---
## 5. Model Saving

The trained model and vectorizer are saved using **Pickle**:

```
best_model.pkl
vectorizer.pkl
```

These files are later used by the web application to make predictions.

---
## 🌐 Web Application


The project includes a **user-friendly web interface built with Streamlit**.

### Features of the App

- Enter any email message

![App Screenshot](https://github.com/rohitvirdi5rv-crypto/Email-Spam-Ham/blob/00343762ac85b4fec3ea9f93c6ca1325b32468dc/Front1.png)

- Click **Predict**
![App Screenshot](https://github.com/rohitvirdi5rv-crypto/Email-Spam-Ham/blob/00343762ac85b4fec3ea9f93c6ca1325b32468dc/Front2.png)
- Instantly see the result:

✅ **HAM** – Safe email
![App Screenshot](https://github.com/rohitvirdi5rv-crypto/Email-Spam-Ham/blob/00343762ac85b4fec3ea9f93c6ca1325b32468dc/Front4.png)
🚫 **SPAM** – Suspicious email
![App Screenshot](https://github.com/rohitvirdi5rv-crypto/Email-Spam-Ham/blob/00343762ac85b4fec3ea9f93c6ca1325b32468dc/Front3.png)

---