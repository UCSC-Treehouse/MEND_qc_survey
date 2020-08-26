# MEND_qc_survey

This code analyzes the composition of RNA-Seq datasets generated from 2179 tumors in 48 cohorts by counting the Mapped, Exonic, Non-duplicate (MEND) reads. It generates the figures and calculations reported in https://doi.org/10.1101/716829v1. The abstract for the manuscript follows.


## Background

The accuracy of gene expression as measured by RNA sequencing (RNA-Seq) is dependent on the amount of sequencing performed. However, some types of reads are not informative for determining this accuracy. Unmapped and non-exonic reads do not contribute to gene expression quantification. Duplicate reads can be the product of high gene expression or technical errors. 

## Findings

We surveyed bulk RNA-Seq datasets from 2179 tumors in 48 cohorts to determine the fractions of uninformative reads. Total sequence depth was 0.2-668 million reads (median (med.) 61 million; interquartile range (IQR) 53 million). Unmapped reads constitute 1-77% of all reads (med. 3%; IQR 3%); duplicate reads constitute 3-100% of mapped reads (med. 27%; IQR 30%); and non-exonic reads constitute 4-97% of mapped, non-duplicate reads (med. 25%; IQR 21%). Informative reads--Mapped, Exonic, Non-duplicate (MEND) reads--constitute 0-79% of total reads (med. 50%; IQR 31%). Further, we find that MEND read counts have a 0.22 Pearson correlation to the number of genes expressed above 1 Transcript Per Million, while total reads have a correlation of -0.05.

## Conclusions

Since the fraction of uninformative reads vary, we propose using only definitively informative reads, MEND reads, for the purposes of asserting the accuracy of gene expression measured in a bulk RNA-Seq experiment. We provide a Docker image containing 1) the existing required tools (RSeQC, sambamba and samblaster) and 2) a custom script. We recommend that all results, sensitivity studies and depth recommendations use MEND units.
