![course card](images/Dartmouth-course-card.png)
# Dartmouth College Bioinformatics for Beginners
---------------------------------

This module introduces you to the [Bash shell scripting language](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), working with common genomics file formats, and working within the terminal environment. In addition to the overview given in this README you will find 6 submodules in the forms of Jupyter notebooks that teach you different components of working with genomics data in the cloud. 

This module will cost you about $2.00 to run end to end, assuming you shutdown and delete all resources upon completion.

Watch this [Introduction Video](https://www.youtube.com/watch?v=VaZedZhjXrU&list=PLXaEJPtnQ4w7Vu7vqWbttBjUGrPp4Qa7b&index=1) to learn more about the module.

## Overview of Page Contents

+ [Data](#data)
+ [Troubleshooting](#troubleshooting)
+ [Funding](#funding)
+ [License for Data](#license-for-data)

## **Data**

The fasta files used in these lessons were pulled from NCBI using the accession number NC_045512.2 for the Severe acute respiratory syndrome coronavirus 2 isolate Wuhan-Hu-1, complete genome and the associated annotation file (GFF file). The fasta file containing the S11 ribosomal protein sequences from several proteobacteria was originally generated for **Shakya et al., 2017**.

The fastq files used in the Genomics file formats lesson were downloaded from the SRA database using accession number SRP033351. This RNA-seq dateset is described in **Himes et al, 2014**. This study investigates the mechanism by which glucocorticoids, a major treatment used in asthma care, prevent inflammation of airway smooth muscle cells (ASM). We subsequently downsized these datasets to streamline the tutorials and stored them in an AWS S3 Bucket. 

The fastq files downloaded from the SRA in submodule 6 **Putting It All Together** are downloaded from the SRA database using accession number SRR18435413. This sample was sequenced as part of a surveillance effort for SARS CoV2 infections in western New Hampshire. 

## **Troubleshooting**

Most of the errors that you might encounter are discussed in submodule 7 **Error mitigation**, however there are some additional errors you may run into that are not discussed in that lesson.

If your code is not being interpreted in the **Jupyter Notebook** as you would expect it to, you should ensure that you are specifying the BASH language within the code chunk. This can be done by writing `%%bash` at the top of the code chunk OR proceeding each command with `!`. Do not use both of these methods, select one and stick with it.

If your code is not being interpreted in the **terminal window** as you would expect, you should ensure you are not specifying the BASH language. The terminal by default expects that commands will be in BASH and you should not copy the `%bash` or `!` that proceed code chunks in the notebook into the terminal. 

If you're not seeing the kernel named __Python [conda env:root]__ you should ensure that the file `jupyter_config.json` is installed in the correct location. If this file exists in the right place you can try refreshing your notebook and giving the notebook a couple minutes to catch up. 

If you're trying to access software that you installed with a conda environment and you're getting a warning that the software does not exist, check that you have the conda environment loaded. In the **Jupyter Notebook** you should see the name of the conda environment in the top right corner of the module, for example *Python [conda env:test_env]*. In the **terminal window** you should see the name of the conda environment in parentheses proceeding the prompt, for example (test_env). 

## **Funding**

This resource was supported with funds from NIH grant P20GM130454 and NIH grant 3P20GM103506.

## **License for Data**

Text and materials are licensed under a Creative Commons CC-BY-NC-SA license. The license allows you to copy, remix and redistribute any of our publicly available materials, under the condition that you attribute the work (details in the license) and do not make profits from it. More information is available [here](https://tilburgsciencehub.com/about/#license).

![Creative commons license](images/licensebuttons.png)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)
