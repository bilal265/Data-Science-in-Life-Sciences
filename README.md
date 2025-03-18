# Data-Science-in-Life-Sciences

# Comprehensive Multi-Omics Analysis of Invasive Lobular and Ductal Breast Cancer

## Project Overview

This repository contains a multi-omics analysis of invasive lobular carcinoma (ILC) and invasive ductal carcinoma (IDC) breast cancer subtypes. The project was conducted as part of the **Data Science in the Life Sciences S23** course at Free University Berlin.

## Table of Contents

- [Abstract](#abstract)
- [Introduction](#introduction)
- [Methods](#methods)
- [Results](#results)
- [Discussion](#discussion)
- [Enrichment Analysis](#enrichment-analysis)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [References](#references)

---

## Abstract

Invasive lobular carcinoma (ILC) is the second most common histologic subtype of invasive breast cancer. This study analyzed 817 breast cancer samples (127 ILC, 490 IDC, and 88 mixed IDC/ILC) and identified genetic markers and molecular features enriched in ILC. Notably, PTEN, TBX3, and FOXA1 mutations were found as ILC-enriched characteristics. Additionally, FOXA1 mutations were associated with enhanced FOXA1 expression and activity. Differences in ER activity between ILC and IDC were also identified. This comprehensive molecular atlas offers insights into the unique biology of ILC and highlights potential clinical treatment opportunities.

---

## Introduction

Invasive lobular carcinoma accounts for approximately 10–15% of all breast cancer cases and is characterized by the loss of E-cadherin expression, resulting in its hallmark discohesive growth pattern. The infiltrative nature of ILC complicates both clinical examination and imaging, while also presenting distinct patterns of metastatic dissemination. This project leverages The Cancer Genome Atlas (TCGA) to provide a detailed analysis of genetic and molecular differences between ILC and IDC.

---

## Methods

- **Dataset:** TCGA Breast Invasive Carcinoma data (n=1,098 patients).
- **Data Types:** Copy number variation (CNV), gene expression (RNA-Seq), mutation data, and protein expression (RPPA).
- **Tools Used:** R (curatedTCGA package), Python (Pandas, Seaborn), and machine learning algorithms for imputation and clustering.

### Data Processing:
- **Data Cleaning:** Removed samples with >30% missing data.
- **Feature Selection:** Focused on ILC and IDC subtypes.
- **Normalization:** Log-transformed RNA-Seq data, standardized CNV data, and used MissForest for missing value imputation in RPPA data.
- **Correlation Analysis:** Explored relationships between CNV and gene expression data.

### Modeling Techniques:
- **Kaplan-Meier Survival Analysis** to investigate survival probabilities based on nodal stage.
- **Non-negative Matrix Factorization (NMF)** for dimensionality reduction and multi-omics data integration.
- **Clustering** based on NMF components to identify subgroups among patients.

---

## Results

- **Molecular Markers:** Identified key mutations enriched in ILC, including PTEN and FOXA1.
- **Subtype Discovery:** Defined three transcriptional subtypes of ILC associated with distinct survival outcomes.
- **Mixed Tumors:** Mixed IDC/ILC cases were molecularly classified as either ILC-like or IDC-like, with no hybrid subtype detected.
- **Survival Analysis:** Patients with reactive-like ILC tumors exhibited better survival than those with proliferative ILC tumors.

### Kaplan-Meier Analysis
- The survival curves revealed significant differences between nodal stage groups in terms of survival probabilities.

### Correlation Analysis
- Identified genes showing strong correlations between CNV and gene expression, e.g., CACNA1H and CACNA2D1.

---

## Enrichment Analysis

Performed enrichment analysis using the "GO_Biological_Process_2018" database:
- **Significant Pathways Identified:**
  - Acute inflammatory response
  - Regulation of protein phosphorylation
  - Regulation of chemotaxis

The analysis revealed that genes associated with NMF component 1 are involved in crucial immune and signaling pathways, supporting their role in cancer progression.

---

## Visualizations
![image](https://github.com/user-attachments/assets/e4cab465-c48d-4a47-915c-1b8966084021)
- **Figure 1:** Distribution of breast cancer subtypes and their recurrent mutations.

- ![image](https://github.com/user-attachments/assets/68eba636-23a3-4bd5-af53-6ee9a209a907)
- **Figure 2:** Kaplan-Meier survival plot for nodal stage groups

- ![image](https://github.com/user-attachments/assets/d1e97993-59e0-4537-8584-c4a64838bc1a)
- **Figure 3:** Correlation boxplot for CNV and gene expression.

- ![image](https://github.com/user-attachments/assets/a1bfad00-175e-4a53-bc40-b496a0f11ccf)
- **Figure 4:** Joint NMF scatterplot showing patient clusters colored by histological subtype and estrogen receptor status.

- ![image](https://github.com/user-attachments/assets/ee2c3fae-56bf-4099-b5c6-8937c0c58932)
- **Figure 5:** Heatmap of NMF components highlighting omics co-regulation patterns.

- ![image](https://github.com/user-attachments/assets/25fd2c98-5ab7-47e5-9162-64c26c6371a4)
- **Figure 6:** This shows expression of the genes associated with the first factor are significantly overlapping the 
biological pathways, such as acute inflammatory response, regulation of protein phosphorylation, and the regulation 
of chemotaxis



## Discussion

This study highlights significant molecular distinctions between ILC and IDC breast cancers:
- **ILC exhibits enriched mutations** in PTEN, TBX3, FOXA1, and lacks E-cadherin.
- **Molecular stratification** of mixed tumors showed they align with either IDC or ILC, but not both.
- **Clinical Implications:** Findings can help design more personalized treatment approaches for ILC patients, as well as guide future research on ILC-targeted therapies.

---

## Conclusion

This project provides a comprehensive multi-omics analysis of breast cancer subtypes, delivering:
- A deeper understanding of ILC biology,
- Insight into survival outcomes based on nodal stage and tumor subtype,
- A framework for future clinical applications and therapeutic developments targeting ILC.

---

## References

- Akbani et al., Nat. Commun. (2014)
- Arpino et al., Breast Cancer Res. (2004)
- Cancer Genome Atlas Research Network (2012, 2014)
- Parker et al., J. Clin. Oncol. (2009)
- Wilkerson & Hayes, Bioinformatics (2010)
- Zou & Hastie, J. R. Stat. Soc. (2005)

---

## Authors

- **Muhammad Bilal Ashraf**    
  Free University Berlin  
  [ashrab97@zedat.fu-berlin.de](mailto:ashrab97@zedat.fu-berlin.de)  

---

> This README summarizes the project and findings based on TCGA breast cancer data. For further details, see the full report and associated code.

