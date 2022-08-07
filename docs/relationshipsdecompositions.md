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

In this publication, we consider two *relationship types* between application elements: by element name similarity and by static relationships. We collected relationships between elements on a file/class level.
 * Element name similarity: 
 * Static: 


#### Relationship Data

Relationship data between elements of each subject applications can be found in `Relationship-Data.zip` [here](../assets/data/Relationship-Data.zip).
The `Relationship-Data` directory contains a sub-directory for each subject application, which contains the following directory structure: 

```bash
Relationship-Data
├── ExampleApplication
│   ├── class-names
│   │   ├── ExampleApplicationClassNameGraph.csv
│   │   └── ExampleApplicationClassNameGraphNormalized.csv
│   ├── static
│   |   ├── ExampleApplicationStaticGraph.csv
│   |   └── ExampleApplicationStaticGraphNormalized.csv
│   └── ExampleApplicationCombinedWeightedGraph.csv
├── ...
```

For both the static and class-name relationships, there is a `*Graph.csv` file with un-normalized weights and a `*GraphNormalized.csv` file with normalized weights between elements.
Additionally, the `*CombinedWeightedGraph.csv` file contains the combined relationship graph from the static and class-name normalized graphs.

Each CSV contains 3 columns: application element A, application element B, and the edge weight between elements A and B.


#### Decomposition Results

The by-static, by-name-similarity, union-based, and consensus-based decompositions for each clustering approach can be found in `Decomposition-Results.zip` [here](../assets/data/Decomposition-Results.zip).
The `Decomposition-Results` directory contains a sub-directory for each clustering approach, namely *Bunch*, *Spectral Clustering* with $k$ set to the number of clusters found in the application's ground-truth architecture (i.e. k=Ground-truth), and *Spectral Clustering* with $k$ set to the number of clustering produced by *Bunch* for each respective recovery technique (i.e k=Bunch).  The directory structure is further split by subject application, like below.

```bash
Decomposition-Results
├── Bunch
│   ├── ExampleApplication
│   │   ├── ExampleApplicationClassName.json
│   │   ├── ExampleApplicationStatic.json
│   │   ├── ExampleApplicationUnion.json
│   │   ├── ExampleApplicationConsensus.json
│   │   ├── ExampleApplicationGroundTruth.json
│   │   └── Consensus_groups.json
│   ├── ...
├── Spectral (k=Bunch)
│   ├── ...
└── Spectral (k=Ground-truth)
    ├── ...
```

The `*ClassName.json`, `*Static.json`, `*Union.json`, `*Consensus.json` files contain the by-name similarity, by-static, union-based and consensus-based decompositions, respectively. 
To produce the by-name similarity and by-static decompositions, the `*ClassNameGraphNormalized` and `*StaticGraphNormalized` were used, respectively. To produce the union-based decomposition, the `*CombinedWeightedGraph` was used. The consensus-based decomposition

The `*GroundTruth.json` file contains the expected decomposition based on the ground-truth architecture. The `Consensus_groups.json` file contains the consensus groups extracted from the by-name similarity and by-static decompositions, and used by the consensus-based approach.
