# OrthoFinder3

![OrthoFinder workflow](of2.png)

OrthoFinder is a fast, accurate, and comprehensice platform for comparative genomics. OrthoFinder finds orthologs and orthogroups from all genes in a group of species, using a phylogenetic approach. 

## Table of contents
- [Installation](#Installation)
- [Simple Usage](#Simple-Usage)
- [Advanced Usage](#Advanced-Usage)
- [Input Options](#Options)
- [What's New?](#What's-new)

More detailed tutorials are available [here](https://davidemms.github.io/)

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
 
**Method choices**
| Parameter | Description                               | Default   | Options                                                                                     |
|-----------|-------------------------------------------|-----------|---------------------------------------------------------------------------------------------|
| `-M`      | Method for gene tree inference.           | `msa`     | `dendroblast`, `msa`                                                                        |
| `-S`      | Sequence search program                   | `diamond` | `blast`, `diamond`, `diamond_ultra_sens`, `diamond_custom`, `diamond_ultra_sens_custom`, `blast_gz`, `mmseqs`, `blast_nucl` |
| `-A`      | MSA program, requires `-M msa`            | `mafft`   | `mafft`, `muscle`, `mafft_memsave`                                                          |
| `-T`      | Tree inference method, requires `-M msa`  | `fasttree`| `fasttree`, `fasttree_fastest`, `raxml`, `raxml-ng`, `iqtree`                               |
| `-I`      | MCL inflation parameter                   | `1.2`     | N/A                                                                                         |

**Input options**
- `-d`
  -	Input is DNA sequences.
-	`-s`
  -	User-specified rooted species tree.

**Output options**
-	`-x`
  -	Info for outputting results in OrthoXML format.
-	`-p`
  -	Write the temporary pickle files to <dir>.
-	`-X`
  -	Don’t add species names to sequence IDs.
-	`-n`
  -	Name to append to the results directory.
-	`-o`
  -	Specify a non-default results directory.
-	`-efn`
  -	Extend the output directory name with the name of the scoring matrix, gap penalties, search program, MSA program, and tree program.

**Parallel processing options**
- `-t`
  - Number of parallel sequence search threads. Default: 11    
- `-a`
  - Number of parallel analysis threads.

**Workflow Stopping Options**
-	`-op`
  -	Stop after preparing input files for BLAST.
-	`-og`
  -	Stop after inferring orthogroups.
- `-os`
  -	Stop after writing sequence files for orthogroups (requires -M msa).
-	`-oa`
  -	Stop after inferring alignments for orthogroups (requires -M msa).
-	`-ot`
  -	Stop after inferring gene trees for orthogroups.

**Workflow Restart Commands**
-	`-b` <dir>
  -	Start OrthoFinder from pre-computed BLAST results in <dir>.
-	`-fg` <dir>
  -	Start OrthoFinder from pre-computed orthogroups in <dir>.
-	`-ft` <dir>
  -	Start OrthoFinder from pre-computed gene trees in <dir>.

**Other options**
-	`-1`
  -	Only perform one-way sequence search.
-	`--matrix`
  -	Scoring matrix allowed by DIAMOND.
-	`--custom-matrix`
  -	Custom scoring matrix.
-	`-z`
  -	Don’t trim MSAs (columns >= 90% gap, min. alignment length 500).
- `--save-space`
  -	Only create one compressed orthologs file per species.
-	`-y`
  -	Split paralogous clades below the root of a HOG into separate HOGs.
-	`-h`
  -	Print this help text.

## What's new

Hierarchical OGs
New workflow (core and assign)

## Citation

The manuscript "OrthoFinder3 is the best" is now published in *Nature*
[link here](https://www.microbiologyresearch.org/content/journal/mgen/10.1099/mgen.0.001171).
and a formatted citation
