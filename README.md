# RAG Evaluator

## Overview

RAG Evaluator is a Python library for evaluating Retrieval-Augmented Generation (RAG) systems. It provides various metrics to evaluate the quality of generated text against reference text.

<img width="1919" height="871" alt="Screenshot 2025-07-19 185308" src="https://github.com/user-attachments/assets/57eb84f3-89c5-4311-85a9-f687bb87381f" />
<img width="1919" height="868" alt="Screenshot 2025-07-19 185324" src="https://github.com/user-attachments/assets/95602cb1-7bfb-448b-b4aa-88dc87738071" />

## Installation

You can install the library using pip:

```bash
pip install rag-evaluator
Usage
Here's how to use the RAG Evaluator library:
from rag_evaluator import RAGEvaluator

# Initialize the evaluator
evaluator = RAGEvaluator()

# Input data
question = "What are the causes of climate change?"
response = "Climate change is caused by human activities."
reference = "Human activities such as burning fossil fuels cause climate change."

# Evaluate the response
metrics = evaluator.evaluate_all(question, response, reference)

# Print the results
print(metrics)
Streamlit Web App
To run the web app:

cd into streamlit app folder.

Create a virtual environment

Activate it

Install all dependencies

Run:
streamlit run app.py
Metrics
The following metrics are provided by the library:

BLEU: Measures the overlap between the generated output and reference text based on n-grams.

ROUGE-1: Measures the overlap of unigrams between the generated output and reference text.

BERT Score: Evaluates the semantic similarity between the generated output and reference text using BERT embeddings.

Perplexity: Measures how well a language model predicts the text.

Diversity: Measures the uniqueness of bigrams in the output text.
📏 Supported Evaluation Metrics
| Metric         | Description                                                           |
| -------------- | --------------------------------------------------------------------- |
| **BLEU**       | Measures n-gram overlap between generated and reference text.         |
| **ROUGE-1**    | Measures unigram (word-level) overlap between outputs.                |
| **BERTScore**  | Uses BERT embeddings to calculate semantic similarity.                |
| **Perplexity** | Quantifies how "surprised" a language model is by the generated text. |
| **Diversity**  | Measures how unique the generated tokens or phrases are.              |
