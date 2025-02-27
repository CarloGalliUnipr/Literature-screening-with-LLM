# Systematic Review Script

This repository contains a Python script designed to assist with systematic reviews in periodontology. The script performs the following tasks:

- **PubMed Data Fetching and Parsing:** Retrieves and parses PubMed records using a list of predefined PMIDs or through a search query with date-range chunking.
- **Embedding Generation & Similarity Calculation:** Encodes article titles and abstracts using a SentenceTransformer, then calculates cosine similarity between target articles and a pool of candidate articles.
- **Data Sub-sampling and Quartile Division:** Divides articles into quartiles based on similarity scores and creates merged datasets.
- **GPT-3.5 Turbo Classification:** Uses GPT-3.5 Turbo to classify articles as **ACCEPT** or **REJECT** based on a “soft approach” or a detailed evaluation prompt.

## Features

- **PubMed Integration:** Fetch and parse records using Biopython.
- **Text Embedding:** Generate sentence embeddings with SentenceTransformers.
- **Similarity Analysis:** Compute cosine similarity to rank articles.
- **Article Screening:** Leverage GPT-3.5 Turbo for zero-shot classification of articles.
- **CSV Output:** Save processed data and classification results in CSV format.

## Requirements

- Python 3.6+
- [Biopython](https://biopython.org/)
- [SentenceTransformers](https://www.sbert.net/)
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [requests](https://docs.python-requests.org/)
- [openai](https://github.com/openai/openai-python)

You can install all dependencies with:

```bash
pip install biopython sentence-transformers pandas numpy requests openai
