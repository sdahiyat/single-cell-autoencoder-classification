# Single-Cell RNA-seq: Autoencoder + Classification Pipeline

This repository contains coursework for a two-part project focused on analyzing single-cell RNA-seq data using both unsupervised and supervised learning techniques.

The project uses:
- **Dimensionality reduction** via an autoencoder
- **Classification** of immune cell types using a neural network

All code is written in Python using `PyTorch`, `scikit-learn`, and `pandas`.

---

## Files

- `Final_Project_Part_1_Autoencoder.ipynb`  
  Trains an autoencoder to learn a compact representation of gene expression data from 765 genes across thousands of single cells.

- `Final_Project_Part_2_Classification.ipynb`  
  Uses the low-dimensional embeddings from Part 1 to classify cell types using a neural network.

---

## Dataset

The dataset contains:
- **`processed_counts.csv`**: log-normalized gene expression values for each cell
- **`labels.csv`**: annotated immune cell types for each cell

Note: The dataset is not included in this repository due to size and course policy. 
