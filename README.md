# Partitioning methods for phylogenomic studies of UCE markers 

The accuracy of phylogenetic inferences often depends on choosing an appropriate model of molecular evolution. In Tagliacollo & Lanfear (submitted), we evaluated the performance of two new partitioning methods for phylogenomics studies of UCES, and conclude that automatic selection of partitions through the SWSC-EN method considerably improves model-fit and parameter estimates. This repository contains scripts to run the SWSC-EN method on your own alignments. For more information about the method, please see the accompanying paper, and the [repository for replicating the analyses in that paper](https://github.com/Tagliacollo/PartitionUCE). 

# Quick Start

Use Python 3.6.x or higher

```python SWSCEN.py input.nex output_folder```

# Installation

## 1. Install Python and its dependencies

SWSC-EN needs Python 3.6.x or higher (but not 2.x!) and some additional libraries to run on personal computers. The simplest way to set this up is to install the Anaconda Python distribution, which can be downloaded from here:

[http://continuum.io/downloads](http://continuum.io/downloads)   

Follow the link for the Python 3.6 graphical installer, then open it and follow the prompts. You need to make sure that you have version 4.4.0 or higher of the Anaconda Python distribution. In addition, install the following dependencies:

[biopython](https://pypi.python.org/pypi/biopython)

[numpy](https://pypi.python.org/pypi/numpy)

[pathlib2](https://pypi.python.org/pypi/pathlib2/) 

[tqdm](https://pypi.python.org/pypi/tqdm)

which you can do with the following commands after installing Anaconda Python 3.6:

```
conda install biopython
conda install numpy
conda install pathlib2
conda install tqdm
```

## 2. Download SWSC-EN

1. Download the latest version of SWSC-EN repository [here](https://github.com/Tagliacollo/PFinderUCE-SWSC-EN/archive/master.zip)

2. Double-click the .zip file, and it will automatically unzip. You will get a folder called 'PFinderUCE-SWSC-EN-master'

3. Move it to wherever you want to store PFinderUCE-SWSC-EN (e.g. in /Applications)
	
## 3. Run SWSC-EN

The instructions below describe how to run the `example_input/example_dataset.nex` using SWSC-EN method. This is a nexus DNA alignment with 15 concatenated UCEs 

1. Open Terminal (on Macs), or a command prompt (on windows) 

2. Type “python“ followed by a space (remember, it needs to be python 3.6.x or higher)

3. Drag and drop the `SWSCEN.py` script onto your terminal or commmand prompt (the script is here `PFinderUCE-SWSC-EN-master/py_script/SWSCEN.py`)

4. Type another space

5. Drag and drop the input file `example_input/example_dataset.nex` onto your terminal

6. Hit Enter/Return to run PFinderUCE-SWSC-EN

## Input File

SWSC-EN needs only a single input file, which is a concatenated nexus alignment (.nex) comprised of UCE markers and including charsets with the locations of the UCEs (example input is in the `/example_input` folder of this repository).


## Output Files

By default the output is stored in the same folder as the input file. If you want to change this, you can just add another argument at the commandline, defining the output folder you'd like to use.

There are two outputs: 

1. A PartitionFinder 2 configuration file (.cfg) to be used as the input file for [PartitionFinder 2](https://academic.oup.com/mbe/article/34/3/772/2738784/PartitionFinder-2-New-Methods-for-Selecting)

2. A csv file (.csv) with values of entropy (SWSC-EN) for each site of the UCEs. 

Example output is provided in the ```example_output/``` folder.
