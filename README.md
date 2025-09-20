# 1_B-cell-Epitope-Prediction
Machine learning and computational tools for B-cell epitope prediction.

# B-cell Epitope Prediction using ML
This repository provides a computational framework for the **prediction and characterization of linear B-cell epitopes** from protein sequences.  
The workflow integrates sequence-derived physicochemical, structural, and immunological descriptors to support downstream analysis in **vaccine design, immunodiagnostics, and therapeutic development**.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Input Format](#input-format)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)
- [Requirements](#requirements)
- [License](#license)

---

## Overview
B-cell epitopes are regions of antigens recognized by antibodies, playing a central role in adaptive immune responses.  
This repository contains Python scripts for calculating **multiple sequence-based features** relevant to epitope prediction, leveraging tools from **BioPython** and **Pandas**.  

The computed features can be used for:  
- Epitope mapping and ranking  
- Pre-processing for machine learning pipelines  
- Comparative analysis of antigenic determinants  

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Key Features
The framework computes a diverse set of descriptors, including but not limited to:

- Hydrophilicity and hydrophobicity indices  
- Surface accessibility and beta-turn propensity  
- Antigenicity and immunogenicity scores  
- Molecular weight and amino acid composition  
- Net charge (at physiological pH) and isoelectric point (pI)  
- Instability index and flexibility parameters  
- Aliphatic index, aromaticity, and extinction coefficient  
- Virulence and adhesion probability estimates  

All descriptors are consolidated into a single **Excel file** for further analysis.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Input Format
- Input is provided as an **Excel file** (`Linear_B-cell.xlsx`).  
- The file must contain a column named **`Sequence`**, with amino acid sequences composed of standard residues (`ACDEFGHIKLMNPQRSTVWY`).  

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Installation
Clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/1_B-cell-Epitope-Prediction.git
cd 1_B-cell-Epitope-Prediction
pip install -r requirements.txt
pip install biopython pandas numpy joblib
import pandas as pd

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Read file:
df = pd.read_excel('/content/drive/My Drive/Colab Notebooks/Linear_B-cell.xlsx')
# Compute features
df.to_excel('b_cell_epitopes_with_features.xlsx', index=False)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Output
b_cell_epitopes_with_features.xlsx
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Requirements:
Python ≥ 3.8
Biopython
Pandas
NumPy
Joblib
