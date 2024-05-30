# 2024_Cryptococcus_Ssd1motifs

This repository contains an analysis of motifs in Cryptococcus neoformans mRNAs that are predicted to be bound by the Ssd1 binding protein.

Edward Wallace, Edward.Wallace@ed.ac.uk, 2024

# Contents

## H99-Ssd1-motifs.Rmd/.html

This file does all the analysis and plots the output. In R markdown format and html output.

Specifically, counting occurrences of the Ssd1-binding motif CNYTCNYT in mRNA annotations for C. neoformans H99 mRNA annotation accompanying Wallace et al (2020), https://doi.org/10.5281/zenodo.3627875 

## data_in

Input data: mRNA sequences in fasta format, copied from https://doi.org/10.5281/zenodo.3627875 

- H99_10p_up12dwn9_3UTRs.fa
- H99_10p_up12dwn9_5UTRs.fa
- H99_10p_up12dwn9_CDS.fa

## results_out

Results output from analysis: Motif counts per mRNA, figure, lists of enriched genes, GO search results.

- H99_CNYTCNYT_counts.txt - data frame of CNYTCNYT counts for each mRNA
- CNYTCNYT_cumdist_plot.png - plot of cumulative distribution of occurences per mRNA and per 5'UTR
- H99_id_list_CNYTCNYT_mRNA_80pc.txt - list of H99 ids for those in 80th percentile or above of counts per mRNA (i.e. 6 occurrences)
- H99_id_list_CNYTCNYT_mRNA_95pc.txt - similarly, 95th percentile of counts per mRNA (i.e. 10 occurrences)
- H99_id_list_CNYTCNYT_mRNA_80pc.txt - similarly, 80th percentile of counts per 5'UTR (i.e. 2 occurrences)
- H99_id_list_CNYTCNYT_mRNA_95pc.txt - similarly, 95th percentile of counts per mRNA (i.e. 4 occurrences)
- GOSlim_XX_CNYTCNYT_YY_ZZ.tsv - GO Slim results from FungiDB Release 68, May 24, of relevant H99_id_list, where:
  - XX is BP for Biological Process or CC for Cellular Component
  - YY is mRNA or 5UTR
  - ZZ is 80pc or 95pc for relevant percentile

