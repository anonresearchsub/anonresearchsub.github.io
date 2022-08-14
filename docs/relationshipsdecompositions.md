---
layout: default
title: Relationships and Decompositions
nav_order: 3
has_children: false
permalink: /docs/relationshipsanddecompositions
---

# Relationships and Decompositions
---

#### Relationships between Application Elements

In this work, we consider two *relationship types* between application elements: by-element-name-similarity and by-static relationships. We collected relationships between elements on a file/class level.

#### Relationship Data

Relationship data between elements of each subject applications can be found in [`Relationship-Data.zip`](../assets/data/Relationship-Data.zip).
The `Relationship-Data` directory contains a sub-directory for each subject application, which contains the following directory structure: 

```bash
Relationship-Data
├── App1
│   ├── class-names
│   │   ├── App1ClassNameGraph.csv
│   │   └── App1ClassNameGraphNormalized.csv
│   ├── static
│   |   ├── App1StaticGraph.csv
│   |   └── App1StaticGraphNormalized.csv
│   └── App1CombinedWeightedGraph.csv
├── App2
│   ├── class-names
│   ├── static
│   └── App2CombinedWeightedGraph.csv
...
```

For both the static and name relationships, the `*ClassNameGraph.csv` and `*StaticGraph.csv` files contain the un-normalized weights and the `*GraphNormalized.csv` file contains the normalized weights between elements.
Additionally, the `*CombinedWeightedGraph.csv` file contains the combined relationship graph from the static and class-name normalized graphs.

Each CSV contains 3 columns: application element A, application element B, and the edge weight between elements A and B.


#### Decomposition Results

The by-static, by-name-similarity, union-based, and consensus-based decompositions for each clustering approach can be found in [`Decomposition-Results.zip`](../assets/data/Decomposition-Results.zip).
The `Decomposition-Results` directory contains a sub-directory for subject application.
For each subject application, the directory structure is further split according to clustering approach, namely *Bunch*, *Spectral Clustering* with *k* set to the number of clusters found in the application's ground-truth architecture (i.e. k=Ground-truth), and *Spectral Clustering* with *k* set to the number of clustering produced by *Bunch* for each respective recovery technique (i.e k=Bunch). 

```bash
Decomposition-Results
├── App1
│   ├── Bunch
│   │   ├── App1ClassName.json
│   │   ├── App1Static.json
│   │   ├── App1Union.json
│   │   ├── App1Consensus.json
│   │   ├── App1GroundTruth.json
│   │   └── Consensus_groups.json
│   ├── Spectral (k=Bunch)
│   │   ├── App1ClassName.json
│   │   ├── App1Static.json
│   │   ├── App1Union.json
│   │   ├── App1Consensus.json
│   │   ├── App1GroundTruth.json
│   │   └── Consensus_groups.json
│   └── Spectral (k=Ground-truth)
│       ├── App1ClassName.json
│       ├── App1Static.json
│       ├── App1Union.json
│       ├── App1Consensus.json
│       ├── App1GroundTruth.json
│       └── Consensus_groups.json
├── App2
...
```

The `*ClassName.json`, `*Static.json`, `*Union.json`, `*Consensus.json` files contain the by-name similarity, by-static, union-based and consensus-based decompositions, respectively. 
To produce the by-name similarity and by-static decompositions, the `*ClassNameGraphNormalized` and `*StaticGraphNormalized` were used, respectively. To produce the union-based decomposition, the `*CombinedWeightedGraph` was used.

The `GroundTruth.json` file contains the expected decomposition based on the ground-truth architecture. The `Consensus_groups.json` file contains the consensus groups extracted from the by-name similarity and by-static decompositions, and used by the consensus-based approach.
