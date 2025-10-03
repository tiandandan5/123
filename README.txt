TCGA miRNA Analysis – Code & Reproducibility Package
====================================================

Overview
--------
This package accompanies the manuscript section:
"Computational analysis of The Cancer Genome Atlas (TCGA) identified highly expressed miRNAs in breast cancer."

It contains the analysis notebook, a minimal conda environment, example input data, and expected output,
so that reviewers can install and run the workflow end‑to‑end.

Contents
--------
- README.txt (this file)
- env/environment.yml (reproducible conda env)
- LICENSE.txt (license for code; default MIT)
- code/cfDNA-tdd.ipynb (Jupyter notebook with analysis)
- examples/example_input.csv (toy data to test the notebook)
- examples/expected_output.txt (expected results on the toy data)

Quick Start
-----------
1) Install Conda (Miniconda/Anaconda). Then create the environment:
   conda env create -f env/environment.yml
   conda activate tcga-mirna

2) Launch Jupyter and open the notebook:
   jupyter notebook code/cfDNA-tdd.ipynb

3) In the notebook, set `DATA_PATH` to point to real TCGA data or use the provided toy dataset in `examples/`.
   The notebook will generate summary tables and plots and print key miRNAs with their normalized counts.

Example Data & Expected Output
------------------------------
- examples/example_input.csv : toy counts for four miRNAs across two samples.
- examples/expected_output.txt : the top-4 miRNAs and their toy normalized counts, to confirm the run.

Data Availability
-----------------
Real TCGA data are subject to TCGA/GDC access policies. Provide instructions or scripts to download
public-level miRNA quantification from GDC (or include DOIs/DRS IDs if controlled). The notebook
expects a table with miRNA IDs and normalized counts (e.g., RPM/CPM/DESeq2-normalized).

Reproducibility Notes
---------------------
- Software versions are pinned in env/environment.yml.
- Random seeds are set in the notebook where applicable.
- The analysis is deterministic for a given input table.


