# Intro to Bioinformatics on the Command Line for Google Cloud

## Overview of Page Contents

+ [Overview](#overview)
+ [Getting Started](#getting-started)
+ [Software Requirements](#software-requirements)
+ [Workflow Diagrams](#workflow-diagrams)

## **Overview**

This module teaches you how to interact with genomics files using the terminal interface in the cloud. Each lesson builds upon the skills and BASH code from the previous lesson using Jupyter notebooks. By the end of the module you should be familiar with the format of many genomics files, installing bioinformatics tools that analyze genomics data, and have an understanding of the process of building complex BASH code to work with genomics files.

## **Getting Started**

Included here are several submodules or tutorials in the form of Jupyter notebooks. The purpose of these submodules is to help users familiarize themselves with the cloud computing environment in the specific context of working with genomics data and software packages to analyze genomics data. These tutorials accomplish this by going step-by-step introducing users to the cloud environment, the terminal interface, the BASH coding language, genomics file formats, the conda software package manager, and methods for mitigating common coding errors. These lessons build familiarity with the terminal environment and set users up to begin working with their own datasets in the terminal environment. For additional technical details on interfacing with the cloud users should reference [NIH Cloud Lab README](https://github.com/STRIDES/NIHCloudLabGCP).

### Creating a Vertex AI Workbench Instance 

Follow the steps highlighted [here](https://github.com/NIGMS/NIGMS-Sandbox/blob/main/docs/HowToCreateVertexAINotebooks.md) to create a new Workbench instance in Vertex AI. Follow steps 1-8 and be especially careful to enable idle shutdown as highlighted in step 8. In step 7 in the Machine type tab, select n1-standard-4 from the dropdown box.

To use our module, open a new Terminal window from your new notebook instance and clone this repo using `git clone https://github.com/NIGMS/Fundamentals-of-Bioinformatics.git`. Navigate to the directory for this project. You will then see the notebooks in your environment.

Before you begin navigating the submodules you will need to enable extensions in the Jupyter notebook. To do this you can click on the puzzle piece icon ![enable extensions](images/extension.png) on the left most menu (down the side of the Jupyter notebook) and click on the red button that says **Enable**.  

## **Software Requirements**

All software needed for this module will be installed in the **Software management** lesson using the `env.yml` file included in this repository. Additionally, you will need access to a Jupyter Environment. Some notebooks will require access to the Google Cloud Platform Vertex AI environment. 

You can install all necessary requirements using the instructions in `env.yml`, but they will generally look like this:

```
name: test_env
channels:
- bioconda
dependencies:
- python= 3.9
- ipykernel
- fastqc
- multiqc
```

## **Workflow Diagrams**

![workflow diagram](images/updated_Dartmouth_AD.svg)

As seen in the image above, we will download sequence files from the Google bucket to our Vertex AI virtual machine. We will practice running BASH commands using the sequence files in the bucket, as well as get practice downloading sequence data from the SRA. Using the Conda package manager we will install and use FastQC, MultiQC, SRA tools, Spades, and Prokka to analyze data from the SRA. Lastly we will create a new Google bucket, and copy our analyzed data to the new bucket. We explain our submodules that execute these processes here:

+ Submodule 1, **Introduction to Terminal** introduces the Jupyter notebook format, the terminal window, the syntax of the BASH coding language, and the architecture behind cloud computing. 
+ Submodule 2, **Introduction to Cloud Computing** teaches you how to navigate through a terminal environment to access computational data, here we download all of the data to your Jupyter notebook instance from the Google bucket used for this module. 
+ Submodule 3, **Genomics File Formats** introduces three common genomics file formats as well as many bash commands for interacting with these file types in the terminal environment. If you would like to complete this module over two days this lesson is an excellent stopping point.
+ Submodule 4, **Beyond Basic BASH** begins with a reminder of all the BASH commands covered in earlier lessons and combine complex commands with a loop and BASH scripting to iterate over several files with a single command. 
+ Submodule 5, **Software Management** uses the Conda package manager to create and install environments where software can be installed. 
+ Submodule 6, **Putting It All Together** leverages all of the skills learned in earlier lessons to download data from the SRA, create a Conda environment for genome assembly and annotation, check the quality, assemble, and annotate a genome. Then create a Google bucket and write a finalized file set to the Google bucket. 
+ Submodule 7, **Error Mitigation** provides strategies for mitigating common coding errors.

### Gemini (Optional)

Generative AI is available for this tutorial in the form of Gemini if you would like to use it. To run it, please reference submodule05 or run the following code within a submodule notebook. 

```!pip install -q google-generativeai google-cloud-secret-manager
!pip install -q git+https://github.com/NIGMS/NIGMS-Sandbox-Repository-Template.git#subdirectory=llm_integrations
!pip install -q ipywidgets

import sys
import os
util_path = os.path.join(os.getcwd(), 'util')
if util_path not in sys.path:
    sys.path.append(util_path)

from gemini import run_gemini_widget, create_gemini_chat_widget 
from IPython.display import display

run_gemini_widget()
