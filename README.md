# Sequential vs. Unordered Mining: Discovering Temporal Purchase Progressions in Online Retail

*CSCE 676 — Data Mining · Texas A&M University*
**Author:** Tejas Singhal (UIN: 836000009)

---

## Project Video

🎥 **[Watch the 2-minute project video here](https://youtu.be/wYY3szkY9h4)**

---

## Start Here

👉 **Main deliverable:** [`main_notebook.ipynb`](main_notebook.ipynb)

This is the curated, story-driven notebook that walks through all analysis end-to-end. Start here.

---

## Overview

This project investigates whether **PrefixSpan sequential pattern mining** surfaces temporal purchase progressions among repeat customers that **FP-Growth basket analysis** is structurally incapable of finding. Using the UCI Online Retail II dataset (805,620 transactions, 5,881 customers, 2009–2011), we show that the two algorithms ask fundamentally different questions from the same data — and find fundamentally different patterns. This analysis is relevant to any e-commerce platform that wants to understand not just *what* customers buy together, but *in what order* they return to buy over time.

---

## Research Questions

1. **RQ1:** What are the most frequent single-category and multi-category purchase patterns (baskets) in the Online Retail II dataset, as identified by FP-Growth?
2. **RQ2:** What sequential buying progressions (across multiple store visits) exist among repeat customers, as identified by PrefixSpan?
3. **RQ3:** Do PrefixSpan sequential patterns reveal temporal buying progressions among repeat customers that are invisible to FP-Growth basket analysis?

**Answer to RQ3:** Yes. Of the 54 length-2 sequential patterns PrefixSpan finds (minsup=20 customers), **44 (81%) have no corresponding frequent itemset in FP-Growth** at any tested support threshold (1%–5%). Among the 23 cross-item progressions, 13 (57%) are sequentially discovered only — item pairs bought across separate visits months apart that basket analysis cannot mine regardless of threshold.

---

## Key Results

- **81%** of PrefixSpan sequential patterns have no basket analysis counterpart at any tested support threshold
- **13 of 23** cross-item progression patterns are sequentially discovered only
- Median customer return gap for top sequential progressions: **131–206 days**
- FP-Growth finds dense within-invoice co-purchase clusters; PrefixSpan finds long-horizon return behaviors — the algorithms are complementary, not redundant

---

## Data

**Dataset:** [Online Retail II — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

- **Source:** UCI ML Repository (Dataset #502)
- **Size:** 805,620 transactions, 5,881 unique customers, 2009–2011
- **Format:** Excel (`.xlsx`), two sheets (Year 2009-2010, Year 2010-2011)
- **Download:** The dataset is too large to commit to git. Download `online_retail_II.xlsx` from the UCI link above and place it in `Checkpoint_1/`.

**Preprocessing steps:**
1. Drop rows with null `CustomerID` or `Description`
2. Filter out cancelled invoices (Invoice starting with `C`)
3. Filter to positive `Quantity` and `Price`
4. Encode `StockCode` as string for consistent joining

The full cleaning pipeline is inline at the top of Section 1 in `main_notebook.ipynb`.

---

## How to Reproduce

This project was built and run in **Google Colab**. The recommended way to run it:

1. Open [`main_notebook.ipynb`](main_notebook.ipynb) in Google Colab (File → Upload notebook)
2. Upload `online_retail_II.xlsx` to Colab session storage (or mount Google Drive)
3. Run all cells in order (Runtime → Run all)

**Local reproduction (alternative):**

```bash
git clone https://github.com/singhaltejas/CSCE676-Data-Mining-Project-TAMU.git
cd CSCE676-Data-Mining-Project-TAMU
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook main_notebook.ipynb
```

Place `online_retail_II.xlsx` in `Checkpoint_1/` before running.

---

## Key Dependencies

| Package | Version | Purpose |
|---|---|---|
| Python | 3.10.12 | Runtime (Google Colab) |
| `pandas` | 2.2.2 | Data loading, cleaning, grouping |
| `matplotlib` | 3.8.3 | Figures and plots |
| `seaborn` | 0.13.2 | Heatmaps |
| `mlxtend` | 0.23.1 | FP-Growth + association rules |
| `prefixspan` | 0.5.2 | Sequential pattern mining |
| `scipy` | 1.13.0 | Statistical utilities |
| `openpyxl` | 3.1.2 | Reading `.xlsx` files |

Full dependency list: [`requirements.txt`](requirements.txt)

---

## Repository Structure

```
CSCE676-Data-Mining-Project-TAMU/
├── main_notebook.ipynb          ← START HERE: final curated analysis
├── requirements.txt             ← pip-pinned dependencies
├── README.md
├── .gitignore
│
├── checkpoints/
│   ├── checkpoint_1.ipynb       ← Checkpoint 1: EDA + baseline cleaning
│   └── checkpoint_2.ipynb       ← Checkpoint 2: methodology proof-of-concept
│
├── assets/                      ← figures generated by main_notebook.ipynb
│   ├── visit_frequency_distribution.png
│   ├── fpgrowth_threshold_sensitivity.png
│   ├── fpgrowth_confidence_vs_lift.png
│   ├── prefixspan_top_patterns.png
│   ├── prefixspan_pattern_lengths.png
│   └── section6_heatmap_comparison.png
│
├── Final/                       ← original final notebook + figures
│   └── 836000009_final.ipynb
│
├── Checkpoint_1/                ← original checkpoint 1 materials
│   └── 836000009_checkpoint_1.ipynb
│
└── Checkpoint_2/                ← original checkpoint 2 materials
    └── 836000009_checkpoint_2.ipynb
```

---

## Techniques Used

| Technique | Type | Library |
|---|---|---|
| FP-Growth + Association Rules | Course standard | `mlxtend` |
| PrefixSpan Sequential Mining | External (beyond course) | `prefixspan` |

---

*CSCE 676 · Texas A&M University*
