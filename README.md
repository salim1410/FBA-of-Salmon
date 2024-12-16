# Systems Biology Project: Metabolic Adaptation in Atlantic Salmon

## Introduction
This project investigates the metabolic responses of Atlantic salmon to temperature stress, focusing on the identification and optimization of reaction fluxes contributing to reduced growth at higher temperatures. By leveraging a systems biology approach, we aim to propose modifications that restore or enhance growth performance under warmer conditions.

---

## Background
Climate change and environmental fluctuations present significant challenges to aquatic species, particularly in their physiological adaptations. Using gene expression data from the study _"Transcriptional responses to temperature and low oxygen stress in Atlantic salmon studied with next-generation sequencing technology"_ (BMC Genomics, 2013), we analyzed enzymatic changes under temperature stress.

### Goal
To identify specific reaction fluxes that hinder growth under elevated temperatures and propose modifications to improve growth at these conditions.

---

## Problem Statement
Identify the reaction fluxes responsible for growth inhibition at higher temperatures and propose engineered adjustments to restore optimal growth.

---

## Methodology

### Input
1. **Gene Expression Data**
   - Collected at 19°C and compared with data at 12°C to identify upregulated and downregulated genes.
2. **SALARECON Model**
   - A genome-scale metabolic model for Atlantic salmon focusing on energy, amino acid, and nucleotide metabolism.
3. **Gene-Annotated Enzymes**
   - Mapping gene expression data to identify enzymes involved in temperature-specific responses.

### Analysis
- Gene data mapping from Ensembl to convert gene IDs to names for SALARECON integration.
- Identification of enzymes from differentially expressed genes.
- Flux Balance Analysis (FBA) using Cobrapy to adjust fluxes based on upregulated and downregulated enzymes.

### Key Steps
1. **Gene-Enzyme Mapping**
   - Extract enzyme-associated genes from gene expression data.
   - Identify enzymes upregulated or downregulated at 19°C.

2. **Model Optimization**
   - Increase the lower flux bound for upregulated enzymes to simulate improved thermal tolerance.
   - Decrease the upper flux bound for downregulated enzymes to adapt to thermal sensitivity.

3. **Simulation**
   - Predict optimized growth performance at elevated temperatures using the SALARECON model.

---

## Results

### Identified Enzymes
**Upregulated Enzymes (Higher Thermal Tolerance):**
- **ALDH6A1**: Involved in methylmalonate semialdehyde metabolism.
- **TD02**: Critical in tryptophan metabolism.
- **GRHPR**: Functions in glyoxylate and hydroxypyruvate reduction.

**Downregulated Enzymes (Thermal Sensitivity):**
- **SARDH**: Catalyzes sarcosine oxidation.
- **DPYS**: Involved in pyrimidine catabolism.
- **PIPOX**: Affects L-lysine catabolism to acetyl-CoA.

### Optimized Model
- The SALARECON model was modified based on enzyme flux adjustments.
- Predicted growth rates improved under simulated warmer conditions.

---

## Data Sources
1. **Gene Expression Data**
   - _"Transcriptional responses to temperature and low oxygen stress in Atlantic salmon studied with next-generation sequencing technology"_ (BMC Genomics, 2013).

2. **Metabolic Model**
   - _"SALARECON connects the Atlantic salmon genome to growth and feed efficiency"_ (PLOS Computational Biology, 2016).
   - Model repository: [SALARECON GitHub](https://github.com/project/SALARECON).

3. **Genome Data**
   - Lien et al., 2016. _"The Atlantic salmon genome provides insights into rediploidization"_ (Nature).

---

## Tools and Resources
- **Programming**: Python, Cobrapy, Jupyter Notebook.
- **Data Processing**: Ensembl gene annotations, CSV merging, and case sensitivity adjustments.
- **Modeling**: Flux Balance Analysis (FBA) to simulate growth performance.

---

## Project Workflow

1. **Data Cleaning and Preparation**
   - Matched SALARECON gene IDs to names using genome data.
   - Merged gene expression data for 19°C and 12°C.

2. **Model Refinement**
   - Adjusted flux bounds for enzymes based on differential gene expression.

3. **Optimization**
   - Simulated growth rates using an optimized metabolic model.

---

## Future Directions
- Modify essential genes (e.g., downregulated under thermal stress) through genetic engineering to enhance thermal tolerance.
- Explore further metabolic pathways to optimize salmon growth under climate-induced temperature variations.

---

## Citation
If you use this project or its findings, please cite the following works:
- Olsvik, P.A., et al. (2013). _Transcriptional responses to temperature and low oxygen stress in Atlantic salmon studied with next-generation sequencing technology_. BMC Genomics.
- Lien, S., et al. (2016). _The Atlantic salmon genome provides insights into rediploidization_. Nature.

---
