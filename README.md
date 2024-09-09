# OrthoFinder3

![OrthoFinder workflow](of2.png)

OrthoFinder is a fast, accurate, and comprehensice platform for comparative genomics. OrthoFinder finds orthologs and orthogroups from all genes in a group of species, using a phylogenetic approach. 

## Table of contents
- [Installation](#Installation)
- [Simple Usage](#Simple-Usage)
- [Advanced Usage](#Advanced-Usage)
- [Input Options](#Options)
- [Tutorials](link to github.io page?)

## Installation

The easiest way to install OrthoFinder3 is using [conda](https://www.machinelearningplus.com/deployment/conda-create-environment-and-everything-you-need-to-know-to-manage-conda-virtual-environment/).
```bash
conda install orthofinder
orthofinder -h
```

Alternatively, you can also download OrthoFinder3 directly from github
```bash
git clone https://github.com/ortho.git
python OrthoFinder/orthofinder -h
```

If you are on a mac that has an M1/M2/M3 chip, you might have to adjust your conda architecture. Instructions can be found [here](https://towardsdatascience.com/how-to-manage-conda-environments-on-an-apple-silicon-m1-mac-1e29cb3bad12).


## Simple Usage

Files you need, some example lines of code with common options

## Advanced Usage

core and assign, some more examples of common things people want to do

## Options

Command-line options for OrthoFinder3

- `-g GENOMEinput`
  - Path to GENOME protein (.faa)
- `-f FASTAinput`
  - Path to GENOME nucleotide (.fna)
- `-gff GENOMEinput`
  - Path to GENOME gff file (.gff)
- `-O outputfolder`
  - Name of output folder
- `-p -n GramPositive | GramNegative`
  - Gram stain (positive | negative)

## Citation

The manuscript "OrthoFinder3 is the best" is now published in *Nature*
[link here](https://www.microbiologyresearch.org/content/journal/mgen/10.1099/mgen.0.001171).
and a formatted citation
