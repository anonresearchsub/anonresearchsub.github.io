---
layout: default
title: Subject Applications
nav_order: 2
has_children: false
permalink: /docs/subject Applications
---

# Subject Applications

The table below contains information about the subject applications used in this publication, including the application name, version, source code, and ground-truth architecture. The table contains a link to the source code repository for each application and the version of the code we extracted from these repositories which we used in our analysis in zip format.

| Subject Applications | Version | Language | Link to Repository                                                       | Source Code                               | Ground-truth Architecture                                    |
|----------------------|---------|----------|--------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------|
| Bash                 | 4.2     | C        | [link](https://github.com/bminor/bash/releases/tag/bash-4.2)             | [zip](/assets/data/bash-source.zip)       | [link](https://www.cs.purdue.edu/homes/lintan/ArchRecovery/) |
| Hadoop               | 0.19.0  | Java     | [link](https://hadoop.apache.org)                                        | [zip](/assets/data/hadoop-source.zip)     | [link](https://www.cs.purdue.edu/homes/lintan/ArchRecovery/) |
| ArchStudio           | 4       | Java     | [link](https://github.com/isr-uci-edu/ArchStudio4)                       | [zip](/assets/data/archstudio-source.zip) | [link](https://www.cs.purdue.edu/homes/lintan/ArchRecovery/) |
| Mozilla Firefox      | 1.9.3a4 | C++      | [link](https://ftp.mozilla.org/pub/firefox/releases/devpreview/1.9.3a4/) | [zip](/assets/data/mozilla-source.zip)    | Directory structure                                          |
| XWiki                | 14.1    | Java     | [link](https://github.com/xwiki/xwiki-platform)                          | [zip](/assets/data/xwiki-source.zip)      | Directory structure                                          |
| PartsUnlimited       | -       | Java     | [link](https://github.com/microsoft/PartsUnlimitedMRP)                   |                                           | [link](https://github.com/microsoft/PartsUnlimitedMRPmicro)  |


<!-- - [Hadoop, 0.19.0](https://hadoop.apache.org/) (used in _Measuring the Impact of Code Dependencies on Software Architecture Recovery Techniques_. T. Lutellier, D. Chollak, J. Garcia, L. Tan, D. Rayside, N. Medvidovic, and R. Kroeger. In IEEE Transactions on Software Engineering)
- [ArchStudio, 4](https://github.com/isr-uci-edu/ArchStudio4) (used in _Measuring the Impact of Code Dependencies on Software Architecture Recovery Techniques_. T. Lutellier, D. Chollak, J.    Garcia, L. Tan, D. Rayside, N. Medvidovic, and R. Kroeger. In IEEE Transactions on Software Engineering)
- [Bash, 4.2](https://github.com/bminor/bash/releases/tag/bash-4.2) (used in _Measuring the Impact of Code Dependencies on Software Architecture Recovery Techniques_. T. Lutellier, D. Chollak, J.    Garcia, L. Tan, D. Rayside, N. Medvidovic, and R. Kroeger. In IEEE Transactions on Software Engineering)
- [Mozilla Firefox, 3.7a4](https://ftp.mozilla.org/pub/firefox/releases/devpreview/1.9.3a4/) (used in _A fast clustering algorithm for modularization of large-scale software systems_. N. Teymourian, H. Izadkhah, and A. Isazadeh. In IEEE Transactions on Software Engineering)
- [XWiki, 14.1](https://github.com/xwiki/xwiki-platform) 
- [PartsUnlimitedMRP](https://github.com/microsoft/PartsUnlimitedMRP) -->

#### Relationship Data
The table below contains the static and name-based similarity relationships we extracted in our study. Additionally, we provide the normalized combined relationships for each case study.

| Subject Application     | Static Relationships | Name-based Similarity Relationships | Normalized and Combined Relationships |
|----------------|----------------------|-------------------------------------|---------------------------------------|
| Bash           |                      |                                     |                                       |
| Hadoop         |                      |                                     |                                       |
| ArchStudio     |                      |                                     |                                       |
| MozillaFirefox |                      |                                     |                                       |
| XWiki          |                      |                                     |                                       |
| PartsUnlimited |                      |                                     |                                       |

#### Decompositions
The table below contains the decompositions produced for each clustering approach: *Bunch*, Spectral clustering with k = GT, and Spectral clustering with k = Bunch.

Each decomposition set contains the following files:
* `static-decomposition`: decomposition produced by static relationships
* `name-decomposition`: decomposition produced by name-based relationships
* `union-decomposition`: decomposition produced by the union-based approach
* `consensus-decomposition`: decomposition produced by the consensus-based approach
  

| Case Study     | Bunch    | Spectral clustering k=GT | Spectral clustering k=Bunch | Expected Decomposition |
|----------------|----------|--------------------------|-----------------------------|------------------------|
| Bash           | [link]() | [link]()                 | [link]()                    | [link]()               |
| Hadoop         | [link]() | [link]()                 | [link]()                    | [link]()               |
| ArchStudio     | [link]() | [link]()                 | [link]()                    | [link]()               |
| MozillaFirefox | [link]() | [link]()                 | [link]()                    | [link]()               |
| XWiki          | [link]() | [link]()                 | [link]()                    | [link]()               |
| PartsUnlimited | [link]() | [link]()                 | [link]()                    | [link]()               |

The files are in ... format ...


<!-- For completeness, we also attach the version of the code we extracted from these repositories, which we used in our analysis: 

- Hadoop: [zip](/assets/data/hadoop-source.zip) 
- ArchStudio: [zip](/assets/data/archstudio-source.zip) 
- Bash: [zip](/assets/data/bash-source.zip) 
- Mozilla Firefox: [zip](/assets/data/mozilla-source.zip) 
- XWiki: [zip](/assets/data/xwiki-source.zip) 


The weights of static and name-based similarity relationships we extracted in our study are given below:

- Hadoop: [zip](/assets/data/hadoop-weights.zip) 
- ArchStudio: [zip](/assets/data/archstudio-weights.zip) 
- Bash: [zip](/assets/data/bash-weights.zip) 
- Mozilla Firefox: [zip](/assets/data/mozilla-weights.zip) 
- XWiki: [zip](/assets/data/xwiki-weights.zip)  -->
