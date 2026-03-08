# Bangla-Hate-Speech-Intensity-Classification
This repository presents a Bangla hate speech intensity classification system, the first of its kind, designed to classify the intensity of hate speech in Bengali text.

---



## Overview

The project focuses on understanding and quantifying hate speech in Bangla by building a robust classification pipeline. Key contributions include:

1. **Dataset Collection & Annotation**
   - Collected a large dataset of Bangla text from multiple sources.
   - Filtered and extracted **hate speech-related data**.
   - Annotated **~11,000+ samples** with intensity levels and categories.

2. **Modeling Approaches**
   - **Logistic Regression** with advanced feature engineering.
   - **BanglaBERT** fine-tuning for contextual embeddings.
   - **mBERT (Multilingual BERT)** for cross-lingual embeddings.
   
3. **Unique Contribution**
   - First-ever study on **Bangla hate speech intensity classification**.
   - Achieves high accuracy across multiple modeling approaches.

---

## Dataset

The dataset includes the following columns:

| Column Name | Description |
|------------|-------------|
| `sentence` | Original text |
| `intensity_level` | Categorical intensity label |
| `intensity_level_normalized` | Normalized numeric label |
| `intensity_category` | Hate speech category |
| `clean_sentence` | Preprocessed text (optional) |

> Note: Preprocessed versions (`clean_sentence`) are used for modeling, but can be omitted for raw text experiments.

---

## Intensity Level Definitions

| Level | Name | Description |
|-------|------|-------------|
| 1 | Disagreement | Mild criticism of ideas, opinions, beliefs, policies. No insults, animals, or violence. |
| 2 | Negative Actions | Criticism of actions, corruption, hypocrisy, betrayal. Not direct insults or animals. |
| 3 | Negative Character | Personal/direct insults (e.g., শালা, হারামজাদা). Attacks on morality or character. Not dehumanizing. |
| 4 | Dehumanizing | Comparing to animals, insects, demons (কুকুর, শুয়োর, জানোয়ার). |
| 5 | Violence | Threats of beating, rape, torture. No explicit killing. |
| 6 | Death | Calls for murder, execution, extermination. Explicit kill words: মেরে ফেলো, ফাঁসি, হত্যা, ধ্বংস, etc. |

---

## Usage

- Preprocess and split the dataset into **training, validation, and test sets**.
- Train **Logistic Regression**, **BanglaBERT**, or **mBERT** models for hate speech intensity classification.
- Evaluate models on **test data** and analyze performance by **intensity level** and **category**.

---

## Requirements

- Python >= 3.8
- Libraries: `pandas`, `torch`, `transformers`, `scikit-learn`, `tqdm`
- GPU recommended for BERT training.

---

## Key Highlights

- First work on **Bangla hate speech intensity classification**.
- Multi-model comparison ensures robustness.
- Includes both **traditional ML** and **deep learning approaches**.

---

## License

This project is released under the **MIT License**.

---

## Citation

If you use this dataset or code, please cite this repository.
