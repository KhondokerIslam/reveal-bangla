# Reveal-Bangla: A Dataset for Cross-Lingual Multi-Step Reasoning Evaluation

This repository provides the experimental implementation of our BLP@AACL-IJCNLP 2025 paper: [Reveal-Bangla: A Dataset for Cross-Lingual Multi-Step Reasoning Evaluation](https://aclanthology.org/2025.banglalp-1.3.pdf). Reveal-Bangla is a manually translated Bangla multi-step reasoning dataset derived from the English _Reveal_ dataset, featuring both binary and non-binary question types.

## Abstract
Language models have demonstrated remarkable performance on complex multi-step reasoning tasks. However, their evaluation has been predominantly confined to high-resource languages such as English. In this paper, we introduce a manually translated Bangla multi-step reasoning dataset derived from the English _Reveal_ dataset, featuring both binary and non-binary question types. We conduct a controlled evaluation of English-centric and Bangla-centric multilingual small language models on the original dataset and our translated version to compare their ability to exploit relevant reasoning steps to produce correct answers. Our results show that, in comparable settings, reasoning context is beneficial for more challenging non-binary questions, but models struggle to employ relevant Bangla reasoning steps effectively. We conclude by exploring how reasoning steps contribute to models' predictions, highlighting different trends across models and languages.

## Dataset 🌟
_Reveal-Bangla_ Dataset is available [here](https://huggingface.co/datasets/khondoker/reveal-bangla).

## Working Directory Overview 📁

```prompts/``` --- __Prompt Templates__ 
- Contains all prompt templates used across languages (English, Bangla) and reasoning settings.
- Filenames are structured as `prompts_{setting_name}_{lang}.yaml`

```code/``` --- __Experimental Notebooks__ 

This folder includes the core experimental and analysis code used in the paper.
Each notebook directly corresponds to a figure in the publication:

  - ```result.ipynb``` --- __Figure 2__ 
  -  ```evaluation.ipynb``` --- __Figure 3__ 
  -  ```analysis.ipynb``` --- __Figure 4__

```results/``` --- __Model Outputs & Analysi__

- Stores all generated outputs from running the notebooks in `code/`
- File naming convention:
  `{experiment_type}_{reasoning_setting}_{language}_{model_name}.{ext}`.
- `experiment_type ∈ {results, analysis, attribution}`

```
results/
 └── <model_name>/
     └── <language>/   (Ben / Eng)
         ├── results_*.json        # outputs from `code/result`
         ├── analysis_*.csv        # outputs from `code/evaluation`
         └── attribution_*.json   # outputs from `code/analysis`
```

## Citation
```
@inproceedings{islam2025reveal,
  title={Reveal-Bangla: A Dataset for Cross-Lingual Multi-Step Reasoning Evaluation},
  author={Islam, Khondoker Ittehadul and Sarti, Gabriele},
  booktitle={Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025)},
  pages={31--43},
  year={2025}
}
```
