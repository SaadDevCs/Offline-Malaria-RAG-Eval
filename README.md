# Offline Malaria RAG: Safe Knowledge Synthesis with Small Language Models

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/)
[![Framework: Google Colab](https://img.shields.io/badge/Framework-Google%20Colab-F9AB00.svg)](https://colab.research.google.com/)

This repository contains the supplementary evaluation data and Python notebooks for our research on deploying strictly constrained Small Language Models (SLMs) for clinical decision support in low-connectivity, malaria-endemic regions. 

Our study introduces the **"Scaling Paradox"** in medical AI, demonstrating that massive cloud-based architectures (e.g., 120B parameter models) and heavily instruction-tuned SLMs often suffer from "helpfulness bias," failing to adhere to strict clinical safety constraints. Conversely, our edge-optimized pipeline successfully executes deterministic, offline RAG.

## ⚠️ Data Availability Notice
> **Note on Dataset Size:** The files provided in the `data/` directory represent a **representative subset** of the complete global dataset used in our full study. 
>
> Due to GitHub's file size and storage bandwidth limitations for large-scale processed text corpora, we cannot host the entire uncompressed database here. However, this repository contains the exact processed document formats, the adversarial evaluation queries, and sufficient data to fully execute the pipeline, reproduce our methodology, and generate the core performance metrics (Constraint Adherence Rate and Token Verbosity) discussed in the paper. The full global dataset is available upon reasonable request to the corresponding author.

## 📂 Repository Structure

* `data/`
  * Contains the subset of processed document chunks used for the Retrieval-Augmented Generation context.
  * Contains the evaluation outputs and `.csv` files recording the latency, token verbosity, and Constraint Adherence Rate (CAR) across the evaluated models (Qwen-2.5-Instruct, Llama-3.2, Phi-3-Mini, Llama-70B, GPT-120B).
* `LLM_Malaria_Recent.ipynb`
  * The primary Google Colab notebook containing the Python scripts to run the evaluation loop, calculate performance metrics, and generate the dual-axis "Scaling Paradox" figure.

## 🚀 Getting Started & Reproducibility

To run the evaluation pipeline or reproduce the data visualizations:

1. Open the `LLM_Malaria_Recent.ipynb` notebook directly in Google Colab.
2. Clone this repository into your Colab environment or mount your Google Drive to access the files in the `data/` folder.
3. Run the analysis cells to output the quantitative evaluation metrics and the matplotlib figures.

## 📖 Citation

If you use this dataset or methodology in your research, please cite our paper:

```bibtex
@inproceedings{abouzahir2026malariarag,
  title={Offline Malaria RAG: Safe Knowledge Synthesis with Small Language Models},
  author={Abouzahir, Saad and Salem, Mostafa and others},
  booktitle={Proceedings of the [Insert Conference Name]},
  year={2026}
}
