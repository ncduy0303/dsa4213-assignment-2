# DSA4213 Assignment 2: Build and Compare Small Language Models

This repository contains a solution for Assignment 2, focusing on building, training, and comparing small language models for next-token prediction. The project implements and evaluates an **LSTM** and a **Transformer (Decoder-only)** model on the Sherlock Holmes text corpus.

The entire workflow - from data download to model analysis - is encapsulated within a single Jupyter Notebook (`Assignment2.ipynb`).

## 📋 Table of Contents

- [DSA4213 Assignment 2: Build and Compare Small Language Models](#dsa4213-assignment-2-build-and-compare-small-language-models)
  - [📋 Table of Contents](#-table-of-contents)
  - [🚀 Project Overview](#-project-overview)
  - [📁 Repository Structure](#-repository-structure)
  - [⚙️ Setup and Installation](#️-setup-and-installation)

## 🚀 Project Overview

The primary goals of this assignment are:

- **Implementation**: Build and train an LSTM and a Transformer model using PyTorch.
- **Dataset**: Use "The Canon of Sherlock Holmes" text, split into 80/10/10 for training, validation, and testing.
- **Evaluation**: Compare the models quantitatively using cross-entropy loss and perplexity, as well as qualitatively through generated text samples.
- **Ablation Studies**: Investigate the impact of different hyperparameters (embedding size, number of layers, context length, etc.) and tokenization schemes (word vs subword vs character).
- **Generation**: Demonstrate the models' generative capabilities using different temperature sampling strategies.

## 📁 Repository Structure

```bash
dsa4213-assignment-2/
├── .gitignore
├── data/
│   └── (This directory will be created automatically for the dataset)
├── models/
│   └── (This directory will be created automatically for saved models)
├── figures/
│   └── (This directory stores training curves and analysis plots for the report)
├── Assignment2.ipynb
├── Assignment2.pdf
├── README.md
└── requirements.txt
```

## ⚙️ Setup and Installation

Follow these steps to set up the local environment. Model weights are included in the repository at `models/` (it was training using a P100 GPU on Kaggle Notebook at [https://www.kaggle.com/code/nguyncaoduy/dsa4213-assignment-2](https://www.kaggle.com/code/nguyncaoduy/dsa4213-assignment-2)).

1. **Clone the repository:**

   ```bash
   git clone <your-repo-url>
   cd dsa4213-assignment-2
   ```

2. **Create a virtual environment (recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Install Quarto CLI:**
   To render the `.ipynb` file to PDF, you need to install the Quarto CLI. Follow the instructions at [quarto.org](https://quarto.org/docs/get-started/). You will also need a LaTeX or Typst engine for PDF generation.
