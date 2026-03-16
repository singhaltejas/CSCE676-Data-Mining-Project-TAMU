# Online Retail Analysis: Frequent Itemset & Sequential Pattern Mining
*A CSCE 676 (Data Mining) Project at Texas A&M University*

**Author:** Tejas Singhal (UIN: 836000009)

## Project Overview
This repository contains a comprehensive data mining project focused on the **Online Retail II** dataset. The goal is to identify hidden customer purchasing patterns through association rules and temporal sequences, enabling better inventory management and targeted marketing strategies.

### Current Progress: Checkpoint 2 Complete
I have defined the core research questions and verified the feasibility of the proposed methodologies, including both course-standard and external data mining techniques.

## Key Research Questions
*   **RQ1 (Course):** Do frequent itemsets and association rules differ meaningfully between the holiday peak season (Nov–Dec) and the rest of the year?
*   **RQ2 (Course):** Given the extreme long-tail item distribution, does ranking rules by lift surface more actionable cross-sell opportunities than confidence?
*   **RQ3 (External):** Among repeat customers, do sequential patterns (PrefixSpan) reveal temporal buying progressions invisible to unordered itemset mining?

## Key Features & Insights
*   **Market Basket Analysis:** Utilizing **FP-Growth** and **Apriori** to find co-purchased items.
*   **Sequential Pattern Mining:** Implementing **PrefixSpan** to analyze the temporal order of purchases over multiple customer visits.
*   **Data Cleaning Pipeline:** Automated handling of missing customer IDs and transaction cancellations. I confirmed through actual data execution that **72.35%** of the unique customers (4,255 out of 5,881) are repeat purchasers, making sequential mining highly feasible.
*   **Interactive Visualizations:** Deep dives into seasonality (peaks in Nov-Dec) and basket size distributions.

## Installation & Setup
To set up the project locally, clone the repository and install the dependencies in a virtual environment:

```bash
git clone https://github.com/singhaltejas/CSCE676-Data-Mining-Project-TAMU.git
cd CSCE676-Data-Mining-Project-TAMU
python3 -m venv .venv
source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
pip install -r requirements.txt
```

## Repository Structure
*   **Checkpoint_1/**: Initial EDA, dataset selection, and baseline cleaning pipeline.
*   **Checkpoint_2/**: Research question formation, dataset-specific EDA, methodological planning, and real-data proof-of-concept runs.
*   **requirements.txt**: Central project dependencies.
*   **README.md**: Central project documentation (this file).

## Quick Start
To view the analysis for the latest checkpoint:
1. Ensure the dataset `online_retail_II.xlsx` is located in the `Checkpoint_1/` directory.
2. Launch Jupyter:
   ```bash
   jupyter notebook "Checkpoint_2/836000009_checkpoint_2.ipynb"
   ```

---
*This project is part of the CSCE 676 course at Texas A&M University.*
