# 🛡️ SafeMail-AI

[![Python](https://img.shields.io/badge/Python-3.11.4-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Flask-Web%20App-green.svg)](https://flask.palletsprojects.com/)
[![Machine Learning](https://img.shields.io/badge/Scikit--Learn-Logistic%20Regression-orange.svg)](https://scikit-learn.org/)
[![Deployment](https://img.shields.io/badge/Deployment-Render%20%7C%20Railway-lightgrey.svg)]()

> **SafeMail-AI** is an intelligent web application designed to detect phishing and scam emails using Natural Language Processing (NLP) and Machine Learning. Created for Winter Code 5.0, this project bridges the gap between theoretical data science and practical, deployable software.

## ✨ Key Features

* **🧠 ML-Powered Classification:** Utilizes a Logistic Regression model paired with a TF-IDF vectorizer to accurately classify emails as safe or suspicious.
* **🔍 Heuristic URL Analysis:** Automatically extracts and evaluates embedded links to detect shortened domains (e.g., `bit.ly`) and highly suspicious Top-Level Domains (TLDs) (e.g., `.xyz`, `.tk`).
* **🚨 Threat Highlighting:** Parses email content to dynamically highlight known scam triggers and urgent keywords (e.g., "verify", "password", "bank") in the UI.
* **🚥 Dynamic Risk Scoring:** Adjusts the confidence level and risk assessment (Low, Medium, High) based on a combination of ML probabilities and deterministic URL analysis.
* **☁️ Production-Ready Backend:** Built with Flask and Gunicorn, featuring environment-based configurations (`development` vs. `production`) for seamless PaaS deployment.

## 🛠️ Tech Stack

* **Language:** Python 3.11.4
* **Backend:** Flask, Gunicorn
* **Machine Learning:** Scikit-Learn, Pandas, NumPy
* **Frontend:** HTML/CSS (Jinja2 Templates, MarkupSafe)
* **Deployment:** Ready for Render, Railway, or Heroku (includes `Procfile` and `runtime.txt`)

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.11+ installed. 

### Local Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/lipikaparida-web/SafeMail-AI.git](https://github.com/lipikaparida-web/SafeMail-AI.git)
   cd SafeMail-AI

2. **Set up a virtual environment:**
  python -m venv venv
  source venv/bin/activate  # On Windows use: venv\Scripts\activate

3. **Install dependencies:**
   pip install -r requirements.txt
   Set FLASK_DEBUG=1 in your .env for local development.

4. **Environment Variables:**
Copy the sample environment file and adjust if necessary:
   cp .env.sample .env

5. **Train the Model (Optional):**
   If you want to retrain the ML model with your own dataset, add your data to phishing.csv and run:
   python train_model.py
   This will generate the required phishing_model.pkl and vectorizer.pkl files in the model/ directory.
   
6. **Run the Application:**
   python app.py

## Access the app locally at http://127.0.0.1:5000

## ☁️ Deployment

SafeMail-AI is structured for immediate deployment on modern PaaS providers.

Push your code to GitHub.

Connect the repository to your preferred platform (Render, Railway, etc.).

The platform will automatically detect the Procfile (web: gunicorn app:app) and runtime.txt to provision the environment.

Ensure APP_ENV is set to production in your platform's environment variables.

## 🧠 Model Architecture details

The core detection engine is built on a Logistic Regression classifier.

Feature Extraction: TfidfVectorizer (capped at 3000 max features, English stop words removed).

Training Data: A curated CSV dataset of labeled phishing and safe emails.

Evaluation: Standard accuracy scoring using an 80/20 train-test split.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page. If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

## Author

**Lipika Parida** — [GitHub](https://github.com/lipikaparida-web) · [LinkedIn](https://www.linkedin.com/in/lipikaparida3/)
