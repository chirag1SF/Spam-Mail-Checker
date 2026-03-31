# Spam Mail Checker

An end-to-end **NLP application** that classifies emails as **Spam** or **Ham** (Legitimate). This tool processes manual text input **and** logs into your Gmail via IMAP to analyze your **latest incoming messages in real-time**.

## Key Features

- **Natural Language Processing**: spaCy-powered lemmatization, text normalization, and preprocessing
- **Vectorization**: TF-IDF for spam keyword detection
- **Live Gmail Sync**: Real-time IMAP connection to `imap.gmail.com`
- **Web Dashboard**: Flask-powered UI for manual checks and live scanning
- **Production Ready**: Pickle-serialized model + vectorizer for instant deployment

## Tech Stack

| Category | Technologies |
|----------|--------------|
| **Language** | Python 3.x |
| **ML** | Scikit-learn, Pandas |
| **NLP** | spaCy (`en_core_web_lg`) |
| **Backend** | Flask |
| **Email** | IMAPClient, Pyzmail |
| **Config** | python-dotenv |

## Quick Start

### 1. Clone & Setup
```bash
git clone https://github.com/chirag1SF/Spam-Mail-Checker.git
cd Spam-Mail-Checker
pip install -r requirements.txt
python -m spacy download en_core_web_lg
```

### 2. Gmail App Password
1. [Google Account](https://myaccount.google.com/) → **Security** → **2-Step Verification** → **App passwords**
2. Generate password for **"Mail"**
3. Create `.env` file:
```env
USERNAME=your_email@gmail.com
PASSWORD=your_16_char_app_password
```

### 3. Launch Dashboard
```bash
flask run
```
**Open**: [http://127.0.0.1:5000](http://127.0.0.1:5000)
