# FUTURE_ML_02
NLP model for support ticket classification and priority prediction
# 📩 Support Ticket Classification & Priority Prediction System

## 🚀 Project Overview
This project simulates a real-world support automation system that helps businesses automatically:

- Categorize incoming support tickets
- Assign priority levels (Critical, High, Medium, Low)

The goal is to improve response efficiency, reduce manual triage, and support faster decision-making in customer support operations.

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

#### 🔍 How it decides:
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

#### 🔍 How priority is decided:
The model uses a combination of:

**Text signals**
- Urgency keywords (e.g., "urgent", "ASAP", "not working")
- Message length (detailed complaints often indicate seriousness)

**Metadata features**
- Ticket channel (email, chat, etc.)
- Customer-related attributes (if available)

👉 In simple terms:
> The model estimates urgency based on how the issue is described and contextual signals.

---

## 🛠️ Technical Implementation

- Python
- Pandas
- Scikit-learn
- TF-IDF Vectorizer (with n-grams)
- LinearSVC (Support Vector Machine)
- ColumnTransformer (for combining text + structured features)

---

## 🧹 Data Preprocessing

- Lowercasing text
- Removing punctuation and noise
- Handling missing values
- Feature engineering:
  - Text length
  - Urgency keyword detection
- Encoding categorical variables

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

## 📉 Key Insights (Very Important)

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

## 🧠 Business Interpretation

If deployed in a real company, this system would:

✔ Assist agents (not replace them)  
✔ Speed up initial ticket sorting  
✔ Flag potentially urgent issues early  
✔ Improve consistency in categorization  

---

## 🚀 Future Improvements

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


---

## 👨‍💻 Author
Thando Manitswana

---

## 🎯 Final Note
This project demonstrates an end-to-end Machine Learning pipeline and highlights a key real-world lesson:

> The biggest limitation in ML systems is often the data — not the model.


