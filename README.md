# Bacteriophage Genome Assembly Parameter Exploration

## Overview
This project investigates how k-mer size affects de Bruijn graph-based genome assembly quality using the Arthrobacter phage Sue2 sequencing dataset.

## Dataset
NCBI SRA Run:
SRR29518805

## Software
- MEGAHIT v1.2.9
- Conda
- matplotlib

## Assembly Commands

### k = 21
```bash
megahit -r SRR29518805.fastq -o output_k21 --k-list 21 -t 2 -m 0.3
```

### k = 31
```bash
megahit -r SRR29518805.fastq -o output_k31 --k-list 31 -t 1 -m 0.1
```

### k = 51
```bash
megahit -r SRR29518805.fastq -o output_k51 --k-list 51 -t 1 -m 0.1
```

## Results Summary

| k-mer | # contigs | N50 | total length |
|---|---|---|---|
| 21 | 38 | 27773 | 51442 |
| 31 | 29 | 42276 | 50707 |
| 51 | 19 | 42296 | 47160 |