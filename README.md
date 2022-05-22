# Contributor analysis in enterprise-driven OSS projects

* **[Angeliki Papadopoulou](https://www.balab.aueb.gr/angeliki-papadopolou.html)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, t8180094@aueb.gr
* **[George Liargkovas](https://www.balab.aueb.gr/george-liargkovas.html)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, gliargovas@aueb.gr
* **[Zoe Kotti](https://zkotti.github.io/)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, zoekotti@aueb.gr

**Abstract:** 

**Link:** 

***

### 1. Introduction
The purpose of this project is to analyze the influence of non-enterprise-affiliated contributors
to enterprise-driven OSS projects.
Particularly we aim to investigate the following project characteristics from contributors' perspective.

- commit frequency
- contribution size (LOC, files)
- activity distribution

### 2. Methodology
To obtain enterprise-driven repositories, we used a [dataset](https://dl.acm.org/doi/epdf/10.1145/3379597.3387495) by Spinellis *et al.* The dataset contains information about 17,264 GitHub repositories that are created by organizations and are maintained mainly by enterprise-affiliated contributors. 

We begin the analysis by using the WoC p2P map, to deduplicate repositories. We do so because we want to study repositories that are created by a valid organization from the beginning, as forked and cloned projects would include the initial repository's commits.

### 3. Preliminary Findings


### 4. Challenges
One of the challenges that we faced early on was trying to deduplicate the dataset using the p2P map. We found it difficult to obtain information on whether a project is a forked or cloned one or not. We propose that a more user-friendly output could have solved that issue.

### 5. Future Work


### References
- [A Dataset of Enterprise-Driven Open Source Software](https://arxiv.org/abs/2002.03927), MSR 2020
- [World Of Code: Complete, Curated, Cross-referenced, and Current Collection of Open Source Version Control Data](https://worldofcode.org/)
