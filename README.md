# Sequential vs. Unordered Mining: Discovering Temporal Purchase Progressions in Online Retail

*CSCE 676 — Data Mining · Texas A&M University*  
**Author:** Tejas Singhal (UIN: 836000009)

---

## Overview

This project investigates whether **PrefixSpan sequential pattern mining** surfaces temporal purchase progressions among repeat customers that **FP-Growth basket analysis** is structurally incapable of finding. Using the UCI Online Retail II dataset (805,620 transactions, 5,881 customers, 2009–2011), we show that the two algorithms ask fundamentally different questions from the same data — and find fundamentally different patterns.

**Key finding:** 81% of sequential patterns have no basket analysis counterpart at any tested support threshold. 13 of 23 cross-item progression patterns are sequentially discovered only, with median customer return gaps of 131–206 days.

---

## Final Notebook

| | |
|---|---|
| **View (no install needed)** | [Open in nbviewer](https://nbviewer.org/github/singhaltejas/CSCE676-Data-Mining-Project-TAMU/blob/main/Final/836000009_final.ipynb) |
| **Run locally** | `Final/836000009_final.ipynb` |

---

## Research Question

> Do PrefixSpan sequential patterns reveal temporal buying progressions among repeat customers that are invisible to FP-Growth basket analysis?

**Answer:** Yes. Of the 54 length-2 sequential patterns PrefixSpan finds (minsup=20 customers), **44 (81%) have no corresponding frequent itemset in FP-Growth** at any tested support threshold (1%–5%). Among the 23 cross-item progressions, 13 (57%) are sequentially discovered only — item pairs bought across separate visits months apart that basket analysis cannot mine regardless of threshold.

---

## Setup

**Requirements:** Python 3.8+

```bash
git clone https://github.com/singhaltejas/CSCE676-Data-Mining-Project-TAMU.git
cd CSCE676-Data-Mining-Project-TAMU
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

**Dataset:** Download `online_retail_II.xlsx` from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii) and place it in `Checkpoint_1/`.

Then launch the final notebook:

```bash
jupyter notebook Final/836000009_final.ipynb
```

---

## Repository Structure

| Folder / File | Contents |
|---|---|
| `Final/836000009_final.ipynb` | **Primary deliverable** — complete analysis notebook |
| `Final/*.png` | Figures saved by the notebook |
| `Checkpoint_1/` | Initial EDA, dataset location, baseline cleaning pipeline |
| `Checkpoint_2/` | Research question formation, methodology proof-of-concept |
| `requirements.txt` | Project dependencies |

---

## Techniques Used

| Technique | Type | Library |
|---|---|---|
| FP-Growth + Association Rules | Course standard | `mlxtend` |
| PrefixSpan Sequential Mining | External (beyond course) | `prefixspan` |

---

*CSCE 676 · Texas A&M University*
