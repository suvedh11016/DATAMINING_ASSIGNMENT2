# 📘 Citation Network Analysis and PageRank Variants

This project analyzes a citation network of research papers and explores different link analysis algorithms — including **Normal PageRank**, **Topic-Sensitive PageRank**, and **Personalized PageRank** — along with similarity metrics such as **Co-citation** and **Bibliographic Coupling**.

---

## 🧩 Project Overview

The goal of this project is to model the citation relationships between academic papers and extract insights using graph-based algorithms. The network is represented as a **directed graph** where:
- Each **node** represents a research paper.
- Each **directed edge (A → B)** indicates that paper A cites paper B.

---

## 📂 Exercises

### **Exercise 1: Graph Construction and Analysis**
- Built a directed citation graph using the dataset.
- Computed:
  - Total vertices and edges
  - Weakly Connected Components (WCC)
  - Strongly Connected Components (SCC)
  - Statistics for the largest WCC and SCC

Example results:

| Metric | Count |
|:------------------------------|:------:|
| Vertices | 49,572 |
| Edges | 163,309 |
| Weakly Connected Components | 6,985 |
| Strongly Connected Components | 47,731 |
| Nodes in Largest WCC | 41,225 |
| Edges in Largest WCC | 161,635 |
| Nodes in Largest SCC | 171 |
| Edges in Largest SCC | 1,190 |

---

### **Exercise 2: Paper Similarity Analysis**
Calculated **Co-citation** and **Bibliographic Coupling** scores.

**Formulas:**
- Co-citation: CoCite(A, B) = | { P | P cites both A and B } |
- Bibliographic Coupling: BiblioCouple(A, B) = | { P | A and B both cite P } |


Top-10 similar paper pairs were listed for each measure.

---

### **Exercise 3: PageRank Computation**
Implemented the **Normal PageRank algorithm** with damping factor `d = 0.85`.  
Displayed the **top-10 most influential papers** based on PageRank scores.

---

### **Exercise 4: Topic-Sensitive PageRank**
Implemented **Topic-Sensitive PageRank** for five topics:
- `security`
- `hashing`
- `streaming`
- `timeseries`
- `search`

For each topic, computed the topic-specific PageRank vector and listed the top-10 papers based on:
- PageRank score
- Number of citations

---

## 📊 Algorithms Explained

| Algorithm | Mathematical Idea | Usage |
|:-----------|:------------------|:------|
| **Normal PageRank** | Random surfer model; rank proportional to incoming link quality and quantity. | Generic importance ranking (Google Search). |
| **Topic-Sensitive PageRank** | PageRank biased toward topic-specific teleportation sets. | Improves search results for topic-specific queries. |
| **Personalized PageRank** | Custom teleportation vector based on user profile or interests. | Recommendation systems, user-personalized ranking. |

---

## ⚙️ Technical Stack
- **Language:** Python 3  
- **Libraries:** `networkx`, `numpy`, `pandas`, `matplotlib`
- **Dataset:** Citation graph (papers and references)
- **Outputs:** Graph statistics, PageRank tables, similarity scores

---

## 🚀 How to Run

```bash
# Clone this repository
git clone https://github.com/suvedh11016/DATAMINING_ASSIGNMENT2.git

# Run the code
pip install jupyter
jupyter notebook 1.ipynb
