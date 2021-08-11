# Data for "Microbial Rhodopsins: The Last Two Decades"

The repository contains sequences, trimmed alignment, the best phylogenetic tree and metadata for known rhodopsin families used in [Microbial Rhodopsins: The Last Two Decades](https://doi.org/10.1146/annurev-micro-031721-020452).

## A phylogenetic tree of representative microbial rhodopsins from the different families

The tree is based on representatives from (mostly) characterized rhodopsin families. Representative sequences were taken from UniRef50 and a custom database of 50%-identity clusters of channelrhodopsins and aligned with mafft using the iterative method with local pairwise alignment and trimmed at positions with >10% alignment gaps to produce a final alignment of 315 protein sequences with a total alignment length of 186 residues. Phylogeny was reconstructed with iqtree with an automatic model selection and 1000 ultra-fast bootstrap iterations, NNI perturbation strength of 0.2 and an upper limit of unsuccessful iterations of 500. The search was repeated 100 times and the best-scoring tree was chosen. Branches with a support of less than 70 are collapsed and support values of 95-100 are indicated with dots. The tree is formally unrooted. Note that the position of the schizorhodopsins on this tree differs markedly from the previous reconstruction, which likely reflects the presence of conflicts in the alignment and thus the precise position of this family remains to be investigated.

Note that only a minority of the selected sequences have been experimentally characterized and not all of the characterized rhodopsins have been included in the dataset.

## Files in the repository

* `data/rhodopsins.fasta` - selected rhodopsin cluster representatives
* `data/rhodopsins_trimmed.fasta` - trimmed alignment used for phylogeny reconstruction
* `iqtree/*` - iqtree output files
* `metadata/metadata.csv` - metadata

## Metadata structure

| Column             | Description                                       |
|--------------------|---------------------------------------------------|
| ID                 | Sequence ID                                       |
| Source             | Source database                                   |
| Organism           | Organism                                          |
| Organism ID        | NCBI taxonomy ID                                  |
| Lineage            | Taxonomic lineage                                 |
| Subfamily          | Rhodopsin clade/subfamily                         |
| Sequence           | Amino acid sequence                               |
| Symbol             | Protein symbol/alias                              |
| Activity reference | Reference for activity for characterized proteins |

