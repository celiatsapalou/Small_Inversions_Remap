# Export regions with high mismatch rate, Remap regions with NGMLR, call inversions

## Overview
Snakefile to export regions with high mismatch rate using pysamstats, remap selected regions with NGMLR, and call inversions with Delay


### Prerequisites
- Snakemake
- pysamstats 
- Python 3.10.8
- R 4.2.0 or higher
- bedtools
- samtools