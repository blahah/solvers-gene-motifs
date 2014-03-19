solvers-gene-motifs
===================

Solvers.io project to predict gene expression from motif combinations in promoters

## Example data

`example_data/example_500rows.csv` is an example of the kind of data we can generate.

- There is an initial column, `AGI`, which contains the gene identifier. This is for information only - it can be discarded for the analysis.
- A final label column, `Value`, is dummy encoded*: either 1 or -1. 1 means the gene was expressed in a particular cell type, while -1 means it was not expressed.
- All the remaining columns are features (transcription factor binding motifs) that exist in the promoter of one or more genes. These are binary: 1 indicates the feature was present, 0 indicates it was absent.

\* *note: we can also provide scalar values rather than dummy encoding.*

## Full datasets

One dataset is provided for now. We can generate many such datasets if needed.

1. https://www.dropbox.com/s/ghb7w0nh0xqg0qh/A_thaliana_motifs_guard_cell_expression.csv

## The challenge

We want to be able to:

1. Predict whether a gene will be expressed in a particular condition given its promoter sequence
2. Find out exactly which combinations of motifs are important in the predictions

or to rephrase without the biology:

1. Predict the `Value` given the motif columns.
2. Identify which features are important in the predictions.