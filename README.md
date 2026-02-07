# Online Retail Analysis: Frequent Itemset & Sequential Pattern Mining
*A CSCE 676 (Data Mining) Project at Texas A&M University*

**Author:** Tejas Singhal (UIN: 836000009)

## Overview
This repository contains a comprehensive data mining project focused on the **Online Retail II** dataset. The goal is to identify hidden customer purchasing patterns through association rules and temporal sequences, enabling better inventory management and targeted marketing strategies.

Key metrics and techniques include:
*   **Word-Level Metrics (for Rules):** Support, Confidence, Lift.
*   **Temporal Patterns:** Sequential Pattern Mining to track customer acquisition over time.

## Key Features
*   **Market Basket Analysis:** Utilizing Apriori and FP-Growth to find co-purchased items.
*   **Sequential Pattern Mining:** Implementing PrefixSpan to analyze temporal order of purchases.
*   **Data Cleaning Pipeline:** Automated handling of missing customer IDs and transaction cancellations.
*   **Interactive Visualizations:** Deep dives into seasonality and basket distributions.

## Installation
To set up the project locally, clone the repository and install the dependencies in a virtual environment:

```bash
git clone https://github.com/singhaltejas/CSCE676-Data-Mining-Project-TAMU.git
cd CSCE676-Data-Mining-Project-TAMU
python3 -m venv .venv
source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
pip install -r requirements.txt
```
*(Note: If requirements.txt is missing, install: pandas matplotlib seaborn openpyxl scipy mlxtend)*

## Quick Start
To view the analysis and results for Checkpoint 1:
1. Ensure the dataset `online_retail_II.xlsx` is in the root directory.
2. Launch Jupyter Notebook or Lab:
   ```bash
   jupyter notebook Checkpoint_1/Project_Checkpoint_1.ipynb
   ```

## Example Insights
### Monthly Transaction Volume
![Monthly Trends](Checkpoint_1/Monthly%20Transaction%20Trends%20(2009%20-%202011).png)
*Example plot showing the significant seasonality with peaks in November and December.*

## Repository Structure
*   `Checkpoint_1/`: Directory containing the primary notebook, exploratory plots, and data copies.
*   More coming as semester progresses

## Contributing
Contributions and feedback are welcome!
1. **Fork** the repository.
2. **Create a Feature Branch** (`git checkout -b feature/NewAnalysis`).
3. **Commit Your Changes** (`git commit -m 'Add new analysis'`).
4. **Push to the Branch** (`git push origin feature/NewAnalysis`).
5. **Open a Pull Request**.

---
*This project is part of the CSCE 676 course at Texas A&M University.*
