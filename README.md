<a id='top'></a>
<div align="center">
  <a href="https://github.com/okarras/EmpiRE-Analysis">
    <img src="Supplementary%20materials/logo.jpg" alt="Logo" width="250" height="250">
  </a>

<h2 align="center">Divide and Conquer the EmpiRE: A Community-Maintainable <b>K</b>nowledge <b>G</b>raph of <b>Empi</b>rical <b>RE</b>search in Requirements Engineering<br/>
<i>A Sustainable Literature Review for Analyzing the State and Evolution of Empirical Research in Requirements Engineering</i></h2>

  <p align="center">
  <br />
    <a href="https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb">Interactive Analysis</a>
    ·
    <a href="https://github.com/okarras/EmpiRE-Analysis/issues">Bug Report</a>
    ·
    <a href="https://github.com/okarras/EmpiRE-Analysis/issues">Feature Request</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About the Project</a></li>
    <li><a href="#built-with">Built With</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

# About the Project
This project contains the constantly updated [data](SPARQL-Data/), [analysis](empire-analysis.ipynb), and [results](Figures/) of a sustainanle literature review on the state and evolution of empirical research in requirements engineering (RE) using the developed KG-EmpiRE. 

## Background
Empirical research in Requirements Engineering (RE) is a constantly evolving topic. Over the years, several publications examined how empirical research in RE is conducted and how it should be conducted in the future by presenting snapshots of the "current" state of empirical research in RE and, more generally, in Software Engineering (SE). These researchers share the same goal of synthesizing a comprehensive, up-to-date, and long-term available overview of the state and evolution of empirical research in RE and SE. Although they share the same goal, use similar methods, i.a., (systematic) literature reviews, and even examine overlapping periods, venues, and themes, they have not collaborated to build on and update earlier works. **Lack of collaboration among researchers** and **updating literature reviews** are two well-known challenges of literature reviews. Overcoming these challenges is critical to ensure the quality, reliability, and timeliness of research findings from literature reviews.

