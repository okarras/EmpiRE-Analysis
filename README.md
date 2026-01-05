<a id='top'></a>
<div align="center">
  <a href="https://github.com/okarras/EmpiRE-Analysis">
    <img src="Supplementary%20materials/logo.jpg" alt="Logo" width="250" height="250">
  </a>

<h2 align="center" style="font-weight: normal">Divide and Conquer the <b>EmpiRE</b>: A Community-Maintainable Knowledge Graph of <b>Empi</b>rical Research in <b>R</b>equirements <b>E</b>ngineering<br/>
<i>A Sustainable Literature Review for Analyzing the State and Evolution of Empirical Research in Requirements Engineering</i></h2><br/>

[![GitHub - Project](https://img.shields.io/badge/GitHub-Project-2ea44f)](https://github.com/okarras/EmpiRE-Analysis) [![Issues - Bug Report](https://img.shields.io/badge/Issues-Bug_Report-2ea44f)](https://github.com/okarras/EmpiRE-Analysis/issues)  [![Issues - Feature Request](https://img.shields.io/badge/Issues-Feature_Request-2ea44f)](https://github.com/okarras/EmpiRE-Analysis/issues) [![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

[![KG-EmpiRE - Dashboard](https://img.shields.io/badge/KG--EmpiRE-Dashboard-5d99c4)](https://empire-compass.tib.eu/R186491/)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18154586.svg)](https://doi.org/10.5281/zenodo.18154586) [![ORKG - KG-EmpiRE](https://img.shields.io/badge/ORKG-KG--EmpiRE-e86161)](https://orkg.org/observatory/Empirical_Software_Engineering?sort=combined&classesFilter=Paper,Comparison,Visualization)
[![ORKG - RDF dump](https://img.shields.io/badge/ORKG-RDF_dump-e86161)](https://orkg.org/api/rdf/dump)
</div>

> [!IMPORTANT]  
> The content of this repository was reviewed on the [Artifact Evaluation Track](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts) of the [32nd IEEE International Requirements Engineering Conference 2024](https://conf.researchr.org/home/RE-2024) and received the [![Badge - Available](https://custom-icon-badges.demolab.com/badge/Badge-Available-B4CEA0?logo=award&logoSource=feather)](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts#Submission-Instructions), the [![Badge - Reusable](https://custom-icon-badges.demolab.com/badge/Badge-Reusable-F09D9F?logo=award&logoSource=feather)](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts#Submission-Instructions), and the [![Award - Best Artifact](https://custom-icon-badges.demolab.com/badge/Award-Best_Artifact-D4AF37?logo=trophy&logoColor=fff)](https://www.oliver-karras.de/wp-content/uploads/2024/06/IEEE_RE2024_Certifiacte_Best_Artifact_Award.pdf).

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
    <li><a href="#related-publications">Related Publications</a></li>
    <li><a href="#executive-summary">Executive Summary</a></li>
    <li><a href="#corresponding-author">Corresponding Author</a></li>
    <li><a href="#how-to-cite">How to Cite</a></li>
  </ol>
</details>

# About the Project
This project contains the constantly updated [data](SPARQL-Data/), [analysis](empire-analysis.ipynb), and [results](Figures/) of a sustainable literature review on the state and evolution of empirical research in requirements engineering (RE) using the developed KG-EmpiRE.

KG-EmpiRE is a community-maintainable knowledge graph (KG) of empirical research in requirements engineering based on scientific data extracted from *currently* **776 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 to 2025. We are *currently* organizing scientific data in KG-EmpiRE using a defined [template](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf) for the six [themes](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf) *research paradigm*, *research design*, *research method*, *data collection*, *data analysis* and *bibliographic metadata* with the long-term plan to expand the themes.

KG-EmpiRE itself is maintained in the [Open Research Knowledge Graph (ORKG)](https://orkg.org). The ORKG is a cross-domain and cross-topic research knowledge graph (RKG) with corresponding technical infrastructure and services for the organization of Findable, Accessible, Interoperable, and Reusable (FAIR) scientific data from papers in accordance with the [FAIR data principles](https://doi.org/10.1038/sdata.2016.18). The [TIB - Leibniz Information Centre for Science and Technology](https://www.tib.eu/en/research-development/open-research-knowledge-graph) develops and maintains the ORKG permanently and has committed itself to the long-term archiving of all data. As a central access point to all curated papers in KG-EmpiRE, we established a more general [ORKG observatory](https://orkg.org/observatory/Empirical_Software_Engineering) on empirical research in software engineering. In addition, the ORKG provides a [RDF dump](https://orkg.org/api/rdf/dump) of all its data, including the most recent data from KG-EmpiRE. We also store the [data](SPARQL-Data/) used for analysis as CSV files.

> [!NOTE]  
> For each <a href="#related-publications">related publication</a>, we provide a folder containing the respective CSV files to enable the replication of the results. The details on the replication of the results can be found in the <a href="#usage-instructions">usage instructions</a>.

In this project, we perform the data analysis of KG-EmpiRE, which has two purposes:

1. We evaluate the coverage of the curated topic of empirical research in RE by KG-EmpiRE.

2. We gain insights into the state and evolution of empirical research in RE.

The data analysis is based on competency questions regarding empirical research in SE, including RE, derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30). They describe their vision of the role of empirical methods in SE, including RE, for the period of 2020 – 2025 by comparing the **"current" state of practice (2007)** with their **target state (2020 - 2025)**. We analyzed these descriptions and derived a total of [77 competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). The number of competency questions answered reflects the **coverage of the curated topic in KG-EmpiRE** (1), and the answers to competency questions provide **insights into the state and evolution of empirical research in RE** (2). For each competency question that can be answered with KG-EmpiRE (*currently* 16 of 77), we specified [SPARQL](https://www.w3.org/TR/sparql11-query/) queries to retrieve and analyze the data of KG-EmpiRE from the ORKG. We provide all details of the analysis with its SPARQL queries, [data](SPARQL-Data/), [visualizations](Figures/), and explanations in the [Jupyter Notebook](empire-analysis.ipynb) hosted on [binder](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb) for interactive replication and (re-)use, always using the most recent data from KG-EmpiRE. In addition, we developed the neuro-symbolic dashboard [EmpiRE-Compass](https://empire-compass.tib.eu/R186491/) that is designed to support the sustainable synthesis, discovery, and reuse of scientific knowledge about empirical research on Requirements Engineering (RE) using ORKG and large language models.

The [analysis](empire-analysis.ipynb) of the individual competency questions always follows the same structure:

1. *Data Selection*: Explaining the competency question and the required data for the analysis.
2. *Data Collection*: Executing the specified SPARQL query to retrieve the data.
3. *Data Exploration*: Exploring the data, including its cleaning and validation, to prepare the data for data analysis.
4. *Data Analysis*: Analyzing the data and creating visualizations.
5. *Data Interpretation*: Interpreting the data and derive insights.

Overall, this project serves to make the [data](SPARQL-Data/), [analysis](empire-analysis.ipynb), and [results](Figures/) openly available in the long term according to the [FAIR data principles](https://doi.org/10.1038/sdata.2016.18) to enable a replicable, (re-)usable and thus sustainable literature review.

In this way, this project can be used for:

1. Replication of the results from the <a href="#related-publications">related publications</a>.

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
┃   ┣━ CQ7/...contains 8 visualizations
┃   ┣━ CQ8/...contains 2 visualizations
┃   ┣━ CQ9/...contains 2 visualizations
┃   ┣━ CQ10/...contains 2 visualizations
┃   ┣━ CQ11/...contains 2 visualizations
┃   ┣━ CQ12/...contains 4 visualizations
┃   ┣━ CQ13/...contains 2 visualizations
┃   ┣━ CQ14/...contains 2 visualizations
┃   ┣━ CQ15/...contains 2 visualizations
┃   ┗━ CQ16/...contains 2 visualizations
┗━ SPARQL-Data/
    ┣━ ESEM 2023/...contains 22 CSV files from the SPARQL queries to replicate the results from the ESEM 2023 publication
    ┣━ Most recent data/...contains 22 CSV files from the SPARQL queries to use the most recent data of KG-EmpiRE
    ┗━ RE 2024/...contains 22 CSV files from the SPARQL queries to replicate the results from the RE 2024 publication
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
| [SPARQL-Data/](SPARQL-Data/)| Storage location of the data retrieved by the corresponding SPARQL queries of the competency questions organized in individual folders per <a href="#related-publications">related publication</a>.|
| [SPARQL-Data/ESEM 2023](SPARQL-Data/ESEM%202023/)| The folder contains a set of 22 CSV files of the data retrieved with the SPARQL queries to replicate the results from the ESEM 2023 publication.|
| [SPARQL-Data/Most recent data](SPARQL-Data/Most%20recent%20data/)| The folder contains a set of 22 CSV files of the data retrieved with the SPARQL queries to use the most recent data of KG-EmpiRE.|
| [SPARQL-Data/RE 2024](SPARQL-Data/RE%202024/)| The folder contains a set of 22 CSV files of the data retrieved with the SPARQL queries to replicate the results from the RE 2024 publication.|
| [Supplementary materials/](Supplementary%20materials/)| Storage location of the supplementary materials of the [analysis](empire-analysis.ipynb) and the <a href="#related-publications">related publications</a>.|
| [Supplementary materials/approach.png](Supplementary%20materials/approach.png)| Visualization of the research approach for building, publishing, and analyzing KG-EmpiRE.|
| [Supplementary materials/Detailed list of all 77 competency questions.xlsx](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx)| The detailed list of all 77 competency questions derived from the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) of regarding the role of empirical methods in all fields of SE, including RE.|
| [Supplementary materials/Detailed ORKG template structure.pdf](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf)| The detailed overview of the developed ORKG template for structuring the scientific data extracted from the *currently* **776 papers**.|
| [Supplementary materials/logo.jpg](Supplementary%20materials/logo.jpg)| Logo of the project.|
| [Supplementary materials/Overview of all content for data extraction.pdf](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf)| The detailed overview of all content identified for data extraction.|
| [CITATION.cff](CITATION.cff)| The file contains human- and machine-readable citation information for software and datasets. Further information can be found on the [Citation File Format (CFF) website](https://citation-file-format.github.io/).|
| [empire-analysis.ipynb](empire-analysis.ipynb)| Jupyter Notebook that contains the entire data analysis of KG-EmpiRE for answering the 16 competency questions.|
| [LICENSE](LICENSE)| License of the project.|
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
> We have only tested the analysis on systems with the Windows operating system, which is why we specify Windows as a necessary system requirement. However, the analysis should also run on other operating systems.

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
In the following, we explain the steps for using the project for the two cases of replication of results from the <a href="#related-publications">related publications</a> and (re-)use of KG-EmpiRE with its most recent data, assuming that the project is executed either <a href="#installation-instructions">locally</a> or on one of the <a href="#executable-machines-and-environments">executable machines and environments</a>. 

## Replication of the results from the related publications

1. In the section "*2. Reusable Functions for Data Analysis*" of the [Jupyter Notebook](empire-analysis.ipynb), change the **DATE** and **PATH** variables from "*now.strftime('%Y-%m-%d')*" and "*'SPARQL-Data/Most recent data/query_'*" to the date and path specified for the respective <a href="#related-publications">related publication</a> to use the corresponding CSV files. Below, we show the code example for the replication of the results from the RE 2024 publication. The results of ESEM 2023 publication can be replicated accordingly.

    ```python
    #For using the most recent data of KG-EmpiRE, use the following date and path.
    #DATE = now.strftime('%Y-%m-%d')
    #PATH = 'SPARQL-Data/Most recent data/query_'

    #For replication of the related publication from ESEM 2023, use the following date and path.
    #DATE = '2023-06-26'
    #PATH = 'SPARQL-Data/ESEM 2023/query_'

    #For replication of the related publication from RE 2024, use the following date and path.
    DATE = '2024-04-30'
    PATH = 'SPARQL-Data/RE 2024/query_'
    ```
1. Restart the kernel and clear all outputs.
2. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

## (Re-)use of KG-EmpiRE with its most recent data

1. In section "*2. Reusable Functions for Data Analysis*" of the [Jupyter Notebook](empire-analysis.ipynb), ensure that the **DATE** and **PATH** variables are set to "*now.strftime('%Y-%m-%d')*" and "*'SPARQL-Data/Most recent data/query_'*".

    ```python
    #For using the most recent data of KG-EmpiRE, use the following date and path.
    DATE = now.strftime('%Y-%m-%d')
    PATH = 'SPARQL-Data/Most recent data/query_'

    #For replication of the related publication from ESEM 2023, use the following date and path.
    #DATE = '2023-06-26'
    #PATH = 'SPARQL-Data/ESEM 2023/query_'

    #For replication of the related publication from RE 2024, use the following date and path.
    #DATE = '2024-04-30'
    #PATH = 'SPARQL-Data/RE 2024/query_'
    ```
2. Restart the kernel and clear all outputs.
3. Run all cells.

<p align="right">(<a href="#top">back to top</a>)</p>

# Related Publications
The first version of KG-EmpiRE based on **570 papers** from the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 2000 to 2022 and the first analysis of the sustainable literature review on the state and evolution of empirical research in RE have been published in:

>Oliver Karras, Felix Wernlein, Jil Klünder, and Sören Auer:<br/>
>[__Divide and Conquer the EmpiRE: A Community-Maintainable Knowledge Graph of Empirical Research in Requirements Engineering__](https://doi.org/10.1109/ESEM56168.2023.10304795),
>In: 2023 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM), New Orleans, LA, USA, 2023, pp. 1-12.<br/>
>
>The publication received the  [![Award - Best Paper](https://custom-icon-badges.demolab.com/badge/Award-Best_Paper-D4AF37?logo=trophy&logoColor=fff)](https://www.oliver-karras.de/wp-content/uploads/2023/10/acm_ieee_esem2023_certificate_best_paper_award.pdf) of the 17th ACM/IEEE International Symposium on Empirical Software Engineering and Measurement 2023.

The second version KG-EmpiRE based on **680 papers** from the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1994 to 2022 and the analysis of the sustainable literature review on the state and evolution of empirical research in RE have been published in:

>Oliver Karras:<br/>
>[__KG-EmpiRE: A Community-Maintainable Knowledge Graph for a Sustainable Literature Review on the State and Evolution of Empirical Research in Requirements Engineering__](https://doi.org/10.1109/RE59067.2024.00063),
>In: 2024 IEEE International Requirements Engineering Conference (RE), Reykjavík, Iceland, 2024.<br/>
>
>The artifact received the [![Badge - Available](https://custom-icon-badges.demolab.com/badge/Badge-Available-B4CEA0?logo=award&logoSource=feather)](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts#Submission-Instructions), the [![Badge - Reusable](https://custom-icon-badges.demolab.com/badge/Badge-Reusable-F09D9F?logo=award&logoSource=feather)](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts#Submission-Instructions), and [![Award - Best Artifact](https://custom-icon-badges.demolab.com/badge/Award-Best_Artifact-D4AF37?logo=trophy&logoColor=fff)](https://www.oliver-karras.de/wp-content/uploads/2024/06/IEEE_RE2024_Certifiacte_Best_Artifact_Award.pdf) from the [Artifact Evaluation track](https://conf.researchr.org/track/RE-2024/RE-2024-artifacts) of the [32nd IEEE International Requirements Engineering Conference 2024](https://conf.researchr.org/home/RE-2024).

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
Our research approach consists of three steps: Data collection, Data extraction, and Data analysis. So far, **we collected 776 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 to 2025. **We extracted and organized their scientific data** on the six themes *research paradigm*, *research design*, *research method*, *data collection*, *data analysis* and *bibliographic metadata* using a developed [ORKG template](https://orkg.org/template/R186491). ORKG templates are an implementation of a subset of SHACL and allow specifying the structure of descriptions of papers. In this way, we determined which data to extract and ensured that all the descriptions of papers were consistent and comparable to **build and publish KG-EmpiRE**. In the supplementary materials, we provide a comprehensive overview of [all contents for data extraction](Supplementary%20materials/Overview%20of%20all%20content%20for%20data%20extraction.pdf) and the [ORKG template](Supplementary%20materials/Detailed%20ORKG%20template%20structure.pdf).

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
> The following insights are *currently* based on the results of the second analysis of KG-EmpiRE with the data from **776 papers** published in the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 to 2025.

The analysis of KG-EmpiRE reveals a clear and sustained state and evolution of empirical research practice in RE. Over the past three decades, the proportion of papers including an empirical study has increased dramatically, rising from an average of 48.6% in the 1990s to 95.0% in the **target state (2020 - 2025)**. This trajectory confirms the vision by [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), in which empirical studies were expected to become the standard rather than the exception. In parallel, the proportion of papers without empirical studies has declined sharply, from 51.4% in the 1990s to only 5.0% in the **target state (2020 - 2025)**. This near disappearance of non-empirical work reflects a cultural and methodological shift toward evidence-based research in RE.

The use of empirical methods for data collection has diversified substantially. *Case studies*, once the dominant method and peaking at 78.0% in 1996, have steadily declined to an average of 20.5% in the **target state (2020 - 2025)**. This decline does not indicate a loss of relevance but rather a more precise and rigorous use of the term, consistent with the observation by [Wohlin](https://doi.org/10.1016/j.infsof.2021.106514) that case studies were often misapplied in earlier decades. *Experiments*, by contrast, have grown in importance, rising from only 8.0% in 2007 to 34.8% in the **target state (2020 - 2025)**, with a peak of 57.0% in 2022. *Surveys* have also increased in adoption, from 8.0% in 2007 to 25.8% in the **target state (2020 - 2025)**, while *interviews* have remained stable at around 21.5%. *Secondary research* has become particularly prominent, growing from 12.0% in 2007 to 41.5% in the **target state (2020 - 2025)**, reflecting the increasing value of systematic reviews and archive analyses. *Action research*, however, remains absent in recent years, with no papers reporting its use in the **target state (2020 - 2025)**. This lack of adoption highlights a gap in industrial relevance, as [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) emphasized the importance of *action research* alongside *case studies* to strengthen the connection between empirical research and practice.

For data analysis, *descriptive statistics* remain the most widely used method, consistently dominating across all decades and reaching 96.0% in the **target state (2020 - 2025)**. Inferential statistics have grown modestly, from 13% in 2007 to 22.3% in the **target state (2020 - 2025)**, but their limited adoption suggests that statistical maturity is still incomplete. *Machine learning* methods, by contrast, have emerged strongly since 2010, reaching 41.7% in the **target state (2020 - 2025)** and marking a significant methodological shift toward computational approaches. *Other methods*, often representing qualitative coding techniques, are also widely used, with 72.5% adoption in the **target state (2020 - 2025)**, though their heterogeneity calls for finer-grained categorization in future analyses. Taken together, these findings indicate that while *descriptive statistics* remain foundational, the field of RE has diversified toward more advanced and varied approaches, though *inferential statistics* remain underutilized.

The number of empirical methods used per paper has also increased, reflecting methodological diversity. Whereas papers in the **"current" state of practice (2007)** typically employed two or three methods, papers in the **target state (2020 - 2025)** most often use three to five methods, with proportions of 14.7% for three methods, 28.2% for four methods, and 23.0% for five methods. This trend demonstrates alignment with the vision by [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) of synthesizing evidence from multiple perspectives, though it also underscores the need for robust frameworks to integrate diverse findings coherently.

Reporting practices have improved markedly over time. *Threats to validity* are now reported in 91.5% of papers in the **target state (2020 - 2025)**, compared to only 17.5% in 2000–2009. However, a third of these papers mention threats without classifying them, and *conclusion validity* remains underreported at 18.6%, compared to external validity (60.4%), internal validity (56.1%), and construct validity (47.9%). This imbalance suggests that while transparency has improved, comprehensive discussion of validity remains incomplete. *Provision of data* has also advanced, with 83.0% of papers in the **target state (2020 - 2025)** providing URLs to raw data or supplementary materials, reflecting a strong cultural shift toward openness and reproducibility. Research questions and answers are more frequently highlighted, with 22.7% of papers in the **target state (2020 - 2025)** presenting them explicitly, while hidden reporting has declined, improving accessibility of findings.

*Secondary research* methods have evolved as well. Archive analysis dominates, accounting for 58.0% of secondary research in the **target state (2020 - 2025)**, while systematic literature reviews have grown to 17.0%, signaling increased methodological rigor. Traditional literature reviews persist at 16.5%, but their relative importance has declined. This evolution shows partial realization of the vision by [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30), as systematic approaches are more common but not yet dominant.

Finally, statistical practice remains uneven. *Descriptive statistics* continue to dominate, with basic measures such as *counts*, *percentages*, and *means* widely applied, while more advanced techniques such as *variance* analysis and *boxplots* remain underutilized. *Inferential statistics* are applied inconsistently, with 72 different tests identified but none used widely. The most frequent test, *Shapiro–Wilk*, appears in only 3.1% of papers. This imbalance suggests that while statistical diversity has increased, maturity in applying inferential methods is still lacking.

In summary, the results demonstrate that the vision of [Sjøberg et al. (2007)](https://doi.org/10.1109/FOSE.2007.30) has been largely realized. Empirical studies dominate, methodological diversity has increased, and reporting practices have matured. However, important gaps remain, particularly in the adoption of *action research*, the comprehensive use of *inferential statistics*, and the balanced reporting of *threats to validity*. Addressing these gaps will be critical for advancing RE toward a fully mature, evidence-based discipline that is both scientifically rigorous and industrially relevant.

## Conclusions
First, we would like to point out that the generalizability of our results is limited, as KG-EmpiRE currently comprises 776 papers from the research area of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from the years 1993 to 2025. This conference is the largest international conference in the research field of RE where a large number of established researchers in this field regularly publish high-quality, peer-reviewed (empirical) research papers. Therefore, the papers analyzed are a representative for the target population of all papers in RE, but they still form only a small subset. Nevertheless, the results provide important insights into the state and evolution of empirical research in RE, especially published in [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/). For this reason, we consider our research approach suitable to enable a sustainable literature review on the state and evoluation of emirical research in RE by using the ORKG with its technical infrastructure and services to build and publish KG-EmpiRE that the research community can constantly maintain, (re-)use, update, and expand by *dividing* the efforts to *conquer* the EmpiRE.

Using the ORKG, the extracted data is not encapsulated in a file as usual, which is, at best, published on a data repository, but in a openly available knowledge graph, which, to put it simply, is nothing more than a graph-based database. Overall, the ORKG offers an ready-to-use and sustainably governed infrastructure that implements best practices, such as FAIR principles and versioning, with services to support researchers in organizing (acquiring, curating, publishing, and processing) FAIR scientific data. As a result, the FAIR scientific data is openly available in the long term and can be understood, processed, and used by humans and machines. Thus, the research community can constantly maintain, (re-)use, update, and expand KG-EmpiRE, that we have built, published, and analyzed, in a long-term and collaborative manner. For example, in case of errors in data extraction, anyone, and in the best case the authors themselves, can update the data. It is also possible to expand KG-EmpiRE by curating more papers using or even expanding the [ORKG template](https://orkg.org/template/R186491) to extract more data in a structured, consistent, and comparable way. In all these cases, anyone can (re-)use this project to replicate this constantly updated data analysis and its results. Using the ORKG to organize scientific data helps to address two of the key challenges of literature reviews: **Lack of collaboration among researchers** and **updating literature reviews**. For this reason, we conclude that using the ORKG represents a step in the right direction towards sustainable literature reviews to ensure the quality, reliability, and timeliness of research findings for a successful long-term collaboration of researchers.

For our future work, we have a plan with short-, mid-, and long-term actions. As short-term actions, we expand KG-EmpiRE by continuously describing more papers from the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) with our [ORKG template](https://orkg.org/template/R186491) to get a comprehensive overview of the state and evolution of empirical research in RE at this conference. We also establish a more general [ORKG observatory](https://orkg.org/observatory/Empirical_Software_Engineering) as a central access point to all curated papers. The observatory is an open group that anyone can join to contribute to the topic. As mid-term actions, we write and publish a literature review article about the state and evolution of empirical research in RE, based on the complete collection of all papers from the research track of the [IEEE International Conference on Requirement Engineering](https://requirements-engineering.org/) from 1993 - 2025. We also expand KG-EmpiRE by including more papers from other important venues, such as the journal [Requirements Engineering](https://link.springer.com/journal/766/volumes-and-issues) or the [International Working Conference on Requirement Engineering: Foundation for Software Quality](https://link.springer.com/conference/refsq), to gain a more comprehensive overview of the state and evolution of empirical research in RE. As long-term action, we extend the [ORKG template](https://orkg.org/template/R186491) to organize more extensive scientific data about empirical resarch in a structured, consistent, and comparable manner and thus to address the 61 still open [competency questions](Supplementary%20materials/Detailed%20list%20of%20all%2077%20competency%20questions.xlsx). With this plan, we work towards maintaining, updating, and expanding KG-EmpiRE togehter with the research community by *dividing* the efforts to *conquer* the EmpiRE.
</details>

<p align="right">(<a href="#top">back to top</a>)</p>

# Corresponding Author

[Dr. rer. nat. Oliver Karras](https://www.oliver-karras.de)

Researcher and Data Scientist - Open Research Knowledge Graph

TIB - Leibniz Information Centre for Science and Technology

Welfengarten 1B

30167 Hannover

E-Mail: [oliver.karras@tib.eu](mailto:oliver.karras@tib.eu)

<p align="right">(<a href="#top">back to top</a>)</p>

# How to Cite
If you want to cite this project, we suggest using the following reference:
>Oliver Karras:<br/>
>[__Divide and Conquer the EmpiRE: A Community-Maintainable Knowledge Graph of Empirical Research in Requirements Engineering - A Sustainable Literature Review for Analyzing the State and Evolution of Empirical Research in Requirements Engineering__](https://doi.org/10.5281/zenodo.18154586), Computer Software, Version v1.1, https://github.com/okarras/EmpiRE-Analysis, 2024.


You can also use the "**Cite this repository**" function in the top right menu resulting from the included [citation file format file](CITATION.cff) for human- and machine-readable citation information for software and datasets. Further information can be found on the [Citation File Format (CFF) website](https://citation-file-format.github.io/).

If you want to cite the related publications, use the references in the section <a href="#related-publications">related publications</a>.

<p align="right">(<a href="#top">back to top</a>)</p>

Released under [MIT](/LICENSE) by [Oliver Karras](https://github.com/OKarras).
