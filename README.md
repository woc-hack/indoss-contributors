# Contributor analysis in enterprise-driven OSS projects

* **[Angeliki Papadopoulou](https://www.balab.aueb.gr/angeliki-papadopolou.html)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, t8180094@aueb.gr
* **[George Liargkovas](https://www.balab.aueb.gr/george-liargkovas.html)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, gliargovas@aueb.gr
* **[Zoe Kotti](https://zkotti.github.io/)**, *[Athens University of Economics and Business](https://www.aueb.gr/en/international), Greece*, zoekotti@aueb.gr

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

The next step would be to find all authors associated with each project. To do this, we use the p2a map, giving the deduplicated projects as input. 
For each project, we want to separate affiliated and non-affiliated to the project's owner organization authors. For this purpose, we use the information regarding authors' emails and extract the email endings, based on the hypothesis that the email of a person working on behalf of an organization would follow the pattern *someone@organization.\**. 

Data cleaning is required on the results of the p2a mapping, in order to determine the dominant domain for each project and calculate the percentage of the domain-affiliated to total authors. The first step of the cleaning is to remove bot accounts, that frequently authorize commits made in GitHub repositories.

Due to time restrictions that prohibit us from cleaning the entire resulting dataset, we proceed by keeping the top 10 dominant domains, based on number of authors that are affiliated with these domains.

### 3. Preliminary Findings
Ratio of enterprise associated authors for top 10 enterprise domains.

| Dominant Domain | Percentage | 
|-----------------|------------|
| microsoft.com  | 20.9%      |
| google.com     | 7.3%       | 
| udacity.com    | 7.2%       |  
| amazon.com     | 6.5%       |  
| pivotal.io     | 4.6%       | 
| redhat.com     | 3.9%       | 
| mozilla.com    | 3.7%       | 
| hashicorp.com  | 2.0%       |  
| fb.com         | 1.2%       | 
| enki.com       | 0.0%       | 


### 4. Challenges
One of the challenges that we faced early on was trying to deduplicate the dataset using the p2P map. We found it difficult to obtain information on whether a project is a forked or cloned one or not. We propose that a more user-friendly output could have solved that issue.

Another challenge emerged while exploring the results of the p2a mapping. During this stage, we realized that a lot of cleaning is required in order to obtain the dominant domain of each project.

### 5. Future Work

In future work, we would like to use the a2A map, in older to filter out commits made by one person using different emails when contributing to a project.

In addition, we aimed to study not only the percentage of non-affiliated to the dominant domain to total authors, but also study their influence in enterprise-driven open source projects. 
To do this, we would use the p2c maps to obtain all commits related to each project and then c2dat maps, in order to get all of the available data related to each commit. 
The next step would be to separate commits made by affiliated and not-affiliated authors and, after calculating the commit percentage, analyze commit frequency and magnitute for each author category. We would calculate these metrics by dividing the initial project dataset into bins, based on the affiliated with the dominant domain to total authors, to investigate the influence of non-affilated authors in enterprise driven projects.

### References
- [A Dataset of Enterprise-Driven Open Source Software](https://arxiv.org/abs/2002.03927), MSR 2020
- [World Of Code: Complete, Curated, Cross-referenced, and Current Collection of Open Source Version Control Data](https://worldofcode.org/)
