# REALM

# Overview  
This project explores how modern open-source and free LLMs can be used to mine user reviews and analyse sentiments involving sarcasm and emotional contradiction. It forms part of a broader academic investigation into using LLMs for Requirements Engineering tasks.

#  Models Evaluated so far
- **Mistral (via Ollama)**  
- **LLaMA2 (via Ollama)**  
- **DistilBERT** (via HuggingFace Transformers)
Each model was tested on the same input reviews with carefully crafted prompts to assess their ability to detect sarcasm and classify sentiment meaningfully.


# Grounded Truth Sentiment Analysis 🧠✨

This Jupyter notebook (`grounded_truth.ipynb`) performs sarcasm-aware sentiment analysis using a **ground truth annotated dataset**. Unlike earlier experiments where we used free-form reviews with no labels, this notebook uses a **labeled dataset** containing known sentiment categories (Positive, Negative, Neutral).

---

## 🧪 What's Inside

- **Simple EDA (Exploratory Data Analysis):**  
  Quickly inspects the dataset to understand distributions and sentiment class balance.

- **Ground Truth Label Extraction:**  
  Extracts clean sentiment labels from the `Feature (Positive)`, `Feature (Negative)`, and `Feature (Neutral)` columns.

- **Sarcasm-Aware AI Predictions:**  
  Uses `Mistral` (via Ollama) to predict sentiment of each review with special handling for sarcasm, irony, and ambiguity.

- **Parallel Inference:**  
  Speeds up AI predictions using Python’s `ThreadPoolExecutor`.

- **Evaluation Metrics:**  
  Compares AI predictions to ground truth using:
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

- **Export:**  
  Saves the annotated output to Excel for easy viewing.

---

## 📁 Output

- Annotated file: `annotated_sentiment_output.xlsx`  
- Each row includes:
  - The original review
  - Ground truth sentiment
  - Mistral’s predicted sentiment

---

## ⚙️ Requirements

- Python 3.x  
- `pandas`, `tqdm`, `ollama`, `concurrent.futures`

---

## 📌 Notes
- Future improvements may include confidence scores, model comparison, and sarcasm flagging.
- All models were run locally using the **Ollama framework** or HuggingFace pipelines  
- Results saved in `.xlsx` format for easy inspection and sharing  
