# gaps2symbolic

## Summary
Converts gaps and regions with no coverage -from next generation sequencing experiments- to symbolic variants in vcf format, and adds them to the vcf file with the patient's observed variants. This makes it possible to analyse gaps and regions with no coverage as if they were variants. The annotation and prioritization of these symbolic variants, along the real ones, may point to false negative results.

## Background
It is not always possible to find a patient's molecular diagnosis after next generation sequencing. Among the many possible reasons for this, lack of coverage of target regions, harbouring the pathogenic variants, is one of them.

To address this possibility, gaps and regions with no coverage are converted to symbolic variants which are subsequently concatenated, in a vcf file, with real variants found in the patient.

## What the commands do
The commands in gaps2symbolic convert sequencing gaps, and regions with no coverage, to symbolic variants. The symbolic variants are then concatenated with real variants found in the patient. The resulting vcf file, combining real and symbolic variants, can then be annotated and analysed in search of genotypes suggesting an association with the phenotypes observed in the patient.


### Table of Contents
* [Software requirements](#software_requirements)
* [Required files for each sample](#required_sample_files)
* [Additional files required](#additional_files_required)
* [Installation](#installation)
* [Usage](#usage)

---
<a name="software_requirements"></a>
## Software requirements
- **bedtools**
- **bcftools**
- **samtools**


<a name="required_sample_files"></a>
## Required files for each sample
- gaps.csv file (e.g. **sample.gaps.csv**)
- PerTargetMetrics.txt (e.g. **sample.PerTargetMetrics.txt**)
- File with metadata for structural variants; it may be manually constructed or it may be obtained from an appropriate file (e.g., **sample.SV.vcf.gz**)
- vcf file with the real variants in the patient (e.g. **sample.vcf.gz**)


<a name="additional_files_required"></a>
## Additional files required
- Human genome reference sequence file, GRCh37 or GRCh38 (e.g., **Homo_sapiens.GRCh37.75.dna.primary_assembly.fa**)


<a name="installation"></a>
## Installation
Download and extract.

Two files should be available:

- README.md
- makeVcfFileWithSymbolicAndRealVariants.txt


<a name="usage"></a>
## Usage
Run the commands in **makeVcfFileWithSymbolicAndRealVariants.txt**

If the sample's files and the reference genome are in a different directory, their paths need to be provided.

