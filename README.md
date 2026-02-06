# CSCE 676: Data Mining - Online Retail Transaction Analysis

**Submitted by:** Tejas Singhal  
**UIN:** 836000009

This repository contains the project work for CSCE 676 (Data Mining). The project focuses on analyzing customer purchasing patterns using a large-scale retail dataset to uncover association rules and temporal purchasing sequences.

## Project Overview
The goal of this project is to apply data mining techniques to identify how products are co-purchased and to predict future purchasing behavior based on historical sequences.

### Dataset
*   **Name:** Online Retail II Dataset
*   **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
*   **Size:** ~1 million transactions (2009-2011)
*   **Key Features:** Invoice ID, Stock Code, Description, Quantity, Invoice Date, Unit Price, Customer ID, and Country.

## Current Progress: Checkpoint 1
In the first phase of this project, I performed:
1.  **Dataset Comparison:** Evaluated three candidate datasets (Retail, Amazon Reviews, and Twitch Social Networks) based on algorithmic feasibility, data quality, and ethical considerations.
2.  **Dataset Selection:** Selected the Online Retail II dataset due to its high compatibility with course topics like Frequent Itemset Mining.
3.  **Exploratory Data Analysis (EDA):**
    *   Cleaned the data by handling missing Customer IDs and removing transaction cancellations.
    *   Analyzed basket size distributions to inform future support thresholds.
    *   Identified seasonal peaks in transactions (Nov-Dec), justifying a deeper look into holiday-specific purchasing rules.

## Data Mining Techniques
*   **Course Techniques:** Frequent Itemset Mining, Association Rules (Apriori/FP-Growth).
*   **Beyond-Course Techniques:** Sequential Pattern Mining (PrefixSpan) to analyze the temporal order of customer acquisitions.

## Repository Structure
*   `Project_Checkpoint_1.ipynb`: Full Python notebook containing data cleaning, visualizations, and selection justification.
*   `GEMINI.md`: Contextual documentation for the project environment.

## Requirements
To run the notebook, you will need:
*   Python 3.10+
*   `pandas`
*   `matplotlib`
*   `seaborn`
*   `openpyxl` (for loading the original Excel dataset)

---
*This project is part of the CSCE 676 course at Texas A&M University.*
