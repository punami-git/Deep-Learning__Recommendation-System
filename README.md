# Recommendation System


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

## Environment Configuration
1. Copy `.env.example` values into your shell environment.
2. Set paths for your local dataset and article embeddings.

## Notebook Execution Order
1. Imports + seed setup
2. Data loading/filtering
3. Temporal split
4. Feature engineering + preprocessing
5. Model training
6. Inference
7. Evaluation

## Formatting / Linting (Optional)
```bash
black .
isort .
ruff check .
```