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

```
.
├── artifacts/                 # Saved models, checkpoints, and logs
│   ├── data_ingestion/        # Downloaded raw dataset
│   ├── data_transformation/   # Processed/tokenized dataset
│   ├── model_trainer/         # Trained models and metrics
│   └── model_evaluation/      # Evaluation results (ROUGE scores, etc.)
│
├── config/                    # Configuration files (YAML)
│   └── config.yaml
│
├── research/                  # Jupyter notebooks for experiments
│   └── experiment.ipynb
│
├── src/
│   └── textSummarizer/
│       ├── components/        # Core modules
│       │   ├── data_ingestion.py
│       │   ├── data_transformation.py
│       │   ├── model_trainer.py
│       │   └── model_evaluation.py
│       │
│       ├── config/            # Configuration manager
│       │   └── configuration.py
│       │
│       ├── constants/         # Constants used in the project
│       │   └── __init__.py
│       │
│       ├── entity/            # Entity classes for configs
│       │   └── config_entity.py
│       │
│       ├── logging/           # Logging setup
│       │   └── logger.py
│       │
│       ├── pipeline/          # Pipelines for training, evaluation, prediction
│       │   ├── training_pipeline.py
│       │   ├── evaluation_pipeline.py
│       │   └── prediction_pipeline.py
│       │
│       └── utils/             # Utility functions
│           └── common.py
│
├── app.py                     # Entry point to run pipelines
├── requirements.txt           # Dependencies
├── README.md                  # Project documentation
└── venv/                      # Virtual environment
```


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


🛠️ Training the Model

To start training, run:
python app.py
