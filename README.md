# STAR NGS Pipeline

This repository contains a shell script for running a complete NGS data analysis pipeline using several bioinformatics tools, including SRA Toolkit, Trimmomatic, FastQC, STAR, and featureCounts. The pipeline performs the following steps:

1. **Data Download**: Downloads NGS data from SRA.
2. **Quality Control**: Performs quality control on raw FASTQ files using FastQC.
3. **Trimming**: Trims adapters and low-quality bases from the reads using Trimmomatic.
4. **Mapping**: Maps the trimmed reads to a reference genome using STAR.
5. **Feature Counting**: Counts the features using featureCounts.

## Prerequisites

Before running the script, ensure that the following tools are installed on your system:

- [SRA Toolkit](https://github.com/ncbi/sra-tools)
- [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)
- [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
- [STAR](https://github.com/alexdobin/STAR)
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

## Output

The script generates several output files, including:

FASTQ files (SRR8986990_1.fastq, SRR8986990_2.fastq)

FastQC reports (SRR8986990_1_fastqc.html, SRR8986990_2_fastqc.html)

Trimmed FASTQ files (SRR8986990_1_trimmed_paired.fastq, SRR8986990_2_trimmed_paired.fastq)

BAM file (mappingAligned.sortedByCoord.out.bam)

Feature counts file (counts_file.txt)

## Notes
Ensure that the paths to the reference genome and GTF files are correct.

Modify the script as necessary to fit your specific data and analysis needs.
