# SafeMail-AI 🛡️📧  
**AI-powered shield against phishing email scams**

SafeMail-AI is a student-centric project built during **Winter of Code 5.0**.  
It helps users detect potentially **phishing/scam emails** using a Machine Learning classifier along with rule-based security checks (keywords + URL analysis).

---

## ✨ Features
- Detects phishing/scam emails using ML classification
- Displays risk level (**LOW / MEDIUM / HIGH**)
- Highlights scam keywords inside email text
- Checks URLs for suspicious domains/TLDs and shortened links
- Simple Flask-based web UI

---

## 🧠 Tech Stack
- **Python**
- **Flask**
- **scikit-learn**
- **Pandas**
- **Gunicorn**
- HTML + Jinja Templates

---

## 📦 Requirements
All dependencies are listed in `requirements.txt`:

- flask
- pandas
- scikit-learn
- gunicorn
- python-dotenv

---

## 📂 Project Structure
```bash
SafeMail-AI/
│── app.py                # Flask app
│── config.py             # Configuration classes
│── train_model.py        # Training script (generates model files)
│── phishing.csv          # Dataset
│── requirements.txt      # Dependencies
│── .env.sample           # Sample environment variables
│── DEPLOY.md             # Deployment guide
│── Procfile              # Deployment config
│── runtime.txt           # Runtime version
└── README.md             # Documentation

---

🚀 Getting Started

✅ Prerequisites
- Python **3.10+** recommended
- pip
- Git

---

## 🔧 Installation

### 1) Clone the repository
```bash
git clone https://github.com/syed1230/SafeMail-AI.git
cd SafeMail-AI

### 2) Create and activate virtual environment

#### Windows (PowerShell / CMD)
python -m venv venv
venv\Scripts\activate

#### If PowerShell blocks activation, run:
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

#### macOS / Linux
python3 -m venv venv
source venv/bin/activate

### 3) Install dependencies
pip install -r requirements.txt

### 4) Setup Environment Variables
copy .env.sample .env

#### macOS / Linux
python3 -m pip install -r requirements.txt
cp .env.sample .env

### 5) Train the ML Model

#### This project requires the following ML model files:
- `model/phishing_model.pkl`
- `model/vectorizer.pkl`

#### Generate them by running:
```bash
python train_model.py

#### If the model/ folder does not exist, create it first:
mkdir model

### 6) Run the Application
python app.py


Note: If the model/ folder already contains .pkl files, you can skip train_model.py.

Open in browser: `http://127.0.0.1:5000/`


---

## 🤝 Contributing

Contributions are welcome! 🎉  
If you'd like to improve this project, follow these steps:

1. Fork this repository

2. Clone your fork

```bash
git clone https://github.com/<your-username>/SafeMail-AI.git
cd SafeMail-AI

3. Create a new branch

```bash
git checkout -b feature/your-feature-name

4. Make changes and commit

```bash
git add .
git commit -m "Added: <short description>"

5. Push to GitHub

```bash
git push origin feature/your-feature-name

6. Open a Pull Request (PR) 🚀

---

## 👩‍💻 Maintainer
Maintained by:

Syed Shagufthaa
GitHub: https://github.com/syed1230

















