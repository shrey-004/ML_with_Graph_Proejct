
---

# 📘 Project Proposal

**Course:** Machine Learning with Graphs
**Semester:** [Fall 2025]
**Student Name(s):**

* Shrey Srivastava (22303)
* Vivek Kumar (22372)
* Manjul Chaturvedi (22194)
* Harsh Shukla (22140)

---

## 1. Project Title

**Author Collaboration Prediction using Graph Neural Networks**

---

## 2. Introduction & Motivation

Research collaboration plays a crucial role in advancing science, enabling the exchange of knowledge, interdisciplinary studies, and innovative problem-solving. Predicting potential collaborations between authors can uncover hidden academic communities, facilitate new partnerships, and recommend future coauthors to researchers.

Coauthorship networks are naturally modeled as graphs, where authors represent nodes and collaborations represent edges. This makes **graph-based machine learning** methods particularly suitable for addressing the problem of collaboration prediction.

---

## 3. Problem Statement

We aim to **predict future or potential collaborations between authors** by modeling the coauthorship network as a graph and applying **link prediction methods**. Given an existing coauthor graph, the task is to infer which pairs of authors are most likely to collaborate but do not currently share an edge.

**Scope:**

* Focus on predicting collaborations at the author level.
* Both homogeneous (authors only) and heterogeneous (authors, papers, venues) graphs may be explored.
* Out of scope: predicting paper acceptance, citation counts, or venue-level impact.

**Challenges:**

* Data sparsity in emerging authors.
* High computational complexity with large coauthorship networks.
* Incorporating textual/semantic features effectively.

---

## 4. Objectives

* Construct a coauthorship network using bibliographic datasets (DBLP, arXiv).
* Implement baseline heuristics for link prediction (e.g., Common Neighbors, Jaccard Index, Preferential Attachment).
* Apply node embedding methods such as **Node2Vec**.
* Develop and evaluate advanced graph models: **Graph Autoencoders (GAE/VGAE)**, **GraphSAGE**, **GAT**, and **LightGCN**.
* Explore knowledge graph embeddings (TransE, DistMult) for heterogeneous graphs.
* Evaluate using metrics such as **AUC, Average Precision, and Recall@K**.
* Provide meaningful insights and visualizations of predicted collaboration links.

---

## 5. Literature Review (Background Work)

* Liben-Nowell & Kleinberg (2007): Proposed link prediction methods using network proximity measures.
* Grover & Leskovec (2016): Introduced **Node2Vec**, an embedding method for graph representation.
* Kipf & Welling (2016): Proposed **Graph Autoencoders (GAE/VGAE)** for unsupervised link prediction.
* Hamilton et al. (2017): Developed **GraphSAGE**, an inductive framework for large-scale graph learning.

**Gap:** While traditional heuristics and embeddings capture structural information, they may not fully exploit semantic or higher-order dependencies. Our project builds upon these by integrating **GNN-based methods** with structural + semantic features for author collaboration prediction.

---

## 6. Methodology

* **Dataset:**

  * Source: DBLP and arXiv metadata (authors, papers, venues).
  * Nodes: Authors (optional: papers, venues, topics).
  * Edges: Coauthorship links.
  * Features: Publication count, aggregated text embeddings of titles/abstracts, venue information.

* **Graph Construction:**

  * Homogeneous graph: Authors as nodes, coauthorship as edges.
  * Heterogeneous graph: Authors, papers, and venues as nodes with typed edges.

* **Baselines:**

  * Common Neighbors, Jaccard Similarity, Preferential Attachment.
  * Node embedding (Node2Vec).

* **Proposed Models:**

  * Graph Autoencoders (GAE/VGAE).
  * GraphSAGE, GAT, LightGCN.
  * Knowledge graph embeddings (TransE, DistMult).

* **Training Objective:**

  * Link prediction via binary classification.
  * Positive samples: existing coauthor edges.
  * Negative samples: randomly chosen non-edges.

* **Evaluation Metrics:**

  * AUC, Average Precision, Recall@K.

* **Tools/Libraries:**

  * PyTorch Geometric, DGL, NetworkX, Scikit-learn.
  * HuggingFace/SentenceTransformers (for textual features).

*(A flowchart of the pipeline—data → graph construction → baseline → GNN models → evaluation—can be added here for clarity.)*

---

## 7. Expected Outcomes

* A trained model that can **recommend potential collaborators** for any given author.
* Quantitative comparison between heuristic, embedding, and GNN-based methods.
* Visualizations of coauthor networks with predicted collaboration links.
* Insights into structural and semantic factors influencing academic collaborations.

---

## 8. Timeline (Work Plan)

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

## 9. Challenges & Risks

* **Large-scale data:** DBLP and arXiv networks may contain millions of nodes and edges.

  * *Mitigation:* Use sampling techniques or focus on specific subfields.
* **Cold-start problem:** New authors with limited data may be difficult to predict.

  * *Mitigation:* Incorporate textual features from papers.
* **Model complexity:** Training advanced GNNs may be resource-intensive.

  * *Mitigation:* Optimize using GPU acceleration and efficient libraries.

---

## 10. References

1. Liben-Nowell, D., & Kleinberg, J. (2007). The link-prediction problem for social networks. *Journal of the American Society for Information Science and Technology*.
2. Grover, A., & Leskovec, J. (2016). Node2Vec: Scalable Feature Learning for Networks. *KDD*.
3. Kipf, T. N., & Welling, M. (2016). Variational Graph Auto-Encoders. *arXiv:1611.07308*.
4. Hamilton, W., Ying, Z., & Leskovec, J. (2017). Inductive Representation Learning on Large Graphs. *NeurIPS*.

---

