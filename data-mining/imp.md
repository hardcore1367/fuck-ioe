# Data Mining (CT72502) — Past Year Question Analysis
**Papers analyzed: 21 sets (2069 Chaitra – 2082 Bhadra)**

---

## Chapter 1: Introduction

**Chapter type:** Theory only
**Syllabus weight:** 2 hrs → 4 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| What is data mining + steps of data mining / KDD process | 15 |
| Data warehouse — definition, features, schemas (star/snowflake), data mart | 9 |
| Data mining vs Data Warehousing — fundamental differences | 3 |

---

## Chapter 2: Data Preprocessing

**Chapter type:** Both (Theory + Numerical)
**Syllabus weight:** 6 hrs → 10 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| OLAP operations (roll-up, roll-down, slice, dice, pivot) + OLAP vs OLTP | 9 |
| Data preprocessing tasks — noise, missing values, cleaning, integration | 8 |
| Curse of dimensionality / dimensionality reduction (PCA, general) | 5 |
| Similarity measures types — Jaccard, cosine, Euclidean, SMC, Minkowski | 4 |
| Data normalization methods — min-max, z-score, decimal scaling | 3 |
| Asymmetric vs symmetric binary data | 2 |
| Nominal and ordinal attributes + handling noisy data | 2 |

### Numerical Types

```
Type 1 — Normalization Calculation
Frequency: 2
Pattern:
  Given: A list of values (e.g., 200, 300, 400, 600, 1000 or frequency histogram data)
  Find: Normalized value using (a) min-max [0,1] (b) z-score (c) decimal scaling
Sub-types:
  1a. Normalize raw dataset (2078 Bhadra, 2079 Chaitra)
  1b. Bin smoothing + normalization (2079 Chaitra also includes bin means depth=3)
```

```
Type 2 — Similarity / Distance Calculation
Frequency: 2
Pattern:
  Given: Table of objects with attributes (binary or numeric)
  Find: Jaccard coefficient (asymmetric), SMC (symmetric), cosine similarity, Euclidean distance
Sub-types:
  2a. Multi-metric on binary attribute table (2080 Baishakh — Ram/Laxmi/Shyam table)
  2b. Cosine + Euclidean on numeric object table (2080 Bhadra — Size/Weight/Color/Taste table)
Note: Both sets ask 4 sub-calculations in 1 question
```

---

## Chapter 3: Classification

**Chapter type:** Both (Theory + Numerical — highest activity chapter)
**Syllabus weight:** 12 hrs → 20 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| Decision tree — ID3 algorithm, information gain, attribute selection (theory) | 8 |
| Naive Bayes classifier — algorithm, prior/posterior probability | 6 |
| KNN (Nearest Neighbor) — algorithm, issues, when to use | 4 |
| Rule-based classifier — working, CN2 algorithm, Accuracy/Laplace measures | 4 |
| ANN / Neural Network classifier — working, general considerations | 4 |
| Overfitting in classification — causes, solutions | 3 |
| Gini index / impurity measures used in decision tree | 3 |
| Bayesian Belief Network (BBN) — use cases, difference from Naive Bayes | 3 |
| Classifier evaluation methods — holdout, k-fold cross-validation, bootstrap | 2 |
| Decision tree vs Rule-based classifier — differences | 2 |

### Numerical Types

```
Type 1 — Decision Tree Construction (ID3 / Information Gain)
Frequency: 4 full numerical sets
Pattern:
  Given: Labeled dataset (categorical attributes + class label)
  Find: Build complete decision tree using ID3 (compute entropy and information gain per attribute)
  Sometimes: Evaluate performance or predict class for a test record
Sub-types:
  1a. Full tree construction (2082 Bhadra, 2079 Bhadra)
  1b. Identify root node only (2081 Bhadra)
  1c. Build tree + predict class for test record (2078 Bhadra)

⚠️ Repeated dataset: Transport Mode (Gender, Car Ownership, Travel Cost, Income Level → Transport Mode),
   10 records — appears in 2081 Bhadra (root node) and 2078 Bhadra (full tree + prediction).

⚠️ Buy Computer dataset (Age, Income, Student, Credit Rating → Buy_Computer), 14 records —
   appears in 2079 Bhadra (ID3) and 2072 Chaitra (Naive Bayes on same table).
```

```
Type 2 — Confusion Matrix Calculations
Frequency: 10
Pattern:
  Given: 2×2 confusion matrix (TP, FP, FN, TN values)
  Find: Accuracy, Sensitivity (TPR), Specificity, Precision, Recall, FPR, Error Rate
  Sometimes: Explain ROC or situations where accuracy is insufficient
Sub-types:
  2a. Standard metrics only — Accuracy, Sensitivity, Specificity, Precision (most common)
  2b. ROC + metrics (2073 Shrawan)
  2c. All 5 metrics including Recall (2072 Chaitra)
  2d. Build confusion matrix from sequence predictions then compute metrics (2070 Chaitra)

⚠️ Matrix (21,6,7,41) appears in 2075 Ashwin Q4 and 2072 Chaitra Q4.
⚠️ Matrix (142,40,98,720) appears in 2078 Bhadra Q6 and 2074 Chaitra Q3.
```

