
# Comparing Transformer Models for Token-Based Code Completion in Python

Token-based code completion plays a crucial role in enhancing developer productivity by predicting the next token in a code sequence. This project presents a comparative analysis of four Transformer-based models fine-tuned specifically for Python code completion tasks.

## 📌 Overview

This study evaluates and compares the performance of the following pre-trained Transformer models:

* **CodeGPT-Small-Py** (124M)
* **CodeGen-350M-Multi** (350M)
* **CodeT5-Base** (220M)
* **GPT-Neo 125M** (125M)

All models were fine-tuned using the **Python subset of the CodeSearchNet dataset** under identical training conditions.

## 🧠 Objective

To determine which Transformer architecture offers the best performance for token-based code completion and to understand the trade-offs between model size, overfitting, and generalization.

## 📊 Evaluation Metrics

Each model was evaluated using:

* **Token-level Accuracy**
* **Perplexity**

## 🏆 Key Findings

| Model Name         | Token Accuracy | Perplexity | Notes                                  |
| ------------------ | -------------- | ---------- | -------------------------------------- |
| CodeT5-Base        | **0.9949**     | High       | Highest accuracy, but overfit          |
| CodeGen-350M-Multi | 0.7628         | **1.4202** | Best generalization and overall winner |
| CodeGPT-Small-Py   | Moderate       | Moderate   | Code-specific, decent performance      |
| GPT-Neo 125M       | Lower          | Higher     | General-purpose, less suited for code  |

* **CodeT5-Base** achieved the highest accuracy but suffered from overfitting, reducing its practical reliability.
* **CodeGen-350M-Multi** demonstrated the best balance of accuracy and perplexity, making it the most reliable for real-world use cases.

## 🧪 Dataset

* **Source**: [CodeSearchNet (Python subset)](https://github.com/github/CodeSearchNet)
* **Preprocessing**: Tokenization using Hugging Face tokenizers, context window slicing, and sequence padding.

## 🖼️ Gradio Interface

An interactive **Gradio UI** was developed to:

* Visualize code token predictions
* Compare multiple models in real-time
* Support developer-friendly experimentation

## 🔮 Future Work

* Extend support for **multi-line code prediction**
* Evaluate models on **larger and more diverse code datasets**
* Conduct **user studies** for interactive usability feedback


