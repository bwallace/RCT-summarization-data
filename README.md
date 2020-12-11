# RCT-summarization-data

Data from our AMIA 2020 paper "Generating (Factual?) Narrative Summaries of RCTs: Experiments with Neural Multi-Document Summarization". Pre-print: https://arxiv.org/abs/2008.11293.

All data here is from abstracts indexed by and available on [PubMed](https://pubmed.ncbi.nlm.nih.gov/). The inputs are titles and abstracts of articles describing randomized controlled trials (RCTs); the targets are taken as the "Author Conclusions" section from the abstracts of Cochrane (https://www.cochranelibrary.com/) evidence syntheses of the same. These report an overall summary of the evidence conveyed in the constituent trials.

The data format is straightforward: We have divided the data into `train`, `dev`, and `test` sets. For each there are two files, comprising `inputs` and `targets` respectively. The former includes the individual trial reports (PMIDs, titles, abstracts) that correspond to a particular evidence synopsis; the latter is the target output (i.e., the authors conclusions as stated in the abstract). Note that there are multiple inputs per target (multi-document summarization), and that the number of trial reports associated with each synthesis varies. See the [Jupyter notebook](https://github.com/bwallace/RCT-summarization-data/blob/main/working-with-the-data.ipynb) for a bit more explanation. 

If you use this data, please cite:

```
@inproceedings{AMIA-summarization-2021,
    title = {{Generating (Factual?) Narrative Summaries of RCTs: Experiments with Neural Multi-Document Summarization}},
    author = {Byron C. Wallace and Sayantan Saha and Frank Soboczenski and Iain J. Marshall},
    Booktitle = {{Proceedings of AMIA Informatics Summit}},
    year = {2021},
}
```

Questions to: b.wallace@northeastern.edu.

