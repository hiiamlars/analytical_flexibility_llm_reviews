# Analytical Flexibility in LLM Reviews

This repository contains the data generation pipeline and statistical analysis script for a study investigating analytical flexibility in Large Language Model (LLM) authored reviews. 

*Note: This project is currently preparing for preregistration on the Open Science Framework (OSF). The preregistration link and DOI will be added here once finalized.*

---

## Basic Repository Structure

The project is strictly organized to separate data generation from downstream statistical analysis:

```text
analytic_flexibility_llm_reviews/
├── README.md
├── LICENSE
├── .gitignore
│
├── data_generation/ # Python based pipeline via GoogleColab
│   ├── review_data_crawl.ipynb           # 1. Data fetching
│   ├── llm_review_generation.ipynb       # 2. Review generation
│   ├── llm_review_segmentation.ipynb     # 3. Review preprocessing
│   ├── llm_review_judgements.ipynb       # 4. Review judgements
│   ├── llm_review_post_processing.ipynb  # 5. Judgement postprocessing
└── analyses/ # R based pipeline via RStudio
    ├── analyses.qmd    # 6. Analysis file
    ├── analyses.html   # Rendered analyses report
    ├── references.bib  # Citation metadata
    └── apa.csl         # Citation style data
```

# Data Management for Data Generation

The python notebooks create all necessary folders for data storage and data loading on their own and on GoogleDrive. The only expected folder setup before execution of the first script `reivew_data_crawl.ipynb` is the following:

```text
MyDrive/
└── Analytical_flexibility_llm_reviews/
    └── iclr
```

# Data Management for Data Analyses

The Quarto file will load the data according to psychDS structure from a sub-folder `data`. Please note that is not the same location where the final python notebook has stored this file which means it will have to be copied over manually.

```text
analytical_flexibility_llm_reviews/
└── data
```
Note that you can make changes to the folder system or the overall setup but may need to adapt the scripts in that case.
