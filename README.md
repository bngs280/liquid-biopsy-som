# ctDNA-som: Somatic Variant Calling Pipeline for Liquid Biopsy

![Nextflow](https://img.shields.io/badge/Nextflow-%E2%89%A50.32.0-brightgreen)
![Docker](https://img.shields.io/badge/Docker-%E2%89%A520.10.0-blue)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A **high-sensitivity** Nextflow & Docker pipeline for detecting somatic variants (SNVs, Indels, CNVs) in circulating tumor DNA (ctDNA/cfDNA). Optimized for low-frequency variants down to **0.1% VAF** with UMI error correction.

## Key Features
- ✅ **Ultra-sensitive calling**: Duplex-UMI support for noise suppression
- ✅ **Flexible modes**: Tumor-naive (plasma-only) & tumor-plasma paired analysis
- ✅ **Biomarkers**: TMB, MSI, and CNV detection
- ✅ **Validated** on [ICGC](https://dcc.icgc.org/) ctDNA data (90% sensitivity @ 0.5% VAF)
- ✅ **Portable**: Dockerized for reproducibility; AWS/GCP compatible

## Quick Start
### Prerequisites
- Nextflow (`>= 22.10.0`)
- Docker (`>= 20.10.0`)

### Run Pipeline
```bash
nextflow run ctdna-som/main.nf \
  --input samplesheet.csv \
  --outdir results \
  -profile docker
