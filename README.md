# Budgeted Multi-Source Counterfactual Annotation for Off-Policy Evaluation

[![NeurIPS 2026](https://img.shields.io/badge/NeurIPS-2026%20Poster-blue.svg)](https://openreview.net/forum?id=446GKdY1L2)
[![arXiv](https://img.shields.io/badge/arXiv-2610.10974-b31b1b.svg)](https://arxiv.org/abs/2610.10974)
[![OpenReview](https://img.shields.io/badge/OpenReview-446GKdY1L2-8c1b13.svg)](https://openreview.net/forum?id=446GKdY1L2)

This repository contains the official implementation of the paper:  
**"Budgeted Multi-Source Counterfactual Annotation for Off-Policy Evaluation"**  
Accepted to **NeurIPS 2026 (Main Track, Poster)**.

[[Paper (arXiv)]](https://arxiv.org/abs/2610.10974) | [[OpenReview]](https://openreview.net/forum?id=446GKdY1L2)

## Repository Structure

* `ASSIT_DT.ipynb`: The script for processing the dataset and querying multiple Large Language Models (Gemini, GPT, Claude) to generate annotations.
* `OPE_Annotation_Optimization.ipynb`: The primary notebook containing the implementation of Off-Policy Evaluation estimators and the annotation optimization framework for synthetic clinical and semi-synthetic ASSISTments bandits.

## Data Preparation

Due to file size constraints, the primary dataset is not included in this repository. It must be downloaded and prepared prior to executing the notebooks.

1. Access the 2012-13 school data from the ASSISTments dataset repository:  
   https://sites.google.com/site/assistmentsdata/2012-13-school-data-with-affect
2. Download the dataset and rename the file to `ASSIT.csv`.
3. Place `ASSIT.csv` directly into the root directory of this repository.

## Configuration

The annotation generation process requires valid API keys for the respective LLM services. 

1. Open `ASSIT_DT.ipynb`.
2. Navigate to the sections designated for Gemini, GPT, and Claude.
3. Replace the placeholder string `API_KEY = "your_api_key"` with your actual API keys.

## Execution Pipeline

To properly reproduce the experimental results, the notebooks must be executed in sequential order:

1. Execute `ASSIT_DT.ipynb`. This step processes the `ASSIT.csv` data and generates the necessary LLM annotations.
2. Once the LLM annotations are saved, execute `OPE_Annotation_Optimization.ipynb`. The LLM-specific sections within this notebook depend directly on the output generated in step 1.

---

## Citation

If you find this work or codebase useful in your research, please cite:

```bibtex
@inproceedings{xiang2026budgetedCFOPE,
  title={Budgeted Multi-Source Counterfactual Annotation for Off-Policy Evaluation},
  author={Xiang, Biao and Eshragh, Ali and Li, Yuexing and Wang, Kai},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2026},
  url={[https://openreview.net/forum?id=446GKdY1L2](https://openreview.net/forum?id=446GKdY1L2)}
}
