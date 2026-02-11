<div align="left">

<h1 style="display: inline-block;">Rapid-CNS2-MNPflex-methylation-classifiers</h1>
</div>

## Overview

Rapid-CNS2 and MNPflex are brain/central nervous system (CNS) tumour methylation classifiers.

The fork is based on nanopore sequencing data (cfDNA and genomic DNA) that includes 5hmC and 5mC modifications (5mC_5hmC or 5mCG_5hmCG). The workflow merges BAM files, calls modifications using Rapid-CNS2 pipeline and generates an input data file for MNP-Flex tool. MNP-Flex API then generates a comprehensive molecular report based on data file.


The input file for MNP-Flex API should be a tab separated (BED) file containing column names: "chr" "start" "end" "coverage" "methylation_percentage" "IlmnID"
    IlmnID -- Illumina InfiniumID for probe  (Infinium MethylationEPIC Manifest Column Headings | Illumina Knowledge)


## Information:

https://github.com/areebapatel/Rapid-CNS2_nf/tree/main/scr

# Installations:

Requirements:
Nextflow (version 3.0.0 or later)
Conda, Docker or Singularity (optional, for containerized execution of tools)
Required input data:
Raw ONT POD5 data (for basecalling) or pre-aligned BAM files
Reference genome file (hg38 required)


nextflow:

https://www.nextflow.io/docs/latest/install.html

#install java:
sudo apt install openjdk-17-jre-headless


#download nextflow:

curl -s https://get.nextflow.io | bash

export CAPSULE_LOG=none

#make nextflow executeable:

chmod +x nextflow

#move nextflow to an executable path:

mkdir -p $HOME/.local/bin/
mv nextflow $HOME/.local/bin/

#Temporarily add this directory ($HOME/.local/bin/) to PATH:
export PATH="$PATH:$HOME/.local/bin"

#Add the directory to PATH permanently by adding the export command to your shell configuration file
~/.bashrc

#check installation success:
nextflow info


#Rapid-CNS2_nf repository:

$ git clone https://github.com/areebapatel/Rapid-CNS2_nf.git

nextflow.config

Installations Done.


