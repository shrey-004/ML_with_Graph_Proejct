# Author Collaboration Prediction using Graph Neural Networks

**Course:** Machine Learning with Graphs  
**Semester:** Fall 2025  
**Team Members:** Vivek Kumar (22372), Shrey Srivastava (22303), Manjul Chaturvedi (22194), Harsh Shukla (22140)

---

## 2. Introduction & Motivation

Research collaborations drive innovation, and predicting potential collaborations can uncover hidden academic communities and recommend promising coauthors. Since coauthorship forms a natural graph (authors as nodes, collaborations as edges), graph-based machine learning provides a strong framework for **link prediction**.

---

## 3. Problem Statement

We aim to predict **future collaborations** in a coauthorship graph. Given an existing network, the task is to identify pairs of authors most likely to collaborate, even without a current link.

---

## 4. Expected Outcomes

Trained model recommending collaborators, comparison between heuristics, embeddings, and GNNs, network visualizations with predicted links, insights into structural and semantic drivers of collaboration.

---

## 5. Timeline (Work Plan)

| Week | Task | Deliverable |
|------|------|-------------|
| 1 | Literature review & problem formulation | Survey document & plan |
| 2 | Dataset collection & preprocessing | Clean dataset |
| 3 | Graph construction & baseline methods | Baseline results |
| 4 | GNN models (GAE, GAT, etc.) | Initial predictions |
| 5 | Model tuning, evaluation, visualization | Metrics & insights |
| 6 | Final analysis, report, presentation | Final report & slides |

---

## 6. Future Plans

We plan to extend the work to a **heterogeneous graph** of authors and papers, using **Word2Vec embeddings** of paper titles/introductions to recommend both collaborators and relevant papers. Hyperparameter tuning will also allow controlling predictions (e.g., focusing on specific subgraphs or localized neighborhoods).
