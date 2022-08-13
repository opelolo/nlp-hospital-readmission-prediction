# Natural Language Processing of Hospital Notes to predict readmission of patients within 30 days of discharge
This is a Natural Language Processing project that predicts hospital readmission of patients within 30 days of discharge. The goal is to prioritize in-patients according to their need for care and reduce readmission for the same illness.

## Introduction
Data scientists would have had a hard time working on health records if technology had not advanced the manual way of collecting health notes in paper to the electronic health records used today. With the availability of data from electronic health records, data scientists can build models that will improve the health of patients and eventually improve personal medicine. This project is an implementation of the paper, Scalable and accurate deep learning with Electronic Health Records (https://arxiv.org/abs/1801.07860). In the paper, deep learning models were developed to predict mortality, unplanned readmission and long-length of stay from the medial records. In this note, I implemented unplanned readmission. 

## Dataset
We will be using the MIMIC-III (Medical Information Mart for Intensive Care III), a free hospital database. This database contains de-identified data from over 40,000 patients who were admitted to Beth Israel Deaconess Medical Center in Boston, Massachusetts from 2001 to 2012. In order to get access to the data for this project, you will need to request access at this link (https://mimic.physionet.org/gettingstarted/access/). There are restrictions on the data, therefore I will not be able to share the data

In this project, we will make use of the following MIMIC tables

* ADMISSIONS - a table containing admission and discharge dates (has a unique identifier HADM_ID for each admission)
* NOTEEVENTS - contains all notes for each hospitalization (links with HADM_ID)
This notebook assumes that ADMISSIONS.csv and NOTEEVENTS.csv were downloaded and placed in the same folder as this notebook. 

## Task
We have a task to predict 30-day unplanned readmission of patients who have been initially discharged from the electronic medical records. 

## Procedure
For this task, I followed the following procedures
1. Data cleaning: After gathering the data, I analyzed the admissions table and cleaned the data because there were missing values. Also, I cleaned the moteevents data and removed unnecessary stop words that were irrelevant
2. Word rating: I used Bag-of-words to prioritise the words needed for our prediction in the hospital notes

## References 
1. https://arxiv.org/abs/1801.07860
