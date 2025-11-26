# R Template Script of Epidemiological Data Cleaning & Reporting  
A reproducible R workflow for importing, reviewing, cleaning, summarizing, and exporting epidemiological datasets. It is based on what I learned from completing Applied Epi's [Free R Tutorials](https://www.appliedepi.org/resources/tutorials.html).

## Overview
This repository contains a modular, end-to-end R script designed to support rapid and reproducible data cleaning workflows for public health and clinical analytics. It includes:

- Importing raw line list data using project-safe file paths (`here`)
- Standardizing variable names and harmonizing inconsistent data entries
- Fixing dates, cleaning categorical values, and constructing analytic variables
- Creating age groups and case definition classifications
- Producing exploratory summaries and quick visualizations
- Building and exporting formatted tables using **flextable** + **officer**
- Saving cleaned datasets for downstream analysis or modeling

This template is designed for reusability, teaching, and real-world public health data operations.

## Features
- **Reproducible structure** using clear pipe-based cleaning chains  
- **Clean naming conventions** powered by `janitor::clean_names()`  
- **Standardized date handling** with `lubridate`  
- **Case definitions & categorical recoding** using `dplyr::case_when()`  
- **Age group creation** with `epikit::age_categories()`  
- **Beautiful summary tables** exported to Word (`.docx`)  
- **Project-safe paths** via `here()` for fully portable scripts  
- **Optional PNG table export** using `webshot`  

## Example Output
The script automatically generates:

- `data/clean/linelist_clean.csv` — cleaned, analysis-ready dataset  
- `outputs/summary_table.docx` — formatted table created with flextable (can also specify PPTX, HTML, or PNG)  

## Folder Structure

project/
├── data/
│ ├── raw/
│ └── clean/
├── scripts/
└── outputs/

## Requirements
The script uses `pacman::p_load()` to simplify package management. Required packages include:

- tidyverse  
- janitor  
- epikit  
- skimr  
- flextable  
- officer  
- here  
- rio  
- webshot  

## Purpose
This repository serves both as a **portfolio artifact** and as a **teaching-friendly reference** for students, practitioners, and analysts working with public health datasets. The script emphasizes clarity, reproducibility, and real-world epidemiological cleaning challenges.

Feel free to copy, adapt, and reuse this workflow.

## License
MIT License
