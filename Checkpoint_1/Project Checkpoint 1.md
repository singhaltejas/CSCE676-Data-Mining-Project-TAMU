# Project Checkpoint 1: Dataset Comparison, Selection, and EDA

**Course:** CSCE 676  
**Assignment Type:** Project Checkpoint 1  
**Points:** 50  
**Due:** Thursday by 11:59pm  
**Submission Type:** Text entry box  

This first checkpoint gets your project off the ground by helping you choose a dataset you’re genuinely interested in and setting a strong foundation for the rest of the semester. You’ll explore three possible datasets, compare their strengths and limitations, and then select one that supports both course techniques and at least one new data mining method you’re excited to learn. Through exploratory data analysis, you’ll start uncovering patterns, challenges, and questions that shape the direction of your project.

**Goal:** Select a dataset that meaningfully supports one or more data mining techniques covered in this course **AND** at least one additional technique not covered in the course. Perform exploratory data analysis (data basics, data collection, data cleaning, bias).

---

## (A) Identification of Candidate Datasets

**Identify three candidate datasets.** Each dataset should:

- Align with at least one course topic (e.g., frequent itemsets, graphs, clustering, text, anomaly detection)
- Provide opportunities for at least one beyond-course technique

**Example candidate datasets + techniques:**

**Retail transaction logs**  
- Course: Frequent Itemsets, Association Rules  
- Beyond course: Bonferroni-corrected correlations, Chi-squared analyses, ANOVA analyses  

**Social network graph**  
- Course: Graph Mining, PageRank, Community Detection  
- Beyond course: Graph neural networks  

**Product reviews or tweets**  
- Course: Text Mining, embeddings  
- Beyond course: Topic modeling, transformer-based embeddings  

**Sensor or network logs**  
- Course: Anomaly Detection, Streams  
- Beyond course: Autoencoder-based anomalies  

**For each dataset, provide:**
- Dataset name and source – e.g., Online Retail Dataset  
- Course topic alignment – e.g., Frequent itemsets and association rule mining  
- Potential beyond-course techniques – e.g., Sequential pattern mining not covered in lecture  
- Dataset size and structure – e.g., 500K transactions, variable-length item baskets  
- Data types – e.g., Transaction IDs, item IDs, timestamps  
- Target variable(s), if any – e.g., None (unsupervised pattern mining), Engagement, Price  
- Licensing or usage constraints – e.g., CC License  

**Possible conferences for datasets and beyond-course techniques:**

- KDD: [https://kdd2025.kdd.org/datasets-and-benchmarks-track-papers-2/](https://kdd2025.kdd.org/datasets-and-benchmarks-track-papers-2/)  
- WSDM: [https://www.wsdm-conference.org/2025/accepted-papers/](https://www.wsdm-conference.org/2025/accepted-papers/)  
- RecSys: [https://recsys.acm.org/recsys25/accepted-contributions/](https://recsys.acm.org/recsys25/accepted-contributions/)  
- ACL: [https://2025.aclweb.org/program/main_papers/](https://2025.aclweb.org/program/main_papers/)  
- EMNLP: [https://2025.emnlp.org/program/main_papers/](https://2025.emnlp.org/program/main_papers/)  
- ICWSM: [https://www.icwsm.org/2025/schedule/allpapers.html](https://www.icwsm.org/2025/schedule/allpapers.html)  

**To work with conference papers:**

1. Copy-paste the paper title that you’re interested in into Google Scholar to find the PDF.  
2. See if the paper has a code link/dataset link. (You are *not* recommended to re-implement algorithms from the papers by hand – you want to find a paper that has existing code.)  
3. You may have to try multiple (many) papers to find a dataset that is downloadable/workable, and code that is runnable. This is expected, and part of the process.

---

## (B) Comparative Analysis of Datasets

Compare the three datasets with respect to both data properties **and** course vs external techniques.

These are the required comparison dimensions that you should write up in a **table** in your report:

**Supported data mining tasks** – e.g.:  
- Retail data: Frequent itemsets (course), sequential patterns (external)  
- Graph data: Centrality (course), node embeddings (external)  
- Review data: Text mining (course), topic modeling (external)  

**Data quality issues** – e.g.:  
- Missing transactions  
- Noisy text  
- Graph sparsity or disconnected components  

**Algorithmic feasibility** – e.g.:  
- Can Apriori work on a dataset of this size?  
- Is sequential pattern mining computationally feasible?  
- Is graph size manageable without Spark?  

**Bias considerations** – e.g.:  
- Recommendation bias in retail data  
- Sampling bias in social media text  

**Ethical considerations** – e.g.:  
- Will pursuing this analysis harm anyone?  
- What are the social power dynamics involved in this dataset (e.g., employer vs. employee dynamic)?

---

## (C) Dataset Selection

**Select one dataset and justify the choice.** Example:

**Selected dataset:** Retail transaction logs  

**Reasons:**
- Directly supports frequent itemsets and association rules (course)  
- Supports sequential pattern mining not covered in class (external)  
- Allows meaningful comparison between unordered and temporal patterns  

**Trade-offs:**
- No natural text component  
- Limited supervised learning opportunities  

---

## (D) Exploratory Data Analysis (Selected Dataset Only)

Perform EDA on the selected dataset. Example analyses:

- Distribution of basket sizes  
- Frequency of top items  
- Sparsity of item co-occurrence  
- Temporal gaps between transactions  
- Initial observations motivating external techniques  

---

## (E) Initial Insights and Direction

**Example observation:**  
Most items appear in fewer than 1% of transactions.

**Example hypothesis:**  
High support thresholds miss meaningful temporal patterns.

**Example potential research questions (RQs):**
- How do different support thresholds affect rule quality?  
- Do sequential patterns reveal structure missed by frequent itemsets?  

---

## (F) GitHub Portfolio Building

- You are expected to post your project code on your professional GitHub as the course progresses; this is to help you build a portfolio, so you will have work that you have done to talk about when you are interviewing for jobs.  
- Include a link to your **public GitHub repository** for the project, with your first notebook posted.  
- You are encouraged to create an initial README describing the project; as an example, see:  
  - [https://github.com/mariateleki/zscore](https://github.com/mariateleki/zscore)

---

## Deliverables

- A fully run Python notebook meeting the requirements specified in this assignment.  
- For every algorithmic decision you make, you must document **why** you made that decision.  
- You will be penalized for messiness – make sure your code is professional, well-explained, and well-documented.  
- A **collaboration declaration** for the full notebook is required – this is the same as in the HWs, with one additional item:  
  1. Collaborators  
  2. Web Sources  
  3. AI Tools  
  4. Citations for any papers that you used  

---

## Rubric

**[50 pts] Strong/Professional:**  
Correct and complete implementation of the task; reasonable assumptions, stated or implied, and justified; thoughtful handling of real-world data issues (missingness, noise, scale, duplicates, edge cases); clear, concise explanations of what was done and why; code is clean, readable, and well-structured, uses appropriate pandas, and would plausibly pass a professional code review; tests meaningfully validate non-trivial behavior (not just "the code runs so it must be right").

**[25 pts] Partial/Developing:**  
Core task mostly completed but with gaps, weak assumptions, or minor mistakes; reasoning is shallow or mostly descriptive; code works but is messy, repetitive, or fragile; tests are superficial, incomplete, or poorly motivated.

**[0 pts] Minimal/Incorrect:**  
Task is largely incorrect, missing, or misunderstands the goal; little to no reasoning or justification; code does not run or ignores constraints; no meaningful tests.
