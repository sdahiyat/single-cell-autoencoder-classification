# Dataset Description

This project uses a single-cell RNA-seq dataset consisting of 700 cells, each annotated with an immune cell type label and corresponding gene expression values. The data is split across two CSV files.

---

## `labels.csv`

This file provides the **cell type annotations** for each single-cell barcode.

| Column Name     | Description                                  |
|------------------|----------------------------------------------|
| `index`          | Unique cell barcode (e.g., `AAAGCCTGGCTAAC-1`) |
| `bulk_labels`    | Assigned immune cell type (e.g., `CD14+ Monocyte`, `Dendritic`, `CD56+ NK`, etc.) |

- **Total rows**: 700  
- **Total cell types**: Multiple distinct immune cell populations

---

## `processed_counts.csv`

This file contains **log-normalized gene expression data** for 765 genes across the same 700 cells. Each row corresponds to one cell (indexed by barcode), and each column corresponds to a gene.

| Column Name     | Description                                        |
|------------------|----------------------------------------------------|
| `Unnamed: 0`     | Cell barcode (matches `index` in `labels.csv`)     |
| All other columns | Log-normalized expression levels for individual genes (e.g., `HES4`, `TNFRSF4`, `ITGB2`, etc.) |

- **Shape**: 700 rows × 766 columns  
- **Gene Count**: 765  
- **Value Type**: Log-transformed normalized RNA-seq read counts

---

These two files serve as the input for dimensionality reduction (via autoencoders) and classification tasks in this project. No additional preprocessing beyond normalization was applied before modeling.