```
Type 3 — Naive Bayes Classification (Numerical Prediction)
Frequency: 3
Pattern:
  Given: Training dataset with class label; test instance X with feature values
  Find: P(class|X) using Naive Bayes; classify X
Sub-types:
  3a. Tabular dataset, predict class label (2079 Bhadra — DefaultedBorrower; 2072 Chaitra — BuyComputer)
  3b. Bayesian Belief Network with given conditional probability tables, compute P(disease|evidence)
      (2081 Baishakh — Heart disease BBN with Exercise/Diet/HeartDisease/ChestPain/BloodPressure)

⚠️ Buy Computer 14-record dataset used for ID3 in 2079 Bhadra and for Naive Bayes in 2072 Chaitra.
```

```
Type 4 — KNN Classification (Numerical)
Frequency: 1
Pattern:
  Given: Labeled training set (sepal/petal measurements), test point, K value
  Find: K nearest neighbors using Euclidean distance; classify test point
Note: 2080 Bhadra — Iris/Flower dataset (7 records), K=3, classify (7, 3.2, 4.7, 1.4)
```

---

## Chapter 4: Association Analysis

**Chapter type:** Both — heavily numerical
**Syllabus weight:** 10 hrs → 18 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| FP-Growth algorithm — explanation, advantages over Apriori, FP-Tree structure | 15 |
| Apriori algorithm — theory, principle, support/confidence, market basket use | 10 |
| Support and confidence — definition, importance in association analysis | 8 |
| Advantages of FP-Growth over Apriori | 6 |
| Sequential patterns — AprioriAll, subsequence generation | 4 |
| Subgraph patterns | 2 |
| Categorical attributes — handling issues in association analysis | 2 |
| Interestingness measures — statistical measures, pattern evaluation | 2 |

### Numerical Types

```
Type 1 — Apriori Algorithm (Frequent Itemset + Association Rules)
Frequency: 10
Pattern:
  Given: Transaction database (TIDs + item sets); min_support (count or %) + min_confidence (%)
  Find: C1→L1→C2→L2→... (candidate and frequent itemsets); association rules meeting confidence
Sub-types:
  1a. Small alphabet items, 4–6 transactions (2082 Bhadra, 2079 Bhadra, 2073 Chaitra, 2070 Chaitra, 2080 Baishakh)
  1b. Named items (MILK/BREAD/BUTTER/EGG), 4 transactions (2081 Bhadra)
  1c. Numbered items M1–M5, 9 transactions (2074 Ashwin)
  1d. Large binary-matrix format (2079 Chaitra — T2–T8 binary matrix)
  1e. Large named items with 7 transactions (2080 Bhadra — T100–T106 with items A,B,C..P)
  1f. Combined with FP-Growth in one question (2076 Ashwin — L-itemset at L=3 + F-List)
```

```
Type 2 — FP-Tree Construction + FP-Growth Mining
Frequency: 5
Pattern:
  Given: Transaction database; support threshold + confidence threshold
  Find: (a) Build FP-Tree step by step for each transaction
        (b) Mine conditional pattern bases and conditional FP-trees → frequent itemsets → association rules
Sub-types:
  2a. Grocery store items (HotDogs, Buns, Ketchup, Coke, Chips), 6 transactions
      2078 Bhadra — support=33.34%, confidence=60%
  2b. Electronic items (Camera, Laptop, Pen drive, Mobile, Earphone), 6 transactions
      2074 Chaitra — FP-Tree construction
  2c. Letter items P,Q,R,S,T, 8 transactions
      2073 Shrawan — support=30%, confidence=75%
  2d. MONKEY/DONKEY-type items (M,O,N,K,E,Y), 5 transactions
      2081 Baishakh — support=60%, confidence=80%; list all strong rules
  2e. Combined with Apriori large dataset (2076 Ashwin)
```

---

## Chapter 5: Cluster Analysis

**Chapter type:** Both — heavily numerical
**Syllabus weight:** 9 hrs → 16 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| K-means algorithm — description, limitations, problems | 8 |
| DBSCAN — algorithm, core/border/noise points, density reachability | 7 |
| Cluster evaluation/validation — measures, issues, SSE | 5 |
| Hierarchical clustering — agglomerative vs divisive, dendrogram | 4 |
| Clustering vs classification — differences | 3 |
| Bisecting K-means | 1 |

### Numerical Types

