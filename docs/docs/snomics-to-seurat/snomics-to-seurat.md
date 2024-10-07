---
layout: doc
tool: true

title: Snomics-to-Seurat
author: Michael Thomas
description: A tool for converting Snomics multiomic output data to Seurat format with graph-based integration.
github: https://github.com/Mike-robiology/snomics_to_seurat
---

## Introduction

The raw output from snomics can be dificult to handle, for a custom analysis would first require 100s of lines of code to be written to convert the data into a format that can be used for analysis. Snomics-to-Seurat is an nextflow pipeling aims to simplify this process. It converts the output from snomics into a multiomic Seurat object and automating much of the quality control and further pre-processing steps.


## Installation

To install Snomics-to-Seurat, clone the repository and navigate to the project directory or if a member of the ukdrmultiomicsproject project the required files are already available in ukdrmultiomicsproject/.

```bash
git clone https://github.com/Mike-robiology/snomics_to_seurat.git
cd snomics_to_seurat
```

## Usage

Usage of the pipeline aims to be as simple as possible. It requires two essenstial steps:

- **Input data**
- **Set parameters**

### Input

The primary input to the pipeline is a CSV file containing a list of sequencing projects, a path to the metadata to include in the object - typically the samplesheet used in the snomics pipeline - and the path to the snomics output directory. The CSV file should be formatted as follows:

```csv
project_id,metadata_path,snomics_output_path
project1,/path/to/project1/metadata.csv,/path/to/project1/snomics/output
project2,/path/to/project2/metadata.csv,/path/to/project2/snomics/output
...
```

This projects can be merged into a single Seurat object or kept separate.

### Parameters

The pipeline requires a number of parameters, sensible defaults are provided in `nextflow.config` but can be changed as needed. These can be set using a config file or passed as command line arguments. The only required parameter is the input CSV file. 

- `--input` - The path to the input CSV file

To use a config file, create a file with the optional parameters (nextflow.config can be used as a template) and pass it to the pipeline using the `-c` flag.

### Example script

Here is an example script, a template is available in the repository.

```bash
#!/bin/bash
#PBS -l walltime=24:00:00
#PBS -l select=1:ncpus=1:mem=4gb

module load gcc
export NXF_OPTS='-Xms1g -Xmx4g'

cd $PBS_O_WORKDIR
export JAVA_HOME=/bin/jdk-17
export PATH=/bin/jdk-17/bin:$PATH
mkdir -p /rds/general/ephemeral/user/$USER/ephemeral/tmp/

nextflow run snomics_to_seurat/snomics_to_seurat.nf \
--input "samplesheet.csv"
```

### Output

The pipeline generates one main output. This is a Seurat object containing the merged and integrated data from the input csv. This object can be used for further analysis in R. It also produces a list of failed samples which do not meet the quality control criteria.


## Support

For any issues or questions, please refer to the [GitHub repository](https://github.com/Mike-robiology/snomics_to_seurat) or contact the authors.