## Motivation
Recent research addresses the above challenges by focusing on when and how to update (systematic) literature reviews in SE and its subfields. While these works provide social and economic decision support and guidance for updating literature reviews, **the central problem is the unavailability of the extracted and analyzed data**, corresponding to open science in SE. Unavailable data complicates **collaboration among researchers** and **updating literature reviews** as the entire data collection, extraction, and analysis must be repeated and expanded for a comprehensive review. Researchers need support in the form of technical infrastructures and services to conduct sustainable literature reviews so that all data is openly available in the long term according to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable). For this purpose, the data must be organized in a flexible, fine-grained, context-sensitive, and semantic representation to be understandable, processable, and usable by humans and machines. Over the last decade, Knowledge Graphs (KGs) have become an emerging technology in industry and academia as they enable this versatile data representation. Besides well-known KGs for encyclopedic and factual data, such as [DBpedia](https://www.dbpedia.org/) and [WikiData](https://www.wikidata.org), using so-called Research Knowledge Graphs (RKGs) for scientific data is a rather new approach. RKGs include bibliographic metadata, e.g., titles, authors, and venues, as well as scientific data, e.g., research designs, methods, and results. They are a promising technology to sustainably organize scientific data so that the data is openly available for long-term collaborations.

### Method
Our research approach consists of three steps: Data collection, Data extraction, and Data analysis. So far, **we collected 634 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1996 to 2022. **We extracted and organized their scientific data** on the six themes *research paradigm*, *research design*, *research method*, *data collection*, *data analysis* and *bibliographic metadata* using a developed [ORKG template](https://orkg.org/template/R186491). ORKG templates are an implementation of a subset of SHACL and allow specifying the structure of descriptions of papers. In this way, we determined which data to extract and ensured that all the descriptions of papers are consistent and comparable to **build and publish KG-EmpiRE**. In the supplementary materials, we provide a comprehensive overview of [all contents for data extraction](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf) and the [ORKG template](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf).

<p align="center">
    <img src="Supplementary%20materials/approach.png" width="600"/>
    
</p>
<p align="center">
    <em>Research approach for building, publishing, and analyzing KG-EmpiRE.</em>
</p>

With this project, we perform the data analysis of KG-EmpiRE, which has two purposes:

(1) We evaluate the coverage of the curated topic of empirical research in RE by KG-EmpiRE.

(2) We gain insights into the state and evolution of empirical research in RE.

The data analysis is based on competency questions regarding empirical research in SE, including RE, derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) describe their vision of the role of empirical methods in SE, including RE, for the period of 2020 – 2025 by comparing the **"current" state of practice (2007)** with their **target state (2020 - 2025)**. We analyzed these descriptions and derived a total of [77 competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). The number of competency questions answered reflects the **coverage of the curated topic in KG-EmpiRE** (1), and the answers to competency questions provide **insights into the state and evolution of empirical research in RE** (2). For each competency question that can be answered with KG-EmpiRE, we specified a [SPARQL](https://www.w3.org/TR/sparql11-query/) query to retrieve and analyze the data of KG-EmpiRE from the ORKG. We provide all details of the analysis with its [data](SPARQL-Data/), [visualizations](Figures/), and explanations in the [Jupyter Notebook](empire-analysis.ipynb) hosted on [mybinder](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb) for interactive reproduction and (re-)use, always using the most recent data from KG-EmpiRE.

### Results
**Coverage:**

Regarding the coverage of the curated topic by the initial KG-EmpirE, we can state that we are able to answer 16 of the 77 competence questions (21%) using the extracted data. While this number of answered competency questions represents an acceptable coverage of the curated topic, the need to expand the [ORKG template](https://orkg.org/template/R186491) to extract and organize more data required to answer the open competency questions is clearly evident. However, we did not focus on building and publishing an already comprehensive KG of empirical research in RE that can be used to answer as many competency questions as possible. Instead, we aimed to lay its foundation by building, publishing, and evaluating the initial KG-EmpiRE. We focused on conducting a literature review to illustrate how researchers can use RKGs, specifically the ORKG, as a technical infrastructure for organizing scientific data in an openly available and long-term way to build and publish KGs that the research community can constantly maintain, (re-)use, update, and expand.

**State and evolution of empirical research in RE:**

Regarding the state and evolution of empirical research in RE by analyzing the KG-EmpiRE, we can report a positive development towards the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). We found that the proportion of papers with an empirical study increases over time with a average proportion of 94.3% for the **target state (2020 - 2025)**. For data collection, researchers frequently and constantly use the established empricial methods *experiment*, *secondary research*, and *survey* with average proportions of 35.7% (*experiment*), 40% (*secondary research*), and 18.7% (*survey*) for the **target state (2020 -2025)**. We also found that the use of the empirical method *case study*, whose increased use is envisioned, decreases over time with a proportion of 22.3% for the **target state (2020 - 2025)**. Despite the decrease, the emprical method *case study* is actually used more frequently than surveys on average in the **target state (2020 - 2025)**. Furthermore, this decrease represents a positive development of the empirical research in RE, as researchers seem to be more aware of the definition of a case study and therefore use the term more purposefully than in the past. This finding is consistent with the conclusion of [Wohlin](https://doi.org/10.1016/j.infsof.2021.106514) who stated that the term *case study* is often misused in software engineering. Consequently, empirical research that is called as a *case study* in recent years appears to actually be a *case study*. For data analysis, researchers mainly and constantly use *descriptive statistics* with a proportion of 87.6% overall and 92% for the **target state (2020 - 2025)**. In contrast, the use of *inferential statistics* with a proportion of 19.2% overall and 26.3% for the **target state (2020 - 2025)** is small. Regarding the general use of empirical methods, we found that the number of empirical methods used for data collection and data analysis in a single papers increases over time, with *three to four empirical methods* most frequently used in one paper. For the **target state (2020 - 2025)**, researchers mainly use *three to even five empirical methods* in a single paper with average proportions of 22% (*three empirical methods used*), 25.3% (*four empirical methods used*), and 26.7% (*five empirical methods used*). This increase in the number of empirical methods used shows a shift as envisioned towards the use of several empirical methods and thus the collection and analysis of data from different perspectives to synthesize evidence. In addition to the empirical methods used, we also found a positive development with regard to the reporting of important information of experimental design. For the **target state (2020 - 2025)**, the proportion of papers reporting *threats to validity*, providing *raw data and supplementary materials*, and highlighting their *research questions and answers* steadily increase over time with average proportions of 91.3% (*threats to validity*), 71.3% (*raw data and supplementary materials*), and 23.7% (*highlighted research questions and answer*) respectively 53% (*highlighted research question and answer hidden in the running text*). 

Despite the positive developments towards the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), we also identified the need for future improvements of empirical research in RE. While [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) envisioned an increased use of *action research, we found that the proportion of *action research* is small over the entire timeframe analyzed (2000 - 2022) with an average proportion of only 2%. For the **target state (2020 - 2025)**, no paper reported the use of *action research*. According to [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), more *case studies* and *action research* are needed to ensure the industrial relevance of empirical research. This part of the vision is not yet nearly achieved. Regarding the reporting of threats to validity, we found two issues for future improvement. First, a proportion of 33.6% of the analyzed papers reporting threats to validity *only mentioned threats to validity* without any further classification of the types of validity. Although the general reporting of threats to validity is useful, the lack of classification of the reported threats to validity makes it difficult for a reader to have a clear overview of whether the threats to validity have been discussed comprehensively. In the future, researchers need to communicate their threats to validity comprehensively and transparently by discussing all type of validity equally and naming the type of validity addressed. Second, the proportion of papers reporting threats to *conclusion validity* with 18.2% is small compared to the other mainly discussed types of valdity (*external validity*: 60.4%, *internal validity*: 56.1%, and *construct validity*: 47.9%). Therefore, researchers need to make more effort to comprehensively discuss the validity of their empirical research by also addressing the conclusion valditiy similar to the other types of validity. Regarding data analysis, the proportion of paper using *inferential statistics* is small with a proportion of only 26.2% for the **target state (2020 - 2025)**. For a mature use of statistical methods as envisioned by [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), researchers have to deal more with *inferential statistics* and include them in the data analysis of their empirical research.

## Interactive Jupyter Notebook
Binder link to the interactive, reproducible, and reusable analysis:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb)

## Zenodo Release
Zenodo link of the latest release:
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8083529.svg)](https://doi.org/10.5281/zenodo.8083529)

