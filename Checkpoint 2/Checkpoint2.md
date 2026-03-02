# Project Checkpoint 2: Research Question Formation

**Due:** Thursday by 11:59pm  
**Points:** 50  
**Submission type:** Text entry box

At this stage, you turn curiosity into clear research questions. Building on what you learned from your dataset and EDA, you’ll define questions that use course methods and stretch a bit further with at least one external data mining method. The goal is to ask questions that are interesting, meaningful, and doable, while also planning how you’ll study them.

## Checkpoint 2: RQ Formation

**Goal:** Define research questions that require both course techniques and externally learned techniques.

---

## 1. Project Scope

Brief recap of dataset and EDA findings – example:

- Dataset: Retail transactions  
- Course techniques: Frequent itemsets  
- External techniques: Sequential pattern mining  

---

## 2. Research Question Definition

Propose **3 research questions**.

- At least **2** must use **course techniques**  
- At least **1** must require an **external technique**

Example RQs:

- **RQ1:** What frequent itemsets emerge under varying support thresholds?  
- **RQ2:** How does confidence compare to lift when evaluating association rules?  
- **RQ3:** Do sequential patterns reveal structure missed by unordered itemsets?

For each RQ, specify:

- **Data mining task type** – e.g., Frequent itemset mining / sequential pattern mining  
- **Relevant algorithm(s)** – e.g., Apriori (course), PrefixSpan (external)  
- **Evaluation criteria** – e.g., Support, confidence, lift, interpretability  

Additionally, perform any additional EDA you need in order to find some interesting questions you want to explore.

---

## 3. Motivation and Feasibility

Example points to cover:

- **Motivation:** EDA shows long-tail and temporal clustering  
- **Non-triviality:** Course techniques alone ignore ordering  
- **Feasibility:** External algorithm learnable and implementable  
- **Risks:** Computational cost, parameter sensitivity  

Additionally, perform any additional EDA you need in order to ensure the method is feasible.

---

## 4. Methodological Planning

Example structure:

- **Course algorithms:** Apriori, FP-Growth  
- **External algorithms:** PrefixSpan  
- **Evaluation:** Pattern quality and diversity  
- **Baselines:** High-support-only mining  

Additionally, perform any initial method runs (e.g., testing out how packages work, etc.) you need in order to ensure the methods are feasible.

---

## Deliverables

- **Written RQ section**  
- **RQ-to-method mapping table** (course vs external)  
- **Method and metric plan**  

You must also submit:

- A fully run **Python notebook** meeting the requirements specified here.  
- For every algorithmic decision you make, you must document **why** you made that decision.  
- You will be penalized for **messiness** – make sure your code is professional, well-explained, and well-documented.  
- A **collaboration declaration** for the full notebook is required – this is the same as in the HWs, with one additional item:
  1. Collaborators  
  2. Web Sources  
  3. AI Tools  
  4. Citations for any papers that you used  

---

## Rubric

### [50 pts] Strong/Professional

Correct and complete implementation of the task; reasonable assumptions, stated or implied, and justified; thoughtful handling of real-world data issues (missingness, noise, scale, duplicates, edge cases); clear, concise explanations of what was done and why; code is clean, readable, and well-structured, uses appropriate pandas, and would plausibly pass a professional code review; tests meaningfully validate non-trivial behavior (not just "the code runs so it must be right").

### [25 pts] Partial/Developing

Core task mostly completed but with gaps, weak assumptions, or minor mistakes; reasoning is shallow or mostly descriptive; code works but is messy, repetitive, or fragile; tests are superficial, incomplete, or poorly motivated.

### [0 pts] Minimal/Incorrect

Task is largely incorrect, missing, or misunderstands the goal; little to no reasoning or justification; code does not run or ignores constraints; no meaningful tests.

---

## Navigation / Context

- Course: **CSCE 676 700** – Week 8: (end) Text Mining + Distributed Computing for Data Mining (Mar 2–8)  
- Assignment: **Project Checkpoint 2: Research Question Formation**  
- Related: Homework 5 Corrections (previous module)  

