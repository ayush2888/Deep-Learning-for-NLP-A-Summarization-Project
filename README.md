# 📝 Text Summarization using Pegasus

This project implements an **abstractive text summarization pipeline** using **Google’s Pegasus model** (via Hugging Face Transformers).  
It trains and evaluates the model on the **SAMSum dataset** for dialogue summarization.

---

## 🚀 Features
- Uses **Pegasus model** for abstractive summarization
- **Data ingestion & preprocessing** handled via configuration-driven pipeline
- **Trainer API (Hugging Face)** for training & evaluation
- Configurable through **YAML files**
- Saves **trained model** and **tokenizer** for reuse

---

## 📂 Project Structure
├── artifacts/ # Saved models, checkpoints, and logs
├── config/ # YAML configuration files
├── research/ # Jupyter/Colab notebooks for experimentation
├── src/ # Source code
│ ├── textSummarizer/
│ │ ├── components/ # Model trainer, data ingestion, data processing
│ │ ├── config/ # Configuration manager
│ │ ├── constants/ # Constants file
│ │ ├── entity/ # Entity classes for configs
│ │ ├── logging/ # Logging utility
│ │ ├── pipeline/ # Training and prediction pipelines
│ │ └── utils/ # Common utility functions
├── venv/ # Virtual environment
├── app.py # Entry point for running pipeline
├── requirements.txt # Dependencies
└── README.md # Project documentation

---

## ⚙️ Installation
```bash
# Clone the repository
git clone https://github.com/ayush2888/Deep-Learning-for-NLP-A-Summarization-Project.git
cd text-summarization-pegasus

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Linux/Mac
venv\Scripts\activate     # On Windows

# Install dependencies
pip install -r requirements.txt

## 📊 Dataset

We use the Samsum dataset (Dialogue Summarization):

Train: 14,732 samples
Validation: 818 samples
Test: 819 samples


