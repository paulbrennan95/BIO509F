# BIO509F
Machine Learning Class Final Project 2020


Table of Contents:

1. Introduction

2. Data Description

3. How to run scripts

4. Outputs



1. Introduction:
HLA molecules exist on surface of cells, and have a peptide loaded onto its exterior surface to present it to immune cells ( T cells and natural killer (NK) cells

Two studies (Dimarco, 2017 and Sarkizova, 2019) have isolated this allele of HLA and eluted the peptides bound to them (n=5748)
Using these peptides, we can use ML tools to determine the binding motifs and predict other peptides that would likely bind 
Robust ANN-based HLA peptide prediction tools already exist, but I wanted to create a lower-throughput tree-based prediction tool so I can ultimately apply it to peptide-HLA and NK cell receptor (KIR) interactions where our data will be on the order of 400 peptides.

The goal of this project is to use a Random Forest Classifier to predict which peptides have a high probability of binding to HLA-C*16:01. 


2. Data Description:
The data consists of peptides eluted from the the HLA-C*16:01 molecule from two studies Dimarco (2017) and Sarkizova (2019). I included a combined list of these peptides in csv format called C1601_peptides_all.csv 

There is no target vector a priori. The target vector is created within the script.



3. How to run scripts:

Run the main function with 3 inputs:  
1. csv file of known-binding peptides to train model
2. algorithm: "RandomForest"
3. csv file of unknown-binding peptides to predict binding probabilities


4. Outputs:
A plot of feature importances will appear in IDE
An output file called output_file.txt will show the prediction probabilities of the unknown peptides (in the directory of the script)

