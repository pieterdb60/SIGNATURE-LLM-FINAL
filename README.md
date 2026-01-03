# SIGNATURE-LLM: Cell2Sentence Tutorial Series

A comprehensive tutorial series demonstrating the use of Large Language Models (LLMs) for single-cell transcriptomics analysis using the [Cell2Sentence (C2S)](https://github.com/vandijklab/cell2sentence) framework.

## Overview

This repository contains hands-on Jupyter notebooks that guide you through the process of:
- Converting single-cell RNA sequencing data into text representations
- Using pre-trained LLMs for cell type annotation
- Fine-tuning models on custom datasets
- Generating synthetic cell data
- Performing downstream pathway inference

## What is Cell2Sentence?

Cell2Sentence bridges numeric gene expression data and text-based LLMs by converting each cell's expression profile into a 'sentence' of genes, sorted by expression level. This approach enables:
- Cell type annotation via natural language classification
- Generative modeling for synthetic cells
- Marker identification and text-based data mining

## Notebooks

The tutorial is organized into the following notebooks:

1. **[Introduction and Setup](1_Introduction_and_Setup.ipynb)** - Environment setup and introduction to the Cell2Sentence framework
2. **[Preprocessing and Cell2Sentence](2_Preprocessing_and_Cell2Sentence.ipynb)** - Loading scRNA-seq data and converting to cell sentences
3. **[Annotation with LLM](3_Annotation_with_LLM.ipynb)** - Using pre-trained models for cell type prediction
4. **[Finetuning on New Datasets](4_Finetuning_on_New_Datasets.ipynb)** - Adapting models to custom datasets
5. **[Cell Type Prediction](5_Cell_Type_Prediction.ipynb)** - Advanced prediction techniques
6. **[Synthetic Cell Generation](6_Synthetic_Cell_Generation.ipynb)** - Generating synthetic cell data with LLMs
7. **[Progeny Pathway Inference](7_progeny_pathway_inference_downstream_AI.ipynb)** - Downstream pathway analysis
8. **[Why Not Use General SOTA LLMs?](8_Why_dont_we_use_a_general_SOTA_LLM.ipynb)** - Discussion on specialized vs. general models

## Requirements

- Python 3.8+
- Conda (recommended) or pip
- CUDA-compatible GPU (optional, for faster training)

### Core Dependencies

- `cell2sentence` - The Cell2Sentence framework
- `scanpy` - Single-cell analysis in Python
- `torch` - PyTorch for deep learning
- `transformers` - Hugging Face transformers library
- `numpy`, `pandas` - Data manipulation
- `matplotlib`, `seaborn` - Visualization

## Installation

### Using Conda (Recommended)

```bash
# Create a new conda environment
conda create -n cell2sentence_env python=3.8 -y
conda activate cell2sentence_env

# Install Cell2Sentence and dependencies
pip install cell2sentence
```

### Using pip

```bash
# Ensure Python 3.8+ is installed
pip install cell2sentence
```

### Verify Installation

```python
import cell2sentence as c2s
import scanpy as sc
import torch
import transformers

print("Cell2Sentence version:", c2s.__version__)
print("CUDA available:", torch.cuda.is_available())
```

## Getting Started

1. Clone this repository
2. Set up your environment using the installation instructions above
3. Launch Jupyter Notebook or JupyterLab
4. Start with notebook 1 and work through the series sequentially

```bash
# Launch Jupyter
jupyter notebook

# Or JupyterLab
jupyter lab
```

## Usage

Each notebook is self-contained with:
- Learning objectives
- Step-by-step code examples
- Explanations of key concepts
- Visualization of results

Follow the notebooks in order for the best learning experience, or jump to specific topics based on your needs.

## Dataset

The tutorials use the PBMC 3k dataset (peripheral blood mononuclear cells) from Scanpy as a demonstration dataset. This contains approximately 2,700 cells and is ideal for learning purposes.

## Key Features

- **Rank-Based Representation**: Convert expression values to gene rankings that preserve ~88% of variance
- **LLM Integration**: Leverage transformer models for biological interpretation
- **Reversible Transformation**: Reconstruct expression profiles from cell sentences
- **Visualization**: UMAP plots and comparative analysis tools
- **Flexible Framework**: Applicable to various single-cell datasets and cell types

## Resources

- [Cell2Sentence GitHub](https://github.com/vandijklab/cell2sentence)
- [Cell2Sentence Paper](https://openreview.net/pdf?id=EWt5wsEdvc)
- [Scanpy Documentation](https://scanpy.readthedocs.io/)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/)

## License

Please refer to the individual notebook licenses and the Cell2Sentence library license for usage terms.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## Acknowledgments

This tutorial series is built upon the Cell2Sentence framework developed by the van Dijk Lab.
