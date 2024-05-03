# Project: Export Regions with High Mismatch Rate, Remap with NGMLR, Call Inversions

## Overview
This Snakefile exports regions with high mismatch rates using pysamstats, remaps the selected regions with NGMLR, and calls inversions with Delly.

### System requirement
- Snakemake
- pysamstats 
- wally
- Python 3.10.8
- R 4.2.0 or higher
- bedtools
- samtools
- Delly


## Input and Output of the Pipeline / Reproduction instructions 

The `input` files are the cram files for each sample in the 1OOO Genome project sequenced by our ONT effort, and the `output` files are bed files for each sample, containing the candidate inversion regions.

#### `Snakefile_cram_remap`
This Snakefile is used for remapping sample CRAM files to detect small inversions. It includes steps for preprocessing, remapping, post-processing, and calling inversions.

#### `base.yaml`
Configuration file for the Snakefile that specifies parameters and paths used in the Snakefile.

#### `sniffles.inversion.bed`
Example BED file containing the format required for running the `wally_dotplots.sh` script. This file lists candidate inversion coordinates, along with carrier and non-carrier samples for each location.

#### `wally_dotplots.sh`
Shell script for generating dotplots from sequence alignments, to visualize candidate inversion locations from the candidate inversion bed file.
