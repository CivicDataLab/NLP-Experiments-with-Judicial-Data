# Studying the implementation of POCSO law
In this experiment, we explored the use of [OpenNyAI](https://opennyai.org/) in extracting relevant POCSO Sections from judgement copies and how it can enrich the existing metadata available on [eCourts](https://ecourts.gov.in/ecourts_home/) portal. 

## Step-1: Converting PDFs into TXT format
The POCSO judgements available on eCourts are all not machine readable. The notebook [PDF_Txt_Conversion](https://github.com/CivicDataLab/NLP_Justice/blob/main/POCSO/PDF_Txt_Conversion.ipynb) helps in converting them into TXT format, which is the input format for OpenNyAI algorithms.

## Step-2: Selecting POCSO cases from Assam for the experiment
We filtered 51 judgements from the 1764 POCSO judgements available in Assam. The criteria for the filtering is discussed here: [POCSO_filter](https://github.com/CivicDataLab/NLP_Justice/blob/main/POCSO/POCSO_filter.ipynb)

## Step-3: Finding POCSO provisions for these 51 judgements:
- Summarise the 51 judgements using OpenNyAI. 5 types of summaries are produced, namely: PREAMBLE, facts, issue, ANALYSIS, and decision.
- Find the POCSO provision in each of the summaries using key word search.
- Find the POCSO provision in the metadata for these 51 judgements.

All these steps are executed in this notebook - [OpenNyAI_Summarize](https://github.com/CivicDataLab/NLP_Justice/blob/main/POCSO/OpenNyAI_Summarize.ipynb)


# Results

Link to the final dataset with POCSO provisions identified both using OpenNyaI and metadata: [pocso_provisions_51judgements.csv](https://github.com/CivicDataLab/NLP_Justice/blob/main/POCSO/Results/pocso_provisions_51judgements.csv)

The inferences are shared in this blog: Link

All the 51 judgements and their OpenNyAI summaries are available in this [folder](https://github.com/CivicDataLab/NLP_Justice/blob/main/POCSO/POCSO_Experiment_Judgements) for review.