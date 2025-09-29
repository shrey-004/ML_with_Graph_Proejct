
---

# 📘 Project Proposal

**Course:** Machine Learning with Graphs
**Semester:** [Fall 2025]
**Student Name(s):**

* Vivek Kumar (22372)
* Shrey Srivastava (22303)
* Manjul Chaturvedi (22194)
* Harsh Shukla (22140)

---

## 1. Project Title

**Author Collaboration Prediction using Graph Neural Networks**

---

## 2. Introduction & Motivation

Research collaborations are central to scientific progress, fostering knowledge exchange and innovation. Predicting potential collaborations can reveal hidden academic communities and recommend promising coauthors.

Since coauthorship naturally forms a graph structure—authors as nodes and collaborations as edges—**graph-based machine learning** offers a powerful framework to address this problem through link prediction.

---

## 3. Problem Statement

We aim to predict **future or potential collaborations** between authors using a coauthorship graph. Given an existing network, the task is to identify pairs of authors most likely to collaborate, even if they currently lack a direct link.

---

## 4. Expected Outcomes

* A trained model recommending potential collaborators for authors.
* Quantitative comparison between heuristic, embedding, and GNN methods.
* Visualizations of networks and predicted collaboration links.
* Insights into structural and semantic factors driving collaborations.

---

## 5. Timeline (Work Plan)

| Week | Task                                       | Deliverable            |
| ---- | ------------------------------------------ | ---------------------- |
| 1–2  | Literature review                          | Short survey document  |
| 3–4  | Dataset collection + preprocessing         | Clean coauthor dataset |
| 5–7  | Implement baselines (heuristics, Node2Vec) | Baseline results       |
| 8–9  | Implement GNN models (GAE, GraphSAGE, GAT) | Initial predictions    |
| 10   | Experiments + model tuning                 | Performance comparison |
| 11   | Final analysis, visualization, insights    | Draft report           |
| 12   | Presentation & submission                  | Final report + slides  |

---

## 6. Future Plans

We plan to extend the network into a **heterogeneous graph** of authors and papers, where papers include **Word2Vec embeddings** of their titles and introductions. This will allow the model to suggest not only new collaborators but also **relevant papers for an author’s research interests**.

Further, **hyperparameters** will enable controlling link predictions—such as focusing on **specific subgraphs** (e.g., by region or field) or restricting predictions to localized neighborhoods for more fine-grained recommendations.

---

## 7. References

1. Liben-Nowell, D., & Kleinberg, J. (2007). The link-prediction problem for social networks. *JASIST*.
2. Grover, A., & Leskovec, J. (2016). Node2Vec: Scalable Feature Learning for Networks. *KDD*.
3. Kipf, T. N., & Welling, M. (2016). Variational Graph Auto-Encoders. *arXiv:1611.07308*.
4. Hamilton, W., Ying, Z., & Leskovec, J. (2017). Inductive Representation Learning on Large Graphs. *NeurIPS*.

---


