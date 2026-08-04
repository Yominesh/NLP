# Chapter 1 Assignments

**Author:** Yominesh Giri

## Overview

This folder contains all assignments for Chapter 1.

## Requirements

- Python 3.12+
- spaCy 3.8+
- `en_core_web_sm` language model

Install dependencies:

```bash
pip install spacy
python -m spacy download en_core_web_sm
```

---

## Assignment 01: Part-of-Speech (POS) Extraction

**Notebook:** `YomineshGiri_POS_01.ipynb`

### Objective

Identify and extract nouns and verbs from an English news article.

### Article Source

BBC News – *"How Wimbledon cracked cricket-obsessed India"*

### Files

| File | Description |
|------|-------------|
| `YomineshGiri_POS_01.ipynb` | Notebook with all code and analysis |
| `article.txt` | Source news article text (863 words) |
| `YomineshGiri_POS_01.csv` | Output CSV with extracted nouns and verbs |

### Approach

1. Load spaCy's pretrained `en_core_web_sm` English model.
2. Read the news article from `article.txt`.
3. Run the text through the spaCy pipeline to assign a POS tag to every token.
4. Filter to keep only alphabetic tokens tagged as `NOUN` or `VERB`.
5. Save the results to a CSV with columns `Word` and `POS_Tag`.

### Results

Out of 863 words in the article, **331 were extracted** as nouns or verbs.

### Key Takeaway

spaCy's POS tagger predicts each tag based on sentence context which means the same word can receive different tags depending on how it is used, demonstrating context-aware NLP in practice.

---
