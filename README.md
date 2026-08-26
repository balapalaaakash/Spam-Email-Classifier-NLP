# 📧 Spam Email Classifier using NLP

## 📌 Project Overview

This project is a Machine Learning and Natural Language Processing (NLP) based Spam Email/SMS Classifier.

The system analyzes the text of a message and classifies it into one of two categories:

* **SPAM** – unwanted or suspicious messages
* **HAM** – normal/legitimate messages

The project uses **TF-IDF Vectorization** to convert text into numerical features and a **Multinomial Naive Bayes** algorithm for classification.

---

## 🎯 Objective

The main objective of this project is to automatically identify spam messages using Natural Language Processing and Machine Learning techniques.

The classifier helps distinguish unwanted messages from legitimate messages based on the words and patterns present in the message.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Joblib**
* **Google Colab**
* **Natural Language Processing (NLP)**
* **TF-IDF**
* **Multinomial Naive Bayes**

---

## 📊 Dataset

The project uses the **SMS Spam Collection dataset**.

The dataset contains SMS messages labeled as either:

* `ham` – legitimate message
* `spam` – spam message

### Dataset Features

| Feature | Description             |
| ------- | ----------------------- |
| Label   | Spam or Ham             |
| Message | Text content of the SMS |

The dataset is divided into training and testing data.

* **80%** → Training
* **20%** → Testing

---

## 🧠 Machine Learning Algorithm

### Multinomial Naive Bayes

Multinomial Naive Bayes is a classification algorithm commonly used for text classification problems.

It calculates the probability of a message belonging to different classes based on the words/features present in the message.

In this project:

```text
Message
   ↓
TF-IDF
   ↓
Numerical Features
   ↓
Multinomial Naive Bayes
   ↓
SPAM / HAM
```

---

## 🔤 NLP Technique — TF-IDF

TF-IDF stands for:

**Term Frequency – Inverse Document Frequency**

It converts text into numerical values that can be processed by a machine learning model.

TF-IDF gives higher importance to words that are useful for distinguishing between messages.

Example:

```text
"Congratulations! You won a free prize!"
```

The text is converted into numerical features using TF-IDF before being given to the classifier.

---

## ⚙️ Project Workflow

```text
SMS Dataset
     ↓
Data Loading
     ↓
Data Cleaning & Preparation
     ↓
Label Encoding
     ↓
Train-Test Split
     ↓
TF-IDF Vectorization
     ↓
Naive Bayes Training
     ↓
Model Prediction
     ↓
Model Evaluation
     ↓
SPAM / HAM Classification
```

---

## 🔄 Implementation Steps

### 1. Load Dataset

The SMS Spam Collection dataset is loaded using Pandas.

### 2. Label Encoding

The labels are converted into numerical values:

```text
HAM  → 0
SPAM → 1
```

### 3. Train-Test Split

The dataset is divided into:

```text
80% Training Data
20% Testing Data
```

### 4. TF-IDF Vectorization

The message text is converted into numerical feature vectors.

### 5. Model Training

A Multinomial Naive Bayes classifier is trained using the TF-IDF features.

### 6. Prediction

The trained model predicts whether an unseen message is spam or legitimate.

### 7. Evaluation

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## 📈 Model Performance

The model achieved approximately **96–98% accuracy** on the test dataset.

> **Note:** The exact accuracy may vary depending on the dataset version and training configuration.

### Evaluation Metrics

The following metrics are used:

* **Accuracy** – Overall percentage of correct predictions.
* **Precision** – How many predicted spam messages were actually spam.
* **Recall** – How many actual spam messages were correctly identified.
* **F1-score** – Combination of precision and recall.

---

## 🔲 Confusion Matrix

The confusion matrix shows the number of correctly and incorrectly classified messages.

The matrix contains:

```text
                Predicted
              Ham     Spam

Actual Ham     TN      FP

Actual Spam    FN      TP
```

Where:

* **TN** = Correctly identified Ham
* **TP** = Correctly identified Spam
* **FP** = Ham incorrectly classified as Spam
* **FN** = Spam incorrectly classified as Ham

---

## 🧪 Example Predictions

### Example 1

**Input:**

```text
Congratulations! You won a free lottery prize. Click now!
```

**Prediction:**

```text
SPAM
```

### Example 2

**Input:**

```text
Hey, are you coming to college tomorrow?
```

**Prediction:**

```text
NOT SPAM
```

---

## 💻 Custom Message Prediction

The project also allows users to enter their own message and obtain a prediction.

Example:

```python
message = "Congratulations! You won a free lottery prize."

result = predict_spam(message)

print("Prediction:", result)
```

Output:

```text
Prediction: SPAM
```

---

## 📂 Project Structure

```text
Spam-Email-Classifier-NLP/
│
├── Spam_Email_Classifier_NLP.ipynb
│
├── spam_classifier.pkl
│
├── tfidf_vectorizer.pkl
│
├── requirements.txt
│
└── README.md
```

### File Description

| File                              | Description                            |
| --------------------------------- | -------------------------------------- |
| `Spam_Email_Classifier_NLP.ipynb` | Complete Google Colab/Jupyter Notebook |
| `spam_classifier.pkl`             | Trained Naive Bayes model              |
| `tfidf_vectorizer.pkl`            | Saved TF-IDF vectorizer                |
| `requirements.txt`                | Required Python libraries              |
| `README.md`                       | Project documentation                  |

---

## ▶️ How to Run the Project

### Option 1 — Google Colab

1. Open the `.ipynb` file.
2. Open it using Google Colab.
3. Run the cells from top to bottom.
4. Load the dataset.
5. Train the model.
6. Evaluate the model.
7. Enter custom messages for prediction.

### Option 2 — Local Computer

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/Spam-Email-Classifier-NLP.git
```

Go into the project directory:

```bash
cd Spam-Email-Classifier-NLP
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook
```

Run the notebook cells sequentially.

---

## 🚀 Future Improvements

The project can be improved by:

* Creating a web interface for users.
* Adding real-time spam detection.
* Using advanced NLP models such as LSTM or BERT.
* Adding email integration.
* Deploying the classifier as a web application.
* Supporting multiple languages.
* Improving detection of phishing and fraudulent messages.

---

## 🌟 Applications

This type of system can be used for:

* Email spam filtering
* SMS spam detection
* Phishing message detection
* Fraudulent message identification
* Automated message filtering
* Communication security systems

---

## 📚 Learning Outcomes

Through this project, I learned:

* Natural Language Processing fundamentals
* Text classification
* TF-IDF feature extraction
* Naive Bayes classification
* Dataset preprocessing
* Model training and testing
* Accuracy evaluation
* Confusion matrix analysis
* Saving and loading machine learning models
* Using GitHub for project documentation

---

## 👨‍💻 Author

**B.Aakash**

Artificial Intelligence & Data Science

---

## 📜 License

This project is created for educational and internship purposes.
