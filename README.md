# Analytical Flexibility in LLM Reviews

This repository contains the data generation pipeline and statistical analysis script for a study investigating analytical flexibility in Large Language Model (LLM) authored reviews. 

*Note: This project is currently preregistered on the Open Science Framework (OSF) under embargo. The preregistration link and DOI will be added here once the embargo is lifted.*

---

## Basic Repository Structure

The project is strictly organized to separate data generation from downstream statistical analysis and data files:

```text
analytic_flexibility_llm_reviews/
├── README.md
├── LICENSE.txt
├── .gitignore
├── registration
│   └── prereg.pdf
├── data_generation/
│   ├── 00_review_data_crawl.ipynb
│   ├── 01_llm_review_generation.ipynb
│   ├── 02_llm_review_segmentation.ipynb
│   ├── 03_llm_review_judgements.ipynb
│   ├── 04_llm_review_post_processing.ipynb
│   └── llm_review_generation.ipynb
├── data/
│   ├── iclr/
│   └── llm_reviews/
└── analyses/
    ├── analyses.qmd
    ├── analyses.html
    ├── references.bib
    └── apa.csl

Note that the python script for review generation was edited after preregistration and that the edited version 'llm_review_generation.ipynb' should be executed in replacement of the registered one.
```

# Data Management for Data Generation

The python notebooks create all necessary folders for data storage and data loading on their own and on GoogleDrive. The only expected folder setup before execution of the first script `00_review_data_crawl.ipynb` is the following:

```text
MyDrive/
└── Analytical_flexibility_llm_reviews/
    └── iclr/
```

# Data Management for Data Analyses

The Quarto file will load the data according to psychDS structure from a sub-folder `data`. Please note that the python scripts stored the data on GoogleDrive, everything else is handled in a separate folder system. For this all data files have to be copied over manully into the following structure:

```text
analytical_flexibility_llm_reviews/
└── data/
    ├── iclr/
    └── llm_reviews/
```
Note that you can make changes to the folder system or the overall setup but may need to adapt the scripts in that case.
