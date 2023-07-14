[![DOI](https://zenodo.org/badge/666335439.svg)](https://zenodo.org/badge/latestdoi/666335439)

# Parameter-Free Molecular Classification with Gzip
### Daniel Probst<sup>1</sup>, You?
<sup>1</sup>Institute of Electrical and Micro Engineering, LTS2, EPFL

## Abstract
TBD

## Introduction
The classification of a molecule on a wide variety of physicochemical and pharmakological properties, such as solubility, efficacy against specific diseases, or toxicity, has become a task of high interest in chemistry and biology. With the rise of deep learning during tha past decade, molecular classification has increasingly be carried out by ever-larger models, with mixed results. The newly published parameter-free text classification approach that makes use of Gzip compression has shown excellent performance compared to deep learning architectures, such as transformers, on benchmark data sets.[^1] As the SMILES string encoding of molecular graphs has been shown to be a well-performing molecular representation for applying NLP methods, such as transformers, to chemical tasks including molecular classification, a comparison with the Gzip-based classification method is also relevant in the context of molecular classification.

## Methods
The Gzip-based classifier introduced in this article has been adapted from the implementation presented by Jiang et al. and differs in three points: (1) as, as the authors have noted, the Gzip-based classification method has a relatively high time complexity, multiprocessing has been added; (2) multi-task classification has been added; and (3) a class weighing scheme has been implemented to account for unbalanced data. Furthermore, the capability to preprocess data, in this case the SMILES strings, has been added to the calling program.

## Results
The current results are presented in the table below. Data sets with random splits were ran a total of four times.

|     Data Set      | Split  | AUROC (Valid) |  F1 (Valid)   | AUROC (Test)  |   F1 (Test)   |
|-------------------|--------|---------------|---------------|---------------|---------------|
|bbbp               |scaffold|0.891 +/- 0.0  |0.902 +/- 0.0  |0.679 +/- 0.0  |0.686 +/- 0.0  |
|bace_classification|random  |0.793 +/- 0.038|0.793 +/- 0.038|0.789 +/- 0.038|0.789 +/- 0.038|
|clintox            |random  |0.805 +/- 0.038|0.965 +/- 0.038|0.77 +/- 0.038 |0.958 +/- 0.038|
|tox21              |random  |0.6 +/- 0.007  |0.308 +/- 0.007|0.599 +/- 0.007|0.303 +/- 0.007|
|sider              |random  |0.56 +/- 0.007 |0.788 +/- 0.007|0.563 +/- 0.007|0.778 +/- 0.007|

## Discussion
TBD

## References
[^1] https://arxiv.org/abs/2212.09410

# What is this?
This is an experiment for a small open source manuscript/article that aims to validate and evaluate the performance of compression-based molecular classification using Gzip. If you want to join/help out, leave a message or a pull request that includes your name and, if available, your affiliation.
