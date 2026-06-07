# Postie Data Science Challenge

This repository contains my work for the Postie data science challenge.

The current version of the project focuses on initial data acquisition, validation, and exploratory analysis. I have not yet attempted to answer the challenge questions directly in this stage. Instead, the goal is to understand the structure and behavior of the transaction logs, identify notable data patterns, and document items that may require deeper analysis.

## Current Status

This repository currently includes:

- reproducible data acquisition from the public challenge data source,
- initial data loading and timestamp normalization,
- exploratory summaries of daily sales and transaction behavior,
- visual analysis of sales, transaction counts, order values, website behavior, and app version behavior,
- notes on unusual transaction values, including large outliers and negative checkout amounts,
- generated figures and summary tables saved to local output folders.

The next stage of work will use these exploratory findings to answer the challenge questions directly.

## Repository Structure

```text
postie-data-science-presentation/
│
├── README.md
├── exploratory_notes.md
├── environment.yml
├── .gitignore
│
├── notebooks/
│   └── 01_exploration.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── outputs/
│   ├── figures/
│   └── tables/
│
└── presentation/
```

## Key Files

### Exploratory Notebook

[`notebooks/01_exploration.ipynb`](notebooks/01_exploration.ipynb)

This notebook contains the initial exploratory analysis. It acquires the raw transaction logs, loads them into pandas, performs light validation and cleanup, generates summary tables, and creates exploratory plots.

### Initial Data Impressions

[`exploratory_notes.md`](exploratory_notes.md)

This markdown file summarizes the main patterns and anomalies noticed during the exploratory phase. It is intended as a lightweight, skimmable companion to the notebook.

Current exploratory themes include:

- timestamp normalization and daily date boundaries,
- day-to-day sales and transaction behavior,
- large transaction outliers,
- the app version transition on July 3,
- negative checkout amounts appearing only on July 3.

### Generated Outputs

Generated figures are saved in:

```text
outputs/figures/
```

Generated summary tables are saved in:

```text
outputs/tables/
```

These outputs are used by the exploratory notes and will support the later analysis/reporting stages.

## Setup

This project uses conda.

Create the environment:

```bash
conda env create -f environment.yml
```

Activate the environment:

```bash
conda activate postie
```

If needed, register the environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name postie --display-name "Python (Postie)"
```

Then open the notebook in VS Code or Jupyter:

```text
notebooks/01_exploration.ipynb
```

## Data Notes

The raw transaction logs are acquired programmatically from the public challenge data source.

Local data files are stored under:

```text
data/raw/
data/processed/
```

Depending on repository settings, raw and processed data may be excluded from version control. The notebook is intended to make data acquisition and processing reproducible.

## Exploratory Notes So Far

The initial exploration suggests several items are worth carrying forward:

- negative checkout amounts occur only on July 3 and are consistently `-12`,
- July 3 includes an app version transition from `1.1` to `1.2`,
- checkout amounts are highly skewed due to a small number of very large transactions,
- timestamp normalization should be explicit when calculating daily totals,
- daily total sales should be interpreted alongside transaction count, median order value, website behavior, app version behavior, and hourly patterns.

These are preliminary observations only. They are not yet final answers to the challenge questions.
