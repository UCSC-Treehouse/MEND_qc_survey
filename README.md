# MEND_qc_survey

This code analyzes the composition of RNA-Seq datasets generated from 2179 tumors in 48 cohorts by counting the Mapped, Exonic, Non-duplicate (MEND) reads. It generates the figures and calculations reported in https://doi.org/10.1101/716829v1. The abstract for the manuscript follows.


## Background
The reproducibility of gene expression measured by RNA sequencing (RNA-Seq) is dependent on the sequencing depth. While unmapped or non-exonic reads do not contribute to gene expression quantification, duplicate reads contribute to the quantification but are not informative for reproducibility. We show that Mapped, Exonic, Non-duplicate (MEND) reads are a useful measure of reproducibility of RNA-Seq datasets utilized for gene expression analysis.

## Findings
In bulk RNA-Seq datasets from 2179 tumors in 48 cohorts, the fraction of reads that contribute to the reproducibility of gene expression analysis varies greatly. Unmapped reads constitute 1-77% of all reads (median (med.) 3%; IQR 3%); duplicate reads constitute 3-100% of mapped reads (med. 27%; IQR 30%); and non-exonic reads constitute 4-97% of mapped, non-duplicate reads (med. 25%; IQR 21%). Mapped, Exonic, Non-duplicate (MEND) reads constitute 0-79% of total reads (med. 50%; IQR 31%).

## Conclusions
Since not all reads in a RNA-Seq dataset are informative for reproducibility of gene expression measurements, and the fraction of reads that are informative varies, we propose reporting a dataset's sequencing depth in MEND reads, which definitively inform the reproducibility of gene expression, rather than total, mapped or exonic reads. We provide a Docker image containing 1) the existing required tools (RSeQC, sambamba and samblaster) and 2) a custom script. We recommend that all RNA-Seq gene expression experiments, sensitivity studies and depth recommendations use MEND units for sequencing depth.
