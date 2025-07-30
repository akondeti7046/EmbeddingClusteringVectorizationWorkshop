# EmbeddingClusteringVectorizationWorkshop
lab 9 

# EmbeddingClusteringVectorizationWorkshop

## Overview
This notebook demonstrates how to train and compare two popular word‐embedding techniques—**Word2Vec** and **GloVe**—on the real‑world IMDb Movie Reviews dataset. You will learn how to:

- Load and preprocess the IMDb reviews using TensorFlow Datasets and NLTK  
- Train a 100‑dimensional Word2Vec model on the review corpus  
- Download and load 100‑dimensional pretrained GloVe vectors via Gensim  
- Compare nearest‑neighbor results and discuss strengths & limitations of each method  

## Contents
1. **Data Preparation**  
   - Download IMDb reviews with `tensorflow_datasets`  
   - Tokenize and normalize text using NLTK  
2. **Word2Vec**  
   - Train a skip‑gram model on your tokenized sentences  
   - Query similar words (e.g., `model_w2v.wv.most_similar('movie')`)  
3. **GloVe**  
   - Download Stanford’s pretrained 100d embeddings  
   - Wrap with a header and load via `KeyedVectors`  
   - Query similar words (e.g., `glove_vectors.most_similar('movie')`)  
4. **Comparison & Talking Points**  
   - Side‑by‑side table of predictive vs. count‑based approaches  
   - Discussion of domain‑specific slang capture vs. broader semantics  

## Prerequisites
- Python 3.7+  
- pip  
- Virtual environment (highly recommended)

## Installation
```bash
# Clone the repo
git clone https://github.com/YourUserName/EmbeddingClusteringVectorizationWorkshop.git
cd EmbeddingClusteringVectorizationWorkshop

# Create & activate a venv (optional but recommended)
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install tensorflow-datasets gensim nltk
