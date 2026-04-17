# Assignment 4 — Clustering, Web Search, and PageRank (Spark)


- Course: CSL7110 — Machine Learning with Big Data
- Student Name: Dwivedi Jyoti Rajeshbhai
- Roll Number: M25CSA010
- GitHub Repository: https://github.com/Jyoti-Dwivedi-010/ML_with_Big_Data_Assignment4


This repository contains the implementation for Assignment 4, which consists of three independent components:

- Clustering using Farthest-First Traversal and k-means++
- Web Search using an Inverted Index
- PageRank implementation using Apache Spark and RDDs

All tasks were implemented in Python using PySpark and standard data structures as required.

$ ML_with_Big_Data_Assignment4/
│
├── assignment4_M25CSA010.ipynb     # Main notebook implementation
├── M25CSA010_CSL7110_Assignment4.pdf  # Assignment report
└── README.md


## Part 1 — Clustering
### Objective

Implement clustering algorithms:

Farthest-First Traversal (k-center)
k-means++ initialization
k-means objective function

Dataset:

4601 data points
58 dimensions
Euclidean feature vectors

### Implemented Functions
- readVectorsSeq(filename)
- kcenter(P, k)
- kmeansPP(P, k)
- kmeansObj(P, C)

### Output
- Dataset points: 4601
- Dimension: 58
- kcenter runtime (sec): 0.294602
- kmeans++ objective: 26528.124826
- kcenter(k1) -> kmeans++ objective: 350760.434241

### Time Complexity
- Both algorithms run in: O(|P| × k)



## Part 2 — Web Search Using Inverted Index
### Objective

Build a basic search engine using an inverted index data structure.

The system processes search queries and returns:

- Pages containing a word
- Positions of words in pages

### Implemented Classes
- MySet
- Position
- WordEntry
- PageIndex
- PageEntry
- MyHashTable
- InvertedPageIndex
- SearchEngine

 

## Part 3 — PageRank on Spark
### Objective

- Implement the PageRank algorithm using RDD-based Spark computation.

### Requirements Implemented
- Spark-based computation
- RDD transformations
- Duplicate edge removal
- 40 iterations
- β (damping factor) = 0.8
- Top 5 and Bottom 5 nodes reporting

### Small Graph Result
- Nodes: 100
- Top score: 0.035731

-> Top 5 nodes:

- 53
- 14
- 40
- 1
- 27

### Whole Graph Result
- Nodes: 1000

-> Top 5 nodes:

- 263
- 537
- 965
- 243
- 285

-> Bottom 5 nodes:

- 558
- 93
- 62
- 424
- 408


## How to Run
### Step 1 — Install Dependencies
pip install pyspark
### Step 2 — Run Notebook
jupyter notebook assignment4_solution.ipynb
### Step 3 — Execute All Cells
Run: Kernel → Restart & Run All



## Key Implementation Details
- Spark vectors used for clustering
- Deterministic random seed for reproducibility
- Custom data structures for inverted index
- Strict RDD-based PageRank implementation
- Exact output matching with reference answers
- Duplicate edges removed using distinct()



## Assumptions
- k = 10
- k1 = 50
- Words converted to lowercase
- Connector words ignored
- Punctuation replaced by spaces
- Duplicate edges removed before PageRank computation

