# Skip-gram with Negative Sampling (SGNS)

## Overview

This assignment implements **Skip-gram with Negative Sampling (SGNS)** from scratch using **Python and NumPy**, without using a deep learning framework.

The main goal is to understand how SGNS learns word embeddings from word co-occurrence information.

## What the Notebook Covers

The notebook includes the following steps:

1. Generate a synthetic text corpus.
2. Preprocess the text and build the vocabulary.
3. Remove very rare words using a minimum-count threshold.
4. Apply subsampling to frequent words.
5. Generate center-context word pairs using a dynamic context window.
6. Create a negative-sampling distribution.
7. Initialize the word embeddings.
8. Calculate the SGNS objective and gradients manually.
9. Train the embeddings using stochastic gradient descent.
10. Evaluate the learned embeddings.
11. Visualize the embeddings using PCA.

## Improvements Made

Several changes were made to make the experiment more robust:

- A larger synthetic corpus is used to provide more training examples.
- Context windows are sampled dynamically.
- Training pairs are regenerated for each epoch.
- Negative sampling is used during training.
- The learning rate is gradually reduced during training.
- Both input and output embeddings are considered when evaluating the learned vectors.
- Several evaluation methods are included, such as nearest neighbours, analogies, cosine similarity, and PCA.

## Training

The model is trained using manually implemented stochastic gradient descent.

The main training settings include:

- **Embedding dimension:** 50
- **Context window:** 4
- **Negative samples:** 5
- **Initial learning rate:** 0.05
- **Final learning rate:** 0.0005
- **Training epochs:** 30

These values are chosen for this small synthetic experiment and are not intended to reproduce the settings used by large-scale Word2Vec models.

## Evaluation

The learned embeddings are evaluated in several ways.

### Nearest Neighbours

The notebook finds words that are closest to a selected word in the learned embedding space.

### Word Analogies

The notebook tests relationships between words using vector arithmetic.

### Cosine Similarity

Known word relationships are compared using cosine similarity to see whether related words have similar representations.

### PCA Visualization

Principal Component Analysis (PCA) is used to project the word vectors into two dimensions so that their structure can be visualized.

## Important Note About the Dataset

The corpus used in this assignment is **synthetic**. It is relatively small compared with the datasets normally used to train real Word2Vec models.

Therefore, the results should not be expected to match pretrained embeddings trained on millions or billions of words. The purpose of this assignment is to demonstrate the SGNS algorithm and show how meaningful word relationships can emerge from word co-occurrence.

## Requirements

The notebook requires:

- Python 3
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook or Google Colab

## Running the Notebook

The notebook can be opened and executed using Jupyter Notebook, JupyterLab, or Google Colab.

Run the cells from top to bottom because later sections depend on variables and embeddings created during earlier sections.

## Output

The notebook produces:

- Vocabulary statistics
- Training progress and average loss
- Nearest-neighbour results
- Analogy results
- Cosine-similarity results
- PCA visualization

## Files

- `Skip-gram with Negative Sampling (SGNS)` — SGNS implementation and experiments
- `README.md` — project documentation

## Conclusion

This assignment demonstrates the complete SGNS pipeline from corpus preparation and training-pair generation to manual gradient updates and embedding evaluation.

