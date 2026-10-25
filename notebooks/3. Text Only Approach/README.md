# 📝 Text Only Approach

This folder contains **28 notebooks** exploring price prediction from **text** inputs (`catalog_content`), spanning feature-based machine learning, transformer models, and ensembles.

**Competition outcome: rank 181 · SMAPE 44.68.** This is the collaborative competition result. The final submission-to-model mapping has not been recovered, so the result is not attributed to an individual notebook. See the [project overview](../../README.md) for the recorded experiment results.

## Ensemble Experiments

### 🥇 **`hybrid-ensemble-validation-test-gap-fixes.ipynb`** 

- **Focus**: Hybrid ensemble experiment
- **Architecture**: Hybrid ensemble with adversarial validation and gap fixes
- **Key Innovations**: Separate feature scaling, stronger embeddings, residual connections

### 🚀 **`advanced-hybrid-solution.ipynb`**

- **Focus**: Ensemble approach combining multiple model families
- **Architecture**: 4-model ensemble (LightGBM + CatBoost + XGBoost + Neural Network)
- **Features**: Sentence transformers, advanced target encoding, price clustering

## 🤖 **Large Language Model Approaches**

### 💎 **Granite Models**

- **`granite-4.0-llm-price-prediction-with-unsloth.ipynb`** - Granite 4.0 with Unsloth optimization
- **`final-granite-amazon-25.ipynb`** - Main Granite implementation  
- **`final-granite-amazon-25-alternative.ipynb`** - Alternative Granite approach

### 🔮 **Qwen Models**  

- **`qwen2-5-finetune-text-only.ipynb`** - Qwen2.5 text-only fine-tuning
- **`qwen-optimized-fast-training.ipynb`** - Optimized Qwen training pipeline

## 🔤 **Encoder Model Approaches**

### 🤖 **T5/FLAN-T5 Family**

- **`flan-t5-model-main-third-method-dynamic-length.ipynb`** - FLAN-T5 with dynamic length handling
- **`flan-t5-model-main-inference.ipynb`** - FLAN-T5 inference pipeline  
- **`flan-t5-model-main-final.ipynb`** - Additional FLAN-T5 experiment
- **`flan-t5-mlp-regression-log-transformed.ipynb`** - T5 + MLP with log transformation
- **`t5-conditional-generation-pytorch-lightning.ipynb`** - T5 with PyTorch Lightning
- **`t5-conditional-generation-pytorch-lightning-alt.ipynb`** - Alternative T5 PyTorch approach
- **`t5-encoder-neural-network-price-classification.ipynb`** - T5 encoder + neural network
- **`updated-t5-model-aug-data.ipynb`** - T5 with data augmentation

### 🧠 **BERT Family**

- **`bert-regression-model-price-prediction.ipynb`** - BERT-based regression
- **`modern-bert-mmd-loss-price-prediction.ipynb`** - Modern BERT with MMD loss  
- **`comprehensive-bert-text-preprocessing-model.ipynb`** - BERT with advanced preprocessing
- **`text-only-bert-optimized-approach.ipynb`** - Optimized BERT implementation

## 🔧 **Feature Extraction & Engineering**

### 🤖 **LLM-Based Feature Extraction**

- **`llm-batch-feature-extraction-15-fields.ipynb`** - Comprehensive 15-field feature extraction
- **`vllm-ultra-fast-feature-extraction-a100.ipynb`** - Ultra-fast GPU-optimized extraction (A100)
- **`llm-feature-extraction.ipynb`** - General LLM feature extraction pipeline

### 🛠️ **Traditional Feature Engineering**

- **`ml-feature-engineering-approach.ipynb`** - Traditional ML with engineered features
- **`faiss-similarity-search.ipynb`** - FAISS-based similarity search

## 📊 **Traditional ML & Specialized Approaches**

### 🌳 **Gradient Boosting**

- **`gradient-boosting-solution-amazon-ml.ipynb`** - Gradient boosting implementation

### 🧪 **Specialized Techniques**

- **`multi-task-t5-beam-search-learning.ipynb`** - Multi-task T5 with beam search
- **`tensorflow-lstm-price-prediction-model.ipynb`** - LSTM-based neural network
- **`amazon-ml-price-prediction.ipynb`** - General ML approach

## Reading the Results

The notebooks use different validation splits and training procedures. Read reported scores in each experiment's context rather than treating the collection as a controlled leaderboard. Saved outputs are retained where present.

## 🔧 **Model Categories**

### 🚀 **Large Language Models (7B+ Parameters)**

- **Granite 4.0**, **Qwen2.5** - State-of-the-art LLMs
- Fine-tuning with Unsloth optimization
- Direct text-to-price generation

### 🔤 **Encoder Models (100M-1B Parameters)**  

- **T5/FLAN-T5**, **BERT** variants
- Text encoding + regression heads
- Efficient training and inference

### 📊 **Traditional ML (Feature-Based)**

- **LightGBM**, **XGBoost**, **CatBoost**
- Hand-crafted and LLM-extracted features
- Fast training, interpretable results

### 🧪 **Hybrid Approaches**

- **Ensemble methods** combining multiple model types
- **Feature fusion** from different extraction methods
- **Multi-stage pipelines** (extract → encode → predict)

## Explore by Topic

- **Ensembles**: `hybrid-ensemble-validation-test-gap-fixes.ipynb` and `advanced-hybrid-solution.ipynb`
- **Transformer regression and generation**: the BERT, T5/FLAN-T5, Granite, and Qwen notebooks
- **Feature engineering and extraction**: the ML and LLM feature-extraction notebooks
- **Similarity search**: `faiss-similarity-search.ipynb`

