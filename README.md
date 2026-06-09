# Postie Data Challenge

This repository contains my analysis for the Postie data challenge.

I approached the project in two parts. First, I explored the raw transaction data to understand the structure, patterns, and potential data-quality concerns. Then, I used those findings to answer the requested challenge questions.

A quick note on format: the notebooks are intentionally more detailed than the written summary. I used the notebooks as my working analysis space, so they include exploratory checks, intermediate outputs, and a few paths I investigated to understand the data more fully. The markdown files are the cleaner review materials: they summarize the main findings, reasoning, and evidence without requiring the reader to work through every exploratory step.


## Exploratory Analysis

The exploratory analysis focuses on understanding the dataset before moving into the requested questions. I used this stage to check how the data was structured, whether fields needed to be normalized, and whether any values stood out as unusual or potentially important for interpretation.

Some of the main checks included:

- **Apples-to-apples checks:** Are the values being compared on the same basis (is normalization required)?
- **Missing-value checks:** Are any important fields missing?
- **Distribution and outlier checks:** Are checkout values skewed or affected by unusually large transactions?
- **Unexpected-value checks:** Are there negative values, mixed types, or other records that need additional context?

| File | Description |
|:---|:---|
| [`exploratory_notes.md`](exploratory_notes.md) | Clean readable notes on the initial data observations and data-quality questions |
| [`notebooks/00_exploration.ipynb`](notebooks/00_exploration.ipynb) | Full exploratory notebook with code, intermediate checks, outputs, and visualizations |

## Requested Analysis

The requested analysis answers the challenge questions directly, using the cleaned data and findings from the exploratory analysis.

The analysis addresses:

1. Why was the `2017-07-03` sales value reported as much lower than the previous day?
2. Other than average sales value per day, what other metrics should be used? Is average sales value the right metric?
3. What information can be extracted from the URLs? Can product prices be inferred?
4. Are there interesting purchasing combinations, events, or metrics worth reporting?
5. Can total sales for `2017-07-04` be predicted? How certain is that prediction?
6. What additional information, data, or access would make the prediction better?

| File | Description |
|:---|:---|
| [`postie_findings_summary.md`](postie_findings_summary.md) | Clean written summary of the challenge-question responses, including the main evidence, reasoning, and conclusions |
| [`notebooks/Analysis.ipynb`](notebooks/Analysis.ipynb) | Full working analysis notebook with supporting code, intermediate checks, outputs, and visualizations |