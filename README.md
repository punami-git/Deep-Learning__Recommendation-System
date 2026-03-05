# Deep Learning Recommendation System

## Short Summary
This project develops a two stage deep learning recommendation system for fashion products. It combines customer profiles, article metadata, transaction behavior, and **ResNet-152 image embeddings** to generate high quality personalized recommendations.

The core model uses a **two-tower neural network** (customer tower + item tower) for fast candidate retrieval at scale, followed by a ranking model that re-scores those candidates and returns top-k results. The image embeddings add visual style signals that structured/tabular features alone cannot capture.

What makes this pipeline different is its **multimodal design**: it unifies user behavior, structured product/customer features, and image semantics in one end-to-end recommendation workflow.

## What It Does
- Loads and preprocesses customer, article, and transaction datasets.
- Creates a time based train/validation/test split.
- Engineers behavioral and metadata-driven features.
- Trains a two stage TensorFlow Recommenders model for retrieval and ranking.
- Retrieves likely candidate items using the two tower architecture.
- Re-ranks candidates to produce final top-k recommendations.
- Filters previously purchased items during inference.
- Evaluates performance using Precision@K, Recall@K, and NDCG@K.

## Main File
- `Final Code.ipynb`

## Setup
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Optional Dev Tooling
```bash
pip install -r requirements-dev.txt
```

## Environment Variables
Use `.env.example` as a template and set local paths for:
- dataset directory
- article embeddings file
- cache/output locations
- runtime settings (epochs, batch size, seed)

## Notebook Run Order
1. Imports + seed setup
2. Data loading/filtering
3. Temporal split
4. Feature engineering + preprocessing
5. Model training
6. Inference
7. Evaluation
