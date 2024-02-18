# RE24 Artifact Track Criteria

## Available

### Contentwise for 2-Pager
- Permanently available for retrievel
  - GitHub, Zenodo, mybinder, and ORKG
- Publicly accessible archival repository such as Zenodo
  - Zenodo
- DOI via archival repository with references in artifact and 2-page paper
  - in Read.me of the project
  - Will be cited in the 2-page paper

### Criteria
1. The artifact is hosted online:
   
   1. GitHub Project: The GitHub project contains the data analysis of KG-EmpiRE which is implemented as a [Jupyter Notebook](empire-analysis.ipynb) that is hosted on [GitHub](https://github.com/okarras/EmpiRE-Analysis). We also publish the releases on [Zenodo](https://doi.org/10.5281/zenodo.8083529). These releases also contain an [RDF dump](Supplementary%20materials/rdf-export-orkg-2023-06-26.nt) of the ORKG to include the most recent data from KG-EmpiRE. The project is also hosted on [mybinder](https://mybinder.org/v2/gh/okarras/EmpiRE-Analysis/HEAD?labpath=%2Fempire-analysis.ipynb) for interactive reproduction and (re-)use, always using the most recent data from KG-EmpiRE.
   
   2. KG-EmpiRE: The scientific date extracted form all papers curated in KG-EmpiRE is part of the [Open Research Knowledge Graph (ORKG)](https://orkg.org). As a central accees point to all curated papers in KG-EmpiRE, we establish a more general [ORKG observatory](https://orkg.org/observatory/Empirical_Software_Engineering) on empirical research in software engineering. The [TIB - Leibniz Information Centre for Science and Technology](https://www.tib.eu/en/research-development/open-research-knowledge-graph) developes and maintains the ORKG permanently and has committed itself to the long-term archiving of all data. In addition, we add a [RDF dump](Supplementary%20materials/rdf-export-orkg-2023-06-26.nt) of the ORKG that includes the most recent data from KG-EmpiRE to every release that is published on [Zenodo](https://doi.org/10.5281/zenodo.8083529).

2. The artifact contains a README.md file summarizing:

   1. "Summary of the Artifact":

      - What does the artifact?

        The project contains the constantly update analysis and results of a sustainable literature review on the state and evolution of empirical research in RE using the developed KG-EmpiRE. KG-EmpiRE is a community-maintainable knowledge graph of empirical research in RE, which is maintained in the Open Research Knowledge Graph (ORKG). The ORKG with its technical infrastructure and services makes the data of the literature review openly available in the long term according to the FAIR data principles.

      - What are the expected inputs and outputs?

        Inputs: Based on 16 competency questions, the corresponding scientific data extracted from *currently* 634 papers curated in KG-EmpiRE is used as input for the individual analyses.
        
        Outputs: For each competency question, we provide the corresponding scientific data with visualizations and explanations as output of the individual analysis.

      - What is the motivation for developing the artifact?

        Overall, this project serves to make the data, analyses, and results openly accessible in the long term to enable a reproducible, (re-)usable and thus sustainable literature review.

          In this way, the project can be used to:

          1. Reproduce the results from the related Publication: O. Karras et al.:[Divide and Conquer the EmpiRE: A Community-Maintainable Knowledge Graph of Empirical Research in Requirements Engineering](https://doi.org/10.1109/ESEM56168.2023.10304795), In: 2023 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM), New Orleans, LA, USA, 2023, pp. 1-12.

          2. (Re-)use KG-EmpiRE with its data for other research on empirical research in RE.

          3. Replicate our research approach for sustainable literature reviews on other topics.

    2. "Authors' Information":
        - Author of the project:
  
          [Dr. rer. nat. Oliver Karras](https://www.oliver-karras.de)

          TIB - Leibniz Information Centre for Science and Technology

          Department Research and Development

          Data Science & Digital Libraries Research Group

          Welfengarten 1B

          30167 Hannover

          E-Mail: [oliver.karras@tib.eu](mailto:oliver.karras@tib.eu)

        - List how to cite a work that uses the artifact
  
          1. Included [CFF-file](CITATION.cff) for "cite this repository" in the menu on the top right.
          
          2. Added reference to the related publication.

    3. "Artifact Loction":
        - Describe at which URL and DOI the artifact can be obtained
3. The artifact contains a LICENSE file with a propoer open-source license.
4. Anyone must be able to access the artifact, without the need for registration.

## Reusable

### Contentwise for 2-Pager
- well-documented, exercisable, complete, includes appropriate evidence of verification
- facilitate reuse and repurpose
- Norms and standards of the research community should be strictly adhered to 

### Criteria
1. Test usability of the artifact on a fresh environment.

   Tested successful with 3 differnt systems.

2. Fulfill all criteria for "Available".
3. The artifact has an extended README.md file:
    1. Same points as for "Available"
    2. "Description of the Artifact":
        - Describe each file in the artifact
    3. "System Requirements":
        - State the required system needed to run the artifact
        - State the required programs needed to run the artifact
        - State the required libraries needed to run the artifact
    4. "Installation Instructions":
        - Detailed description of how to run the artifact from scratch
    5. "Executable machine & environment":
        - Provide an executable version of artifact (We use mybinder.org).
    6. "Maximum Runnable Time":
        - The artifact must be runnable in a maximum of 60 minutes
    7. "Usage Instructions":
        - Explain how the artifact can be used.
        - For tools: Provide instructions on how to interact with the artifact
        - For tools: Provide all information about the artifact that enables others to reuse the artifact
        - For dataset: Provide explanations on how the artifact can be reused by others
    8. "Steps to Reproduce":
        - Provide instructions on how to generate the results in the paper
        - Known deviations from results presented in the paper should be explicitly outlined
        - Time for reproducing must be at maximum 60 minutes.

## 2-pager
1. Describe how the artifact builds on the previous paper or previous artifact.
2. Use IEEE format 