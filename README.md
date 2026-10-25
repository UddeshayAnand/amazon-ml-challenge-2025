# Amazon ML Challenge 2025 · Product Price Prediction

Predicting product prices from catalog descriptions and product images, with experiments spanning feature engineering, traditional machine learning, transformer models, and multimodal approaches.

**Competition outcome: rank 181 · SMAPE 44.68.** This was a collaborative challenge effort. The final submission-to-model mapping has not been recovered, so this outcome is not attributed to a particular notebook.

[Exploratory data analysis](notebooks/1.%20Exploratory%20Data%20Analysis/README.md) · [Multimodal approaches](notebooks/2.%20MultiModal%20Approach/README.md) · [Text-only approaches](notebooks/3.%20Text%20Only%20Approach/README.md) · [Data description](data/README.md) · [Problem statement](docs/Amazon%20ML%202025%20Problem%20Statement.pdf)

## Project at a glance

| Area | Included work |
|---|---|
| Problem | Price prediction from product catalog information |
| Data exploration | Price distributions, product descriptions, feature exploration, and diagnostic analysis |
| Text-only experiments | Feature-based models, BERT, T5/FLAN-T5, Granite, Qwen, and ensemble approaches |
| Multimodal experiments | CLIP-based image features and vision-language modeling |
| Featured text experiment | FLAN-T5 encoder, masked mean pooling, and an MLP predicting `log1p(price)` |
| Repository format | 34 notebooks organized into three approach folders, with supporting documentation |

## Challenge and data

The supplied challenge statement specifies 75,000 labeled training products and 75,000 test products. The task is to predict prices using product catalog information, including descriptions, quantities, and available images. External price lookup was prohibited.

The local CSV files and their column descriptions are documented in [data/README.md](data/README.md). The full training and test image collections are omitted to keep the repository size manageable; the intended `train_images/` and `test_images/` folders are left empty. Git does not retain empty directories.

The [problem statement](docs/Amazon%20ML%202025%20Problem%20Statement.pdf) is kept in `docs/`.

## Explore the experiments

| Folder | Notebooks | Focus |
|---|---:|---|
| [Exploratory Data Analysis](notebooks/1.%20Exploratory%20Data%20Analysis/README.md) | 4 | Visualization, feature engineering, diagnostics, and price-classification exploration |
| [MultiModal Approach](notebooks/2.%20MultiModal%20Approach/README.md) | 2 | Combining product descriptions with visual information |
| [Text Only Approach](notebooks/3.%20Text%20Only%20Approach/README.md) | 28 | Regression, text generation, feature extraction, similarity search, and ensembles |

The notebooks preserve the individual experiments and their existing saved outputs where present. Their data preparation, model choices, and evaluation procedures vary by experiment.

The historical FLAN-T5 regression experiment uses Huber loss on log-transformed prices and a `512 → 256 → 128 → 1` regression head.

## Recorded results

| Result | SMAPE (%) ↓ |
|---|---:|
| Competition outcome, rank 181 | 44.68 |
| Historical FLAN-T5 encoder + MLP | 45.08568 |
| Historical FLAN-T5 generation | 44.30027 |
| Historical EDA LightGBM baseline | 53.7165 |
| Historical EDA ensemble | 53.9187 |

## Repository map

```text
notebooks/
  1. Exploratory Data Analysis/   Four exploration and feature-engineering notebooks
  2. MultiModal Approach/         Two text-and-image experiment notebooks
  3. Text Only Approach/          Twenty-eight text-based experiment notebooks
data/                            Train/test CSV files and dataset description
docs/                            Challenge problem statement
```

## Scope and limitations

- This repository presents the notebook experiments and their supporting materials.
- Image collections and trained checkpoints are not bundled.
- Evaluation procedures differ across notebooks; consult each experiment for its context.
- The competition outcome belongs to the collaborative effort and is not assigned to a specific notebook.

## References

- [FLAN-T5-XL model card](https://huggingface.co/google/flan-t5-xl)
- [Transformers T5 documentation](https://huggingface.co/docs/transformers/model_doc/t5)
- [Scaling Instruction-Finetuned Language Models](https://arxiv.org/abs/2210.11416)
