# GRN Inference and Perturbation
Archive of bioinformatic approaches used in my MSc thesis. Leveraging publicly available single-cell genomics to create gene regulatory networks (GRNs) in an accessible and reproducible fashion. 

My research interest is in developmental neuroinformatics, but this workflow is applicable to any niche cell type of interest / gene of interest combo according to your research question!

## A story told in thirds

This repository can be viewed in roughly a three-part structure:

1. **Preprocessing of the single-cell RNA-seq and ATAC-seq datasets.** The housekeeping stuff! This includes quality control, dimension reduction (unsupervised ML), and manual annotation (establishing a "ground truth" for downstream analyses). 
2. **Gene regulatory network (GRN) synthesis and perturbation.** The fun stuff! Building, pruning, and evaluating the networks, and, if desired, simulating gene-of-interest (GOI) knockouts. 
3. **Benchmarking and validation**. The novel stuff! I also validate my GRNs with *in vivo* in-house datasets. My thesis asserts that rank-rank hypergeometric overlap (RRHO) is an apt and scalable metric to be evaluating the concordance-discordance ratio between GRN algorithms. 
This metric has been previously used in comparing differential gene expression, proteomic vs. transcriptomic analyses, and short- vs. long-read sequencing. RRHO is rank-based and threshold-free, and I want to convince more research groups to consider adding RRHO to their benchmarking suite. 

# REQUIREMENTS

Replicating this project requires high-performance computing (HPC). Personally, I used the allocation generously provided by UBC's ARC Sockeye. For Sockeye users, I used 1-2 base nodes, and seldom 1 medium node. Please see [their technical documentation for details](https://confluence.it.ubc.ca/spaces/UARC/pages/319206082/About+Sockeye#AboutSockeye-NodeSpecifications).

| Type | CPU | Total Cores | System Memory | Memory per Core | 
| ----------- | ----------- |----------- | ----------- |----------- |
| Base | 2 x Intel Xeon Gold 6230 (2.1GHz) | 40 | 192GB DDR4-2666 ECC | 4.8GB |
| Medium | 2 x Intel Xeon Gold 6230 (2.1GHz) | 40 | 384GB DDR4-2666 ECC	| 9.6GB	|

This project uses a combination of R and Python, in the form of RMarkdown vignettes and JupyterNotebooks, respectively. The desired packages for each step are built using Apptainer/Singularity. I have included the .def files in this repo for reference, but have replaced filepaths with dummy variables for obvious reasons. 

# CITATION

Ip, K. (2025). Revisiting the unipolar brush cell during cerebellar embryonic development through in silico perturbation (T). University of British Columbia. Retrieved from https://open.library.ubc.ca/collections/ubctheses/24/items/1.0450337

