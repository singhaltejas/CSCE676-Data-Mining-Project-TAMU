# CSCE 676 - Project Progress Context

## Project Status: Checkpoint 1 Complete
- **Student:** Tejas Singhal (UIN: 836000009)
- **GitHub Repository:** https://github.com/singhaltejas/CSCE676-Data-Mining-Project-TAMU

## Dataset Selection
- **Selected Dataset:** Online Retail II (UCI Repository)
- **Path:** `./online_retail_II.xlsx`
- **Focus:** Transactional data from 2009-2011.

## Technical Strategy
- **Course Topic:** Frequent Itemset Mining & Association Rules (Apriori/FP-Growth).
- **Beyond-Course Technique:** Sequential Pattern Mining (PrefixSpan) to analyze temporal purchase sequences.
- **Environment:** Python 3.14.0 virtual environment (`.venv`) with pandas, seaborn, and openpyxl.

## Key Insights from EDA
- Significant seasonality with peaks in Nov-Dec.
- Most baskets are < 20 items, but a long tail of bulk orders exists.
- Missing Customer IDs (243k rows) were removed to enable sequential tracking.

## Future Checkpoints
- **Checkpoint 2:** Likely focused on implementing the core Frequent Itemset mining and beginning the "Beyond-Course" implementation.