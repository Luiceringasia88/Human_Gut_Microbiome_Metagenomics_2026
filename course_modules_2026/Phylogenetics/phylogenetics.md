# Building Phylogenetic Trees

![Image of a DNA](images/DNA.png)

## Learning Objectives

- Understand common methods of phylogenetic tree inference
- Use IQ-TREE and FastTree for phylogenetic tree inference from alignment data.
- Describe key steps in creating a phylogenetic tree.

## Contents
- [Phylogenetic Tree Inference](#phylogenetic-tree-inference)
- [Multiple Sequence Alignments](#multiple-sequence-alignments)
- [Building a Phylogenetic Tree](#building-a-phylogenetic-tree)
- [Summary](#summary)

---

## Phylogenetic Tree Inference

### Tree Topology

A phylogenetic tree represents evolutionary relationships among sequences.  
The topology describes how taxa are connected, independent of branch lengths.

### Applications of Phylogenetic Trees

Phylogenetic trees are widely used to:

- Understand evolutionary relationships  
- Identify transmission clusters  
- Investigate population structure  
- Track pathogen spread  

### Newick Format

Phylogenetic trees are commonly stored in **Newick format**, which represents tree structure using parentheses.

Example:


### Methods for Inferring Trees

Common tree inference approaches include:

- Distance-based methods  
- Maximum Parsimony  
- Maximum Likelihood  
- Bayesian inference  

### Assessing Tree Uncertainty (Bootstrap)

Bootstrap analysis evaluates confidence in tree branches by resampling alignment columns and reconstructing trees multiple times.

---

## Multiple Sequence Alignments

Phylogenetic inference requires a **multiple sequence alignment (MSA)**.  
The alignment ensures homologous positions are compared across sequences.

Alignment quality directly affects tree accuracy. Always inspect alignments before proceeding with inference.

---

## Building a Phylogenetic Tree

### Extracting Variable Sites with SNP-sites

`SNP-sites` extracts variable positions from an alignment to generate a reduced alignment containing informative sites only.

```bash
snp-sites -o core_snps.aln alignment.fasta
