# Integrative Multi-Omics Landscape of Lung Cancer: Cross-Compartment Molecular Concordance

> **Project Status:** 🔒 *Source code and specific final model parameters are currently restricted pending peer-reviewed publication. This repository serves as a technical showcase of methodology and multi-omics integration capabilities.*

## 🧬 Executive Summary
This project investigates the **"Tumor-Imprint" hypothesis**: the degree to which circulating nucleic acids (cfRNA/cfDNA) faithfully recapitulate the structured molecular architecture of primary tumors. By integrating transcriptomic, genomic, and epigenomic layers, I developed a biologically grounded framework for liquid biopsy biomarker discovery.

## 📊 Performance Highlights
* **Diagnostic Power:** Final 9-gene signature achieved an **AUC of 0.965** ($p < 10^{-32}$).
* **Clinical Utility:** High-risk stratification yielded a **Hazard Ratio (HR) of 1.55** ($p = 0.0028$) in external validation ($n = 601$).
* **Biological Fidelity:** Identification of a 53-gene "Mirror Signature" with high cross-compartment correlation.

## 🛠️ Multi-Omics Integration Framework

### 1. Transcriptomic Landscape (Tissue vs. cfRNA)
I identified a conserved transcriptomic echo in circulation. While solid tumors exhibit high DEG burden (1,651 genes), the cfRNA profile (416 genes) represents a selective, systemic signature.

| Comparison Cohort | Total DEGs | Upregulated ($log_{2}FC > 2$) | Downregulated ($log_{2}FC < -2$) |
| :--- | :---: | :---: | :---: |
| **Solid Tumor vs. Healthy** | 1,651 | 1,312 | 339 |
| **Lung Cancer cfRNA vs. Healthy** | 416 | 106 | 310 |

### 2. Composite Biomarker Prioritization
To move beyond simple statistical significance, I implemented a **Weighted Composite Scoring Framework** ($0.6 \times AUC + 0.4 \times r$) to prioritize genes that are both diagnostically accurate and biologically concordant.

| Top Candidate | Diagnostic AUC | Mirror Fidelity ($r$) | Composite Score |
| :--- | :---: | :---: | :---: |
| **IGFL2** | 0.818 | 0.704 | **0.876** |
| **TMEM179** | 0.720 | 0.820 | **0.847** |
| **DDX3ILA1** | 0.640 | 0.903 | **0.818** |

### 3. Multi-Layer Regulatory Synergy
The signature is supported by coordinated alterations across the central dogma:
* **Genomics:** Concentrated genomic instability in mucin regions (**MUC5AC**, **MUC3A**, **MUC2**).
* **Epigenomics:** Widespread hypomethylation in transport/signaling hubs (e.g., **PSAT1**, **SLC24A2**, **ADRA1A**).
* **Functional Pathways:** GO/KEGG analysis confirmed dominant dysregulation in **Calcium/Sodium Ion Homeostasis**.

## 🧪 Technical Stack & Validation
* **Bioinformatics:** `DESeq2` for DEGs, `Metilene` for Methylation, `FreeBayes` for Variant Calling.
* **ML & Stats:** Composite Scoring, Cox Proportional Hazards, Kaplan-Meier Analysis.
* **External Validation:** Rigorous testing against the **TCGA-LUAD** cohort ($n = 601$).

## 📁 Repository Contents
* `figures/`: Anonymized high-resolution UMAPs, Volcano plots, and ROC Curves.
* `tables/`: Comprehensive DEG lists and mutation density profiles.

## 🤝 Professional Contact
For technical inquiries regarding the multi-omics integration framework or collaboration:
**[Your Name]** | [Your LinkedIn Link] | [Your Email]
