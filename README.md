# Functional & Non-Functional Requirements Generation

Fine-tune T5 to automatically generate functional and non-functional software requirements from project scope descriptions using NLP and Transformers.

---

## 🚀 Project Overview

This project fine-tunes the `t5-base` model using the Hugging Face Transformers library to perform a text-to-text generation task: transforming scope descriptions into structured software requirements.

### ✨ Key Features

- Prepares a custom dataset of scope and requirement pairs
- Fine-tunes `t5-base` for structured generation
- Evaluates model using BLEU and ROUGE scores
- Produces both functional and non-functional requirements

---

## 📁 Dataset

The dataset is a JSON file with entries like:

```json
{
  "scope": "Build a library management system.",
  "functional_requirements": [
    "Allow users to borrow and return books",
    "Track overdue items"
  ],
  "non_functional_requirements": [
    "System should be responsive",
    "Ensure data is backed up daily"
  ]
}
````

## 🧠 Model

We use the T5 (Text-To-Text Transfer Transformer) model:

* Pretrained: `t5-base`
* Task format: `"Scope: <scope>" → "Functional Requirements:...\nNon-Functional Requirements:..."`

---

## 🛠️ Installation

```bash
pip install -U accelerate transformers datasets torch rouge_score
```

---

## 📊 Training & Evaluation

Training pipeline includes:

* Tokenization
* Dataset splitting: Train / Validation / Test
* Evaluation with BLEU and ROUGE
* Output analysis and visualization

Metrics like `ROUGE-L` and `sentence_bleu` are used to measure text generation quality.

---

## 📈 Sample Output

**Input:**

```
Scope: Develop an online food ordering platform.
```

**Output:**

```
Functional Requirements:
- Users can browse restaurants and menus.
- Place orders and make payments online.

Non-Functional Requirements:
- Platform should be mobile responsive.
- Ensure payment processing is secure.
```

---

## 🤖 Dependencies

* transformers
* datasets
* torch
* rouge\_score
* nltk
* matplotlib
* accelerate

---

## 📌 Usage

To run the notebook, simply open:

```bash
T5-base-functional-nonfunctional-requirements-generation.ipynb
```

Train your own model or fine-tune it on similar data.

---

## 📜 License

Feel Free to use the project.

---

## 👥 Contribution

* Contributions welcome via pull request!
