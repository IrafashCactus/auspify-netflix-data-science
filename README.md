# Auspify Netflix Data Science

A task-oriented workspace for the Netflix data science project.

## Project structure

- `data/raw/`: Original source data, including `Dataset.csv`. Keep source files unchanged.
- `data/processed/`: Cleaned and transformed datasets, including `netflix_clean.csv`.
- `notebooks/`: One Jupyter notebook per task.
- `docs/`: Project decisions, methodology, and findings.
- `evidence/`: Screenshots organized into one folder per task.
- `reports/`: Final project reports and deliverables.

## Setup

Install the project dependencies with:

```bash
python -m pip install -r requirements.txt
```

Place the original dataset in `data/raw/`. Write cleaned outputs to `data/processed/`; do not edit the original file.
