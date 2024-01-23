# RE24 Artifact Track Criteria
 is a community-maintainable knowledge graph on empirical research in requirements engineering that consists of 626 papers from the IEEE International Conference on Requirement Engineering. The ORKG is an infrastructure with service for the organization of FAIR scientific knowledge from publications, software, and datasets. 

## Available

### Contentwise for 2-Pager
- Permanently available for retrievel
- Publicly accessible archival repository such as Zenodo
- DOI via archival repository with references in artifact and paper(?)

### Criteria
1. The artifact is hosted online:
    1. The URL to access the artifact is immutable and a DOI redirects to the immutable URL.

        The artifact consists of two parts:
        1. KG-EmpiRE: All papers curated in KG-EmpirRE are part of the Open Research Knowledge Graph (ORKG) that is accessible unter the following URL: https://orkg.org. All contents in the ORKG have https:// + Uniform Resource Identifiers (URIs) so that their are accessible on the web. The central accees point to all curated papers is accessible under the following URL: https://orkg.org/observatory/Empirical_Software_Engineering?sort=combined&classesFilter=Paper,Comparison,Visualization. The ORKG is a permanent service of TIB - Leibniz Information Centre for Science and Technology, which has committed itself to long-term archiving of the data and regularly performs RDF dumps as backups.
        2. Jupyter notebook: The data analysis is implemented as a Jupyter notebook that is accessible on GitHub: https://github.com/okarras/EmpiRE-Analysis. We also publish the releases on Zenodo: https://doi.org/10.5281/zenodo.8083529. In this way, we obtain a DOI that redirects to the immutable URL of the GitHub repository. These releases also include the newest RDF dump of the ORKG from TIB. The interactive version is hosted on mybinder.

2. The artifact contains a README.md file summarizing:
    1. "Summary of the Artifact":
        - What does the artifact?
        - What are the expected inputs and outputs?
        - What is the motivcation for developing the artifact?
    2. "Authors' Information":
        - List all authors
        - List how to cite a work that uses the artifact
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