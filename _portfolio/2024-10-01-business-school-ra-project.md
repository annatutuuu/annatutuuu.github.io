---
title: "Research Assistant - St Andrews Business School"
subtitle: "Supervisor: Dr Sapnoti Eswar & Dr Irina Merkurieva"
collection: portfolio
section: undergrad_research
permalink: /portfolio/business-school-ra-project/
date: 2024-10-01
project_period: "Sep 2024 - Dec 2024"
header:
  teaser: projects/business-school-ra.svg
excerpt: "Built a Python pipeline for entity resolution between LinkedIn employment data and patent records using fuzzy matching and company name normalization."

---
## Overview
Independent research project merging LinkedIn employment data with patent inventor and assignee records to study the relationship between firm employees and patent activity.

## Key Components
### Data Pipeline
- Developed a Python-based fuzzy-matching pipeline to link three datasets:
  - LinkedIn firm/employee data
  - Patent Inventors data
  - Patent Assignees data
- Automated merging and matching based on user-specified columns.

### Company Name Normalization
- Implemented a `cmpny` module with `extract_name_parts` to standardize company names before matching.
- Added handling for:
  - Entity types (`INC`, `LLC`, `CORP`)
  - Common industry words (`TECHNOLOGY`, `SYSTEMS`, `ENERGY`)
  - Whitespace normalization

### Configurable UI
- Built `settings.py` to allow users to:
  - Input file paths
  - Select matching columns
  - Set similarity thresholds
- Saved configuration to `settings.json` for reproducibility.

### Probabilistic Record Linkage
- Applied the `recordlinkage` library for fuzzy matching across firm and worker name fields.
- Used configurable thresholds to balance match accuracy and computational efficiency.

### Scalability
- Designed the workflow for large CSV datasets with flexible column configurations.
- Kept the pipeline adaptable to matching tasks beyond the original use case.

## Links
- [Code (GitHub/GitLab)](https://github.com/Rusteal/inventions_fuzzy_matching)

