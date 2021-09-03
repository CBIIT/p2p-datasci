---
layout: post
title: "ATOM Modeling Pipeline (AMPL) for Drug Discovery"
subtitle: "A hands-on tutorial"
cover-img: "/assets/img/zebrafish.jpg"
tags: [event-announcement]
---

Do you want to know how to use Machine Learning (ML) for accelerating drug discovery? 
Join us on September 14, 2:00 pm – 3:30 pm ET for the second workshop on using Machine Learning (ML) to accelerate drug discovery! The workshop focuses on using the Atom Modeling PipeLine (AMPL), an open-source conda-based software that automates key drug discovery steps. AMPL is designed to take molecular binding data (ex., IC50, ki, etc.) and carry out the ML steps with minimal user intervention (see the figure shown above). The first workshop held in June highlighted AMPL’s capabilities for creating ML-ready datasets.


**Date:** Tuesday, Sep 14, 2021

**Time:** 2:00 p.m – 3:30 p.m. ET

**Recording**: [here](https://youtu.be/NJ_3ExXXk_o)

**Presentation**: [here](../attachments/AMPL-workshop-08042021.pdf)

**Location:** [Webex](https://cbiit.webex.com/cbiit/onstage/g.php?MTID=e48de54732116bf8fc1f281aae7d60bd2)

**Registration:** Not required

**Presenter:** [Sarangan Ravichandran, PhD, PMP](https://sites.google.com/site/sakaravi/) Senior Data Scientist, ATOM Consortium/Frederick National Laboratory for Cancer
               Research ([FNLCR](https://frederick.cancer.gov)) and Adjunct Professor in Bioinformatics, Hood College
               
**Supporting materials:** [Tutorial](https://github.com/ravichas/AMPL-workshop-2) and 
[AMPL: A Data-Driven Modeling Pipeline for Drug Discovery](https://pubmed.ncbi.nlm.nih.gov/32243153/)

The second workshop on September 14 will demonstrate three preliminary in-silico drug discovery topics:
* data ingestion
* cleaning/tidying
* curation on AMPL

Note: This session will be 90 minutes and will use Google COLAB notebooks (compatible to Jupyter notebooks) for demonstration. Please see the outline below:

Notebook-1: Ingestion, Cleaning and Exploratory Data Analysis(EDA) of Binding Assay Data (30 minutes)  
* Issues associated with data ingestion and curation (data sources: Drug Data Commons; ChEMBL and ExCAPE-DB)  
* Exploratory data analysis of the ingested datasets
* Standardization of outcome units such as IC50 (etc. um to nM)
* Data visualization and comparison

Notebook-2: Standardization of SMILES, Featurization and Compound Overlap/Diversity using a Python Jupyter Notebook (30 minutes)

* Compound overlap
* SMILES standardization
* Explore compound diversity using featurization and Tanimoto distance
* Create plots/heatmaps for analysis
 

Notebook-3: Curate, Merge Datasets to Create the Final ML-ready Dataset (30 minutes)
* Removal of duplicates
* Filter extreme data
* Merge the DTC, ChEMBL, and ExCAPE-DB datasets to create a curated dataset
* Data curation on the merged data
* Creation of ML-ready dataset


To learn more about the software, visit the AMPL GitHub repository at this [link](https://github.com/ATOMconsortium/AMPL)

**Questions?** Contact the [NCI Data Science Learning Exchange](mailto:NCIDataScienceLearningExchange@mail.nih.gov)
