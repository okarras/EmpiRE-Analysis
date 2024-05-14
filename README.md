<a id='top'></a>
<div align="center">
  <a href="https://github.com/okarras/EmpiRE-Analysis">
    <img src="Supplementary%20materials/logo.jpg" alt="Logo" width="250" height="250">
  </a>

<h2 align="center" style="font-weight: normal">Divide and Conquer the EmpiRE: A Community-Maintainable <b>K</b>nowledge <b>G</b>raph of <b>Empi</b>rical Research in <b>R</b>equirements <b>E</b>ngineering<br/>
<i>A Sustainable Literature Review for Analyzing the State and Evolution of Empirical Research in Requirements Engineering</i></h2><br/>

[![GitHub - Project](https://img.shields.io/badge/GitHub-Project-2ea44f)](https://github.com/okarras/EmpiRE-Analysis) [![Issues - Bug Report](https://img.shields.io/badge/Issues-Bug_Report-2ea44f)](https://github.com/okarras/EmpiRE-Analysis/issues)  [![Issues - Feature Request](https://img.shields.io/badge/Issues-Feature_Request-2ea44f)](https://github.com/okarras/EmpiRE-Analysis/issues) [![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8083529.svg)](https://doi.org/10.5281/zenodo.8083529) [![ORKG - KG-EmpiRE](https://img.shields.io/badge/ORKG-KG--EmpiRE-e86161)](https://orkg.org/observatory/Empirical_Software_Engineering?sort=combined&classesFilter=Paper,Comparison,Visualization)
[![ORKG - RDF dump](https://img.shields.io/badge/ORKG-RDF_dump-e86161)](https://orkg.org/api/rdf/dump)
</div>

> [!IMPORTANT]  
> The content of this repository was reviewed on the [Artifact Evaluation track](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts) of the [32nd IEEE International Requirements Engineering Conference 2024](https://conf.researchr.org/home/RE-2024) and awarded the [![Badge - Reusable](https://custom-icon-badges.demolab.com/badge/Badge-Reusable-8250DF?logo=award&logoSource=feather)](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts#Submission-Instructions).
> 

# Table of Contents
<details>
  <summary>Contents</summary>
  <ol>
    <li><a href="#about-the-project">About the Project</a></li>
    <li><a href="#folder-structure-and-files">Folder Structure and Files</a></li>
    <li><a href="#system-requirements">System Requirements</a></li>
    <li><a href="#installation-instructions">Installation Instructions</a></li>
    <li><a href="#executable-machines-and-environments">Executable Machines and Environments</a></li>
    <li><a href="#usage-instructions">Usage Instructions</a></li>
    <li><a href="#related-publication">Related Publication</a></li>
    <li><a href="#executive-summary">Executive Summary</a></li>
    <li><a href="#corresponding-author">Corresponding Author</a></li>
    <li><a href="#how-to-cite">How to Cite</a></li>
  </ol>
</details>

# About the Project
This project contains the constantly updated [data](SPARQL-Data/), [analysis](empire-analysis.ipynb), and [results](Figures/) of a sustainable literature review on the state and evolution of empirical research in requirements engineering (RE) using the developed KG-EmpiRE. 

KG-EmpiRE is a community-maintainable knowledge graph (KG) of empirical research in requirements engineering based on scientific data extracted from *currently* **680 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1994 to 2022. We are *currently* organizing scientific data in KG-EmpiRE using a defined [template](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf) for the six [themes](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf) *research paradigm*, *research design*, *research method*, *data collection*, *data analysis* and *bibliographic metadata* with the long-term plan to expand the themes.

KG-EmpiRE itself is maintained in the [Open Research Knowledge Graph (ORKG)](https://orkg.org). The ORKG is a cross-domain and cross-topic research knowledge graph (RKG) with corresponding technical infrastructure and services for the organization of Findable, Accessible, Interoperable, and Reusable (FAIR) scientific data from papers in accordance with the [FAIR data principles](https://doi.org/10.1038/sdata.2016.18). The [TIB - Leibniz Information Centre for Science and Technology](https://www.tib.eu/en/research-development/open-research-knowledge-graph) develops and maintains the ORKG permanently and has committed itself to the long-term archiving of all data. As a central access point to all curated papers in KG-EmpiRE, we established a more general [ORKG observatory](https://orkg.org/observatory/Empirical_Software_Engineering) on empirical research in software engineering. In addition, the ORKG provides a [RDF dump](https://orkg.org/api/rdf/dump) of all its data, including the most recent data from KG-EmpiRE. We also store the [data](SPARQL-Data/) used for analysis as CSV files, which can be distinguished by date.

> [!NOTE]  
> The CSV files with the date "*2023-06-26*" enable the replication of the results of the <a href="#related-publication">related publication</a>. The details on the replication of the results can be found in the <a href="#usage-instructions">usage instructions</a>.

In this project, we perform the data analysis of KG-EmpiRE, which has two purposes:

1. We evaluate the coverage of the curated topic of empirical research in RE by KG-EmpiRE.

2. We gain insights into the state and evolution of empirical research in RE.

The data analysis is based on competency questions regarding empirical research in SE, including RE, derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). They describe their vision of the role of empirical methods in SE, including RE, for the period of 2020 – 2025 by comparing the **"current" state of practice (2007)** with their **target state (2020 - 2025)**. We analyzed these descriptions and derived a total of [77 competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). The number of competency questions answered reflects the **coverage of the curated topic in KG-EmpiRE** (1), and the answers to competency questions provide **insights into the state and evolution of empirical research in RE** (2). For each competency question that can be answered with KG-EmpiRE (*currently* 16 of 77), we specified [SPARQL](https://www.w3.org/TR/sparql11-query/) queries to retrieve and analyze the data of KG-EmpiRE from the ORKG. We provide all details of the analysis with its SPARQL queries, [data](SPARQL-Data/), [visualizations](Figures/), and explanations in the [Jupyter Notebook](empire-analysis.ipynb) hosted on [binder](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb) for interactive replication and (re-)use, always using the most recent data from KG-EmpiRE.

The [analysis](empire-analysis.ipynb) of the individual competency questions always follows the same structure:

1. *Data Selection*: Explaining the competency question and the required data for the analysis.
2. *Data Collection*: Executing the specified SPARQL query to retrieve the data.
3. *Data Exploration*: Exploring the data, including its cleaning and validation, to prepare the data for data analysis.
4. *Data Analysis*: Analyzing the data and creating visualizations.
5. *Data Interpretation*: Interpreting the data and derive insights.

Overall, this project serves to make the [data](SPARQL-Data/), [analysis](empire-analysis.ipynb), and [results](Figures/) openly available in the long term according to the [FAIR data principles](https://doi.org/10.1038/sdata.2016.18) to enable a replicable, (re-)usable and thus sustainable literature review.

In this way, this project can be used for:

1. Replication of the results from the <a href="#related-publication">related publication</a>.

2. (Re-)use of KG-EmpiRE with its most recent data.

3. Repetition of our research approach for sustainable literature reviews on other topics.

<p align="right">(<a href="#top">back to top</a>)</p>

# Folder Structure and Files
In the following, we first show a graphical overview of the folder structure and files of the project before we describe them in more detail.

## Graphical Overview
```
EmpiRE-Analysis/
┣━ .vscode/
┃   ┗━ settings.json
┣━ Figures/
┃   ┣━ CQ1/...contains 2 visualizations
┃   ┣━ CQ2/...contains 8 visualizations
┃   ┣━ CQ3/...contains 2 visualizations
┃   ┣━ CQ4/...contains 4 visualizations
┃   ┣━ CQ5/...contains 2 visualizations
┃   ┣━ CQ6/...contains 3 visualizations
┃   ┣━ CQ7/...contains 6 visualizations
┃   ┣━ CQ8/...contains 2 visualizations
┃   ┣━ CQ9/...contains 2 visualizations
┃   ┣━ CQ10/...contains 2 visualizations
┃   ┣━ CQ11/...contains 2 visualizations
┃   ┣━ CQ12/...contains 4 visualizations
┃   ┣━ CQ13/...contains 2 visualizations
┃   ┣━ CQ14/...contains 2 visualizations
┃   ┣━ CQ15/...contains 2 visualizations
┃   ┗━ CQ16/...contains 2 visualizations
┣━ SPARQL-Data/...contains two sets of 22 CSV files from the SPARQL queries (most recent and the release).
┣━ Supplementary materials/
┃   ┣━ approach.png
┃   ┣━ Detailed list of all 77 competency questions.xlsx
┃   ┣━ Detailed ORKG template structure.pdf
┃   ┣━ logo.jpg
┃   ┗━ Overview of all content for data extraction.pdf
┣━ CITATION.cff
┣━ empire-analysis.ipynb
┣━ LICENSE
┣━ README.md
┣━ requirements.txt
┗━ runtime.txt
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Description of the Folders and Files 
| **Directory** | **Description** |
|---------------|-----------------|
| [.vscode/](.vscode/)[settings.json](.vscode/settings.json)| Storage location of the workspace settings file for [Visual Studio Code](https://code.visualstudio.com/).|
| [Figures/](Figures/)|Storage location of all visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) organized in individual subfolders per competence question.|
| [Figures/CQ1](Figures/CQ1/)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 1.|
| [Figures/CQ2](Figures/CQ2/)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 2.|
| [Figures/CQ3](Figures/CQ3/)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 3.|
| [Figures/CQ4](Figures/CQ4/)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 4.|
| [Figures/CQ5](Figures/CQ5)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 5.|
| [Figures/CQ6](Figures/CQ6)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 6.|
| [Figures/CQ7](Figures/CQ7)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 7.|
| [Figures/CQ8](Figures/CQ8)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 8.|
| [Figures/CQ9](Figures/CQ9)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 9.|
| [Figures/CQ10](Figures/CQ10)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 10.|
| [Figures/CQ11](Figures/CQ11)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 11.|
| [Figures/CQ12](Figures/CQ12)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 12.|
| [Figures/CQ13](Figures/CQ13)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 13.|
| [Figures/CQ14](Figures/CQ14)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 14.|
| [Figures/CQ15](Figures/CQ15)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 15.|
| [Figures/CQ16](Figures/CQ16)| Storage location of the visualizations as PNG files generated by the [analysis](empire-analysis.ipynb) for competency question 16.|
| [SPARQL-Data/](SPARQL-Data/)| Storage location of the data  retrieved by the corresponding SPARQL queries of the competency questions. The folder contains two sets of 22 CSV files of the data retrieved with the SPARQL queries, differentiated by date: the most recent and the release date for replication("*2023-06-26*").|
| [Supplementary materials/](Supplementary%20materials/)| Storage location of the supplementary materials of the [analysis](empire-analysis.ipynb) and the <a href="#related-publication">related publication</a>.|
| [Supplementary materials/approach.png](Supplementary%20materials/approach.png)| Visualization of the research approach for building, publishing, and analyzing KG-EmpiRE.|
| [Supplementary materials/Detailed list of all 77 competency questions.xlsx](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx)| The detailed list of all 77 competency questions derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) of regarding the role of empirical methods in all fields of SE, including RE.|
| [Supplementary materials/Detailed ORKG template structure.pdf](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf)| The detailed overview of the developed ORKG template for structuring the scientific data extracted from the *currently* **680 papers**|.
| [Supplementary materials/logo.jpg](Supplementary%20materials/logo.jpg)| Logo of the project.|
| [Supplementary materials/Overview of all content for data extraction.pdf](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf)| The detailed overview of all content identified for data extraction.|
| [CITATION.cff](CITATION.cff)| The file contains human- and machine-readable citation information for software and datasets. Further information can be found on the [Citation File Format (CFF) website](https://citation-file-format.github.io/).|
| [empire-analysis.ipynb](empire-analysis.ipynb)| Jupyter Notebook that contains the entire data analysis of KG-EmpiRE for answering the 16 competency questions.|
| [LICENSE](LICENSE)| License of the project|
| [README.md](README.md)| README file of the project.|
|[requirements.txt](requirements.txt)| A list of packages or libraries needed to work on the project that can all be installed with the file.|
|[runtime.txt](runtime.txt)| Specification of the Python runtime to declare the exact version number to use.|

<p align="right">(<a href="#top">back to top</a>)</p>

# System Requirements
The following system requirements must be met to run this project:

<div align="center">

[![OS - Windows](https://img.shields.io/badge/OS-Windows-blue?logo=windows&logoColor=white)](https://www.microsoft.com/)
[![Anaconda3 - 23.7.4](https://img.shields.io/badge/Anaconda3-conda_23.7.4-blue)](https://www.anaconda.com/)
[![Made with Python](https://img.shields.io/badge/Python->=3.11-blue?logo=python&logoColor=white)](https://python.org)
[![pip - 23.2.1](https://img.shields.io/badge/pip->=23.2.1-blue)](https://pypi.org/project/pip/)

</div>

> [!NOTE]  
> We have only tested the analysis on systems with the Windows operating system, which is why we specify Windows as a necessary system requirement.

All required packages and libraries are installed automatically when running:

    pip install -r requirements.txt

We use [Visual Studio Code](https://code.visualstudio.com/) for developing and can recommend the following [YouTube Tutorial](https://www.youtube.com/watch?v=h1sAzPojKMg) for setting up [Jupyter Notebooks](https://jupyter.org/) in [Visual Studio Code](https://code.visualstudio.com/). 

<p align="right">(<a href="#top">back to top</a>)</p>

# Installation Instructions
In the following, we explain how to install the project for execution on a local machine using a terminal, assuming that the system requirements are met.

## 1. Clone the repository.
```sh
git clone https://github.com/okarras/EmpiRE-Analysis
```

## 2. Navigate to the main directory of the project.
```sh
cd EmpiRE-Analysis
```

## 3. Create a virtual environment with Anaconda.
```sh
conda create --name empire_venv
```

## 4. Activate the virtual environment.
```sh
conda activate empire_venv
```

## 5. Install the required packages and libraries.
```sh
pip install -r requirements.txt
```

## 6. Start the Jupyter Notebook.
```sh
jupyter notebook empire-analysis.ipynb
```

<p align="right">(<a href="#top">back to top</a>)</p>

# Executable Machines and Environments

## Binder (Recommended)
We use [binder](https://mybinder.org/) to provide an executable machine and environment where the project is hosted for interactive replication and (re-)use. 

> [!IMPORTANT]  
> If you follow the link below, the project will start on [binder](https://mybinder.org/) to run it in a [JupyterLab](https://jupyter.org/). If a built image already exists, the start should take about 1 - 2 minutes. If a built image needs to be created, the start can take about 5 minutes.

<div align="center">

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb)

</div>

Once the project has been started in [JupyterLab](https://jupyter.org/), carry out the following steps:

1. Restart the kernel and clear all outputs.
2. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

## GitHub Codespaces
If you have a GitHub account, you can use [GitHub Codespaces](https://github.com/features/codespaces) to execute the project. 

<div align="center">

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/okarras/EmpiRE-Analysis?quickstart=1)

</div>

> [!IMPORTANT]  
> You can use [GitHub Codespaces](https://github.com/features/codespaces) to start the project either in Visual Studio Code or JupyterLab, depending on your preferences.

Once the project has been started, carry out the following steps:

1. Open a terminal and install the required packages and libraries.
    ```sh
    pip install -r requirements.txt
    ```
2. Open the analysis script: [empire-analysis.ipynb](empire-analysis.ipynb).
3. Restart the kernel and clear all outputs.
4. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

# Usage Instructions
In the following, we explain the steps for using the project for the two cases of replication of results from the <a href="#related-publication">related publication</a> and (re-)use of KG-EmpiRE with its most recent data, assuming that the project is executed either <a href="#installation-instructions">locally</a> or on one of the <a href="#executable-machines-and-environments">executable machines and environments</a>. 

## Replication of the results from the related publication

1. In the section "*2. Reusable Functions for Data Analysis*" of the [Jupyter Notebook](empire-analysis.ipynb), change the **DATE** variable from "*now*" to "*2023-06-26*" to use the corresponding CSV files with the data of the <a href="#related-publication">related publication</a>.

    ```python
    #DATE = now.strftime('%Y-%m-%d')
    #For replication of the related publication use the following date.
    DATE = '2023-06-26'
    ```
2. Restart the kernel and clear all outputs.
3. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

## (Re-)use of KG-EmpiRE with its most recent data

1. In section "*2. Reusable Functions for Data Analysis*" of the [Jupyter Notebook](empire-analysis.ipynb), ensure that the **DATE** variable is set to "*now*".

    ```python
    DATE = now.strftime('%Y-%m-%d')
    #For replication of the related publication use the following date.
    #DATE = '2023-06-26'
    ```
2. Restart the kernel and clear all outputs.
3. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

# Related Publication
The first version of KG-EmpiRE based on **570 papers** from the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 2000 to 2022 and the first analysis of the sustainable literature review on the state and evolution of empirical research in RE have been published in:

>Oliver Karras, Felix Wernlein, Jil Klünder, and Sören Auer:<br/>
>[__Divide and Conquer the EmpiRE: A Community-Maintainable Knowledge Graph of Empirical Research in Requirements Engineering__](https://doi.org/10.1109/ESEM56168.2023.10304795),
>In: 2023 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM), New Orleans, LA, USA, 2023, pp. 1-12.<br/>
>
>The paper received the [__Best Paper Award__](https://www.oliver-karras.de/wp-content/uploads/2023/10/acm_ieee_esem2023_certificate_best_paper_award.pdf) of the 17th ACM/IEEE International Symposium on Empirical Software Engineering and Measurement 2023.

<p align="right">(<a href="#top">back to top</a>)</p>

# Executive Summary
<details>
<summary>TL;DR</summary>

## Background
Empirical research in RE is a constantly evolving topic. Over the years, several publications examined how empirical research in RE is conducted and how it should be conducted in the future by presenting snapshots of the "current" state of empirical research in RE and, more generally, in Software Engineering (SE). These publications share the same goal of synthesizing a comprehensive, up-to-date, and long-term available overview of the state and evolution of empirical research in RE and SE. Although they share the same goal, use similar methods, i.e., (systematic) literature reviews, and even examine overlapping periods, venues, and themes, they have not collaborated to build on and update earlier works. **Lack of collaboration among researchers** and **updating literature reviews** are two well-known challenges of literature reviews. Overcoming these challenges is crucial to ensure the quality, reliability, and timeliness of research findings from literature reviews and thus enable sustainable literature reviews.

## Motivation
Recent research addresses the above challenges by focusing on when and how to update (systematic) literature reviews in SE and its subfields. While these works provide social and economic decision support and guidance for updating literature reviews, **the central problem is the unavailability of the extracted and analyzed data**, corresponding to open science in SE. Unavailable data complicates **collaboration among researchers** and **updating literature reviews** as the entire data collection, data extraction, and data analysis must be repeated and expanded for a comprehensive review. Researchers need support in the form of technical infrastructures and services to conduct sustainable literature reviews so that all data is openly available in the long term according to the FAIR data principles. For this purpose, the data must be organized in a flexible, fine-grained, context-sensitive, and semantic representation to be understandable, processable, and usable by humans and machines. Over the last decade, Knowledge Graphs (KGs) have become an emerging technology in industry and academia as they enable this versatile data representation. Besides, well-known KGs for encyclopedic and factual data, such as [DBpedia](https://www.dbpedia.org/) and [WikiData](https://www.wikidata.org), using so-called Research Knowledge Graphs (RKGs) for scientific data is a rather new approach. RKGs include bibliographic metadata, e.g., titles, authors, and venues, as well as scientific data, e.g., research designs, methods, and results. They are a promising technology to sustainably organize scientific data so that the data is openly available for long-term collaborations.

## Objective
**Our long-term objective is to constantly maintain a KG-EmpiRE with the research community to synthesize a comprehensive, up-to-date, and long-term available overview of the state and evolution of empirical research in RE**. For this purpose, we use the [ORKG](https://orkg.org/) with its technical infrastructure and services to build and publish KG-EmpiRE that the research community can constantly maintain, (re-)use, update, and expand by *dividing* the efforts to *conquer* the EmpiRE. With this work, we lay the foundation for such a comprehensive, up-to-date, and long-term available overview of the state and evolution of empirical research in RE by building, publishing, and analyzing KG-EmpiRE.

## Method
Our research approach consists of three steps: Data collection, Data extraction, and Data analysis. So far, **we collected 680 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1994 to 2022. **We extracted and organized their scientific data** on the six themes *research paradigm*, *research design*, *research method*, *data collection*, *data analysis* and *bibliographic metadata* using a developed [ORKG template](https://orkg.org/template/R186491). ORKG templates are an implementation of a subset of SHACL and allow specifying the structure of descriptions of papers. In this way, we determined which data to extract and ensured that all the descriptions of papers were consistent and comparable to **build and publish KG-EmpiRE**. In the supplementary materials, we provide a comprehensive overview of [all contents for data extraction](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf) and the [ORKG template](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf).

<p align="center">
    <img src="Supplementary%20materials/approach.png" width="600"/>
    
</p>
<p align="center">
    <em>Research approach for building, publishing, and analyzing KG-EmpiRE.</em>
</p>

With this project, we perform the data analysis of KG-EmpiRE, which has two purposes:

(1) We evaluate the coverage of the curated topic of empirical research in RE by KG-EmpiRE.

(2) We gain insights into the state and evolution of empirical research in RE.

The data analysis is based on competency questions regarding empirical research in SE, including RE, derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). They describe their vision of the role of empirical methods in SE, including RE, for the period of 2020 – 2025 by comparing the **"current" state of practice (2007)** with their **target state (2020 - 2025)**. We analyzed these descriptions and derived a total of [77 competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). The number of competency questions answered reflects the **coverage of the curated topic in KG-EmpiRE** (1), and the answers to competency questions provide **insights into the state and evolution of empirical research in RE** (2). For each competency question that can be answered with KG-EmpiRE, we specified [SPARQL](https://www.w3.org/TR/sparql11-query/) queries to retrieve and analyze the data of KG-EmpiRE from the ORKG. We provide all details of the analysis with its SPARQL queries, [data](SPARQL-Data/), [visualizations](Figures/), and explanations in the [Jupyter Notebook](empire-analysis.ipynb) hosted on [binder](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb) for interactive replication and (re-)use, always using the most recent data from KG-EmpiRE.

## Results
**Coverage:**

Regarding the coverage of the curated topic of empirical research in RE by KG-EmpiRE, we can state that we can answer 16 of the 77 competence questions (21%) using the extracted data. While this number of answered competency questions represents an acceptable coverage of the curated topic, the need to expand the [ORKG template](https://orkg.org/template/R186491) to extract and organize more data required to answer the open competency questions is clearly evident. Our work lays the foundation for a sustainable literature review on the state and evolution of empirical research in RE by building, publishing, and analyzing KG-EmpiRE, which can be constantly and collaboratively updated. In this way, we demonstrate how researchers can use the ORKG with its technical infrastructure and services for organizing scientific data in an openly available and long-term way to build and publish KGs that the research community can constantly maintain, (re-)use, update, and expand.

**State and evolution of empirical research in RE:**

> **NOTE**  
> The following insights are *currently* only based on the results of the first analysis of KG-EmpiRE with the data from **570 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 2000 to 2020. However, the analysis always uses the most recent data from KG-EmpiRE so that the visualizations already contain the newly added data from the **110 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1994 to 1999.

Regarding the state and evolution of empirical research in RE by analyzing KG-EmpiRE, we can report a positive development towards the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). We found that the proportion of papers with an empirical study increases over time with an average proportion of 94.3% for the **target state (2020 - 2025)**. For data collection, researchers frequently and constantly use the established empirical methods *experiment*, *secondary research*, and *survey* with average proportions of 35.7% (*experiment*), 40% (*secondary research*), and 18.7% (*survey*) for the **target state (2020 -2025)**. We also found that the use of the empirical method *case study*, whose increased use is envisioned, decreases over time with a proportion of 22.3% for the **target state (2020 - 2025)**. Despite the decrease, the empirical method *case study* is used more frequently than surveys on average in the **target state (2020 - 2025)**. Furthermore, this decrease represents a positive development of the empirical research in RE, as researchers seem to be more aware of the definition of a case study and, therefore, use the term more purposefully than in the past. This finding is consistent with the conclusion of [Wohlin](https://doi.org/10.1016/j.infsof.2021.106514) who stated that the term *case study* is often misused in software engineering. Consequently, empirical research that is called a *case study* in recent years appears to be a *case study*. For data analysis, researchers mainly and constantly use *descriptive statistics* with a proportion of 87.6% overall and 92% for the **target state (2020 - 2025)**. In contrast, the use of *inferential statistics* with a proportion of 19.2% overall and 26.3% for the **target state (2020 - 2025)** is small. Regarding the general use of empirical methods, we found that the number of empirical methods used for data collection and data analysis in a single paper increases over time, with *three to four empirical methods* most frequently used in one paper. For the **target state (2020 - 2025)**, researchers mainly use *three to even five empirical methods* in a single paper with average proportions of 22% (*three empirical methods used*), 25.3% (*four empirical methods used*), and 26.7% (*five empirical methods used*). This increase in the number of empirical methods used shows a shift as envisioned towards the use of several empirical methods and thus the collection and analysis of data from different perspectives to synthesize evidence. In addition to the empirical methods used, we also found a positive development regarding the reporting of important information on experimental design. For the **target state (2020 - 2025)**, the proportion of papers reporting *threats to validity*, providing *raw data and supplementary materials*, and highlighting their *research questions and answers* steadily increase over time with average proportions of 91.3% (*threats to validity*), 71.3% (*raw data and supplementary materials*), and 23.7% (*highlighted research questions and answer*) respectively 53% (*highlighted research question and answer hidden in the running text*). 

Despite the positive developments towards the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), we also identified the need for future improvements of empirical research in RE. While [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) envisioned an increased use of *action research*, we found that the proportion of *action research* is small over the entire timeframe analyzed (2000 - 2022) with an average proportion of only 2%. For the **target state (2020 - 2025)**, no paper reported the use of *action research*. According to [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), more *case studies* and *action research* are needed to ensure the industrial relevance of empirical research. This part of the vision is not yet nearly achieved. Regarding the reporting of threats to validity, we found two issues for future improvement. First, a proportion of 33.6% of the analyzed papers reporting threats to validity *only mentioned threats to validity* without any further classification of the types of validity. Although the general reporting of threats to validity is useful, the lack of classification of the reported threats to validity makes it difficult for a reader to have a clear overview of whether the threats to validity have been discussed comprehensively. In the future, researchers need to communicate their threats to validity comprehensively and transparently by discussing all types of validity equally and naming the type of validity addressed. Second, the proportion of papers reporting threats to *conclusion validity* with 18.2% is small compared to the other mainly discussed types of validity (*external validity*: 60.4%, *internal validity*: 56.1%, and *construct validity*: 47.9%). Therefore, researchers need to make more effort to comprehensively discuss the validity of their empirical research by also addressing the conclusion validity similar to the other types of validity. Regarding data analysis, the proportion of papers using *inferential statistics* is small with a proportion of only 26.2% for the **target state (2020 - 2025)**. For a mature use of statistical methods as envisioned by [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), researchers have to deal more with *inferential statistics* and include them in the data analysis of their empirical research.

## Conclusions
First of all, we want to remark that the generalizability of our findings is limited as KG-EmpiRE is in the first stage due to the limited analysis of the 570 papers from the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 2000 to 2022. This conference is the largest international conference in the research field of RE where a large number of established researchers in this field regularly publish high-quality, peer-reviewed (empirical) research papers. Therefore, the papers analyzed are representative of the target population of all papers in RE, but they still form only a small subset. Nevertheless, the results provide important insights into the state and evolution of empirical research in RE, especially published in [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/). For this reason, we consider our research approach suitable to enable a sustainable literature review on the state and evolution of empirical research in RE by using the ORKG with its technical infrastructure and services to build and publish KG-EmpiRE that the research community can constantly maintain, (re-)use, update, and expand by *dividing* the efforts to *conquer* the EmpiRE.

Using the ORKG, the extracted data is not encapsulated in a file as usual, which is, at best, published on a data repository, but in an openly available knowledge graph, which, to put it simply, is nothing more than a graph-based database. Overall, the ORKG offers a ready-to-use and sustainably governed infrastructure that implements best practices, such as FAIR principles and versioning, with services to support researchers in organizing (acquiring, curating, publishing, and processing) FAIR scientific data. As a result, the FAIR scientific data is openly available in the long term and can be understood, processed, and used by humans and machines. Thus, the research community can constantly maintain, (re-)use, update, and expand KG-EmpiRE, that we have built, published, and analyzed, in a long-term and collaborative manner. For example, in case of errors in data extraction, anyone, and in the best case the authors themselves, can update the data. It is also possible to expand KG-EmpiRE by curating more papers using or even expanding the [ORKG template](https://orkg.org/template/R186491) to extract more data in a structured, consistent, and comparable way. In all these cases, anyone can (re-)use this project to replicate this constantly updated data analysis and its results. Using the ORKG to organize scientific data helps to address two of the key challenges of literature reviews: **Lack of collaboration among researchers** and **updating literature reviews**. For this reason, we conclude that using the ORKG represents a step in the right direction towards sustainable literature reviews to ensure the quality, reliability, and timeliness of research findings for a successful long-term collaboration of researchers.

For our future work, we have a plan with short-, mid-, and long-term actions. As short-term actions, we expand KG-EmpiRE by describing more papers from the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) with our [ORKG template](https://orkg.org/template/R186491). Our goal over the coming months is to cover the entire research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 - 2023 to get a comprehensive overview of the state and evolution of empirical research in RE at this conference. We also establish a more general [ORKG observatory](https://orkg.org/observatory/Empirical_Software_Engineering) on empirical research in software engineering as a central access point to all curated papers. The observatory is an open group that anyone can join to contribute to the topic. As mid-term actions, we write and publish an [ORKG review](https://orkg.org/about/16/Reviews) about the state and evolution of empirical research in RE, based on the complete collection of all papers from the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 - 2023. An [ORKG review](https://orkg.org/about/16/Reviews) is a special kind of literature review article that the research community can constantly maintain when underlying content in the ORKG changes due to updates or expansions. Besides the [ORKG review](https://orkg.org/about/16/Reviews), we expand KG-EmpiRE by including more papers from other important venues, such as the journal [Requirements Engineering](https://link.springer.com/journal/766/volumes-and-issues) or the [International Working Conference on Requirement Engineering: Foundation for Software Quality](https://link.springer.com/conference/refsq), to gain a more comprehensive overview of the state and evolution of empirical research in RE. As long-term action, we extend the [ORKG template](https://orkg.org/template/R186491) to organize more extensive scientific data about empirical research in a structured, consistent, and comparable manner and thus to address the 61 still open [competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). With this plan, we work towards maintaining, updating, and expanding KG-EmpiRE together with the research community by *dividing* the efforts to *conquer* the EmpiRE.
</details>

<p align="right">(<a href="#top">back to top</a>)</p>

# Corresponding Author

[Dr. rer. nat. Oliver Karras](https://www.oliver-karras.de)

TIB - Leibniz Information Centre for Science and Technology

Department Research and Development

Data Science & Digital Libraries Research Group

Welfengarten 1B

30167 Hannover

E-Mail: [oliver.karras@tib.eu](mailto:oliver.karras@tib.eu)

<p align="right">(<a href="#top">back to top</a>)</p>

# How to Cite
If you want to cite this project, we suggest to use the following reference:
>Oliver Karras:<br/>
>[__Divide and Conquer the EmpiRE: A Community-Maintainable Knowledge Graph of Empirical Research in Requirements Engineering - A Sustainable Literature Review for Analyzing the State and Evolution of Empirical Research in Requirements Engineering__](https://zenodo.org/doi/10.5281/zenodo.8083528), Computer Software, Version v1.0, https://github.com/okarras/EmpiRE-Analysis, 2023.

You can also use the "**Cite this repository**" function in the top right menu resulting from the included [citation file format file](CITATION.cff) for human- and machine-readable citation information for software and datasets. Further information can be found on the [Citation File Format (CFF) website](https://citation-file-format.github.io/).

If you want to cite the related publication, use the reference in the section <a href="#related-publication">related publication</a>.

<p align="right">(<a href="#top">back to top</a>)</p>

Released under [MIT](/LICENSE) by [Oliver Karras](https://github.com/OKarras).