```
Type 1 — K-means Clustering
Frequency: 10+
Pattern:
  Given: 2D points; K value; sometimes initial centroids specified
  Find: Iteratively assign points to clusters, recompute centroids, show final clusters
  Sometimes: Calculate SSE; list demerits

Sub-types:
  1a. K=2 on 5–7 2D points (most common)
  1b. K=3 on 1D points, calculate SSE (2073 Chaitra — {5,12,18,24,30,42,48})
  1c. K=3 on large 2D matrix, Manhattan distance, 3 iterations (2079 Chaitra)
  1d. K=2 with specified initial centroid (2081 Bhadra, 2081 Baishakh)

⚠️ Dataset {(2,3),(3,3),(6,8),(8,8),(7,5)}, initial centroid (2,3) appears identically in
   2081 Bhadra Q8 and 2081 Baishakh Q8.

⚠️ 6-point dataset (1,2),(2.5,1),(3.5,1.5),(4,1),(3.5,2.5),(5,3) appears in
   2078 Bhadra Q8 and 2074 Ashwin Q7.
```

```
Type 2 — Hierarchical Clustering (Dendrogram)
Frequency: 3
Pattern:
  Given: Either raw 2D points (compute distance) or pre-built distance matrix
  Find: Apply agglomerative hierarchical clustering (single/complete/average linkage); draw dendrogram

Sub-types:
  2a. Distance matrix given directly (p1–p6), draw dendrogram (2080 Bhadra)
  2b. Raw 2D coordinates, complete-linkage, Euclidean distance (2080 Baishakh)
  2c. Theory + dendrogram example (2079 Chaitra)
```

```
Type 3 — DBSCAN Clustering
Frequency: 1 full numerical set
Pattern:
  Given: Set of 2D points; ε (epsilon) and MinPts values
  Find: Identify core, border, and noise points; form clusters

⚠️ Points (2,10),(2,5),(8,4),(5,8),(7,5),(6,4),(1,2),(4,9), ε=2, MinPts=2
   appears in 2082 Bhadra Q5. No other set gives exact numerical DBSCAN — others are algorithm/theory.
```

```
Type 4 — Cluster Validation
Frequency: 2 (implicit in K-means)
Pattern:
  Given: Clustering result
  Find: SSE calculation (2073 Chaitra), or discuss validity measures
```

---

## Chapter 6: Anomaly / Fraud Detection

**Chapter type:** Theory only (algorithm-level)
**Syllabus weight:** 3 hrs → 6 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| Anomaly detection definition + distance-based method | 17 |
| Different approaches — statistical, proximity, density, cluster-based | 6 |
| Types of anomaly (point, contextual, collective) with examples | 3 |
| Issues associated with anomaly detection | 2 |
| Likelihood-based approach for anomaly detection | 1 |
| Base Rate Fallacy | 1 |
| Nearest Neighbor used for anomaly detection | 1 |

> **Note:** Distance-based method is by far the most tested. Expect a 5–8 mark question on it in every exam.

---

## Chapter 7: Advanced Applications

**Chapter type:** Theory only (mostly short notes)
**Syllabus weight:** 3 hrs → 6 marks

### Theory Topics

| Topic | Frequency |
|---|---|
| Time Series Data Mining (short note or brief explanation) | 10 |
| Web Mining — categories, taxonomy, structure, Page Rank | 12 |
| Multimedia Mining | 2 |
| Seasonality in time series | 1 |

> **Note:** This chapter is almost always tested via 2–3 short notes (3–5 marks each). Time Series and Web Mining appear in every few papers. Multimedia is rare.

---

## Chapter Summary

| Chapter | Type | Most Important to Practice | Repeated Datasets |
|---|---|---|---|
| Ch1: Introduction | Theory only | KDD process steps; Data Warehouse vs DM | None |
| Ch2: Preprocessing | Both | OLAP operations; normalization methods (numerical) | Normalization dataset (200,300,400,600,1000) |
| Ch3: Classification | Both | Confusion matrix calculations; ID3 decision tree construction | Transport Mode (ID3): 2081B + 2078B; Confusion matrix (21,6,7,41): 2075 + 2072; (142,40,98,720): 2078 + 2074 |
| Ch4: Association | Both | FP-Tree construction + FP-Growth mining; Apriori algorithm | No exact Apriori dataset repeats; FP-Growth datasets all different |
| Ch5: Clustering | Both | K-means numerical; DBSCAN theory + numerical | K-means {(2,3),(3,3),(6,8),(8,8),(7,5)}: 2081 Bhadra + 2081 Baishakh; 6-point dataset: 2078 Bhadra + 2074 Ashwin |
| Ch6: Anomaly Detection | Theory only | Distance-based method (asked in every set) | None |
| Ch7: Advanced Apps | Theory (short notes) | Time Series + Web Mining (one short note each, every exam) | None |

