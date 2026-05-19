# FUTURE_ML_02
# NLP model for support ticket classification and priority prediction


## 🚀 Project Overview
This project builds a Machine Learning model to automatically classify customer support tickets and predict their priority.

The goal is to help support teams:

Respond faster to urgent issues
Automatically route tickets
Improve customer satisfaction

---

## 💼 Business Problem
Support teams often face:
- High volumes of incoming tickets
- Delays in identifying urgent issues
- Inconsistent categorization by agents

This system uses Machine Learning and NLP to assist in:
✔ Faster ticket routing  
✔ Consistent classification  
✔ Early identification of critical issues  

---


## ⚙️ How the System Works

### 1️⃣ Ticket Categorization (Classification Model)

The model analyzes ticket text (subject + description) and assigns it to a category such as:
- Billing Issues
- Technical Support
- Account Access
- Refund Requests

####  How it decides:
- Uses **TF-IDF vectorization** to convert text into numerical features
- Captures important keywords and phrases (e.g., "payment failed", "login error")
- Applies a **Linear Support Vector Machine (LinearSVC)** to classify tickets

👉 In simple terms:
> The model learns patterns in how customers describe different problems.

---

### 2️⃣ Priority Prediction (Urgency Model)

The system predicts how urgent a ticket is:
- Critical
- High
- Medium
- Low

####  How priority is decided:
The model uses a combination of:

**Text signals**
- Urgency keywords (e.g., "urgent", "ASAP", "not working")
- Message length (detailed complaints often indicate seriousness)

**Metadata features**
- Ticket channel (email, chat, etc.)
- Customer-related attributes (if available)

👉 In simple terms:
> The model estimates urgency based on how the issue is described and contextual signals.

## Ticket Category Classification

Predicts:

Billing inquiry
Cancellation request
Product inquiry
Refund request
Technical issue

---

##  Technical Implementation

- Python
- Pandas
- Scikit-learn
- TF-IDF Vectorizer (with n-grams)
- LinearSVC (Support Vector Machine)
- ColumnTransformer (for combining text + structured features)

---

##  Data Preprocessing

The text data was cleaned using:

Lowercasing
Removal of punctuation
Stopword removal

A new feature full_text was created by combining:

Ticket Description
Cleaned text

## Feature Engineering

Text was converted into numerical format using:

TF-IDF Vectorization

This helps the model understand the importance of words in each ticket.

---

## 📊 Model Evaluation

### Ticket Classification
- Accuracy: ~20%

### Priority Prediction
- Accuracy: ~26%

### Metrics Used:
- Precision
- Recall
- F1-score
- Confusion Matrix

---

##  Key Insights (Very Important)

### 1️⃣ Text alone is not enough
Many tickets use similar language across different categories, making classification difficult.

### 2️⃣ Priority is not purely text-driven
Urgency often depends on:
- Customer value
- SLAs
- Business impact

These were not fully captured in the dataset.

### 3️⃣ Model confusion is realistic
The confusion matrix shows overlap between:
- High vs Medium
- Critical vs High

👉 This reflects real-world ambiguity in support environments.

---

##  Business Interpretation

If deployed in a real company, this system would:

✔ Assist agents (not replace them)  
✔ Speed up initial ticket sorting  
✔ Flag potentially urgent issues early  
✔ Improve consistency in categorization  

---

##  Future Improvements

To make this production-ready:

- Use advanced NLP models (e.g., BERT)
- Include SLA and customer tier data
- Add rule-based overrides for critical cases
- Train on larger, more structured datasets
- Implement human-in-the-loop validation

---

## 📂 Project Structure
├── data/
├── notebooks/
├── models/
├── README.md

<img width="980" height="616" alt="Confusion matrix" src="https://github.com/user-attachments/assets/2e93b2d5-9c55-4376-958d-8ca718497bd7" />


---

## 👨‍💻 Author
Thando Manitswana

---

##  Final Note
This project demonstrates an end-to-end Machine Learning pipeline and highlights a key real-world lesson:

> The biggest limitation in ML systems is often the data — not the model.


