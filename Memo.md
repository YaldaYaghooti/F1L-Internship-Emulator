# Key Scientific Question (KSQ)

Using available scRNA-seq data from cancer cell lines, how would you explore the use of the following FDA-approved antibody therapies in additional cancers?

Trastuzumab: Targets HER2 and is used in the treatment of HER2-positive breast and gastric cancers.

Bevacizumab: Targets VEGF and is used for a variety of cancers, including colorectal, lung, glioblastoma, breast, liver, and kidney cancer.

# My Understanding of the KSQ

How can we use scRNA-seq data to identify cell lines from cancer types other than ones mentioned above that are (in a way) similar to these cancer types?

# Unclear elements of the KSQ

1) Do we assume that any cell line with the mentioned cancer types with the mentioned condition (e.g., HER2-positive) respond to these medications?
2) Is this a classification task (stating in the end what other cancer types will probably respond to these medications) or should we rank cancer types based on any score we obtain?
3) Do we only have access to scRNA-seq data or could we use other data types such as genetic mutations present in the cell lines?

# Questions about the [Paper]( https://www.nature.com/articles/s41588-020-00726-6 )

**Q1: How did the authors handle the potential caveat of co-culturing cell lines before profiling by scRNA-seq? Why do you think that caveat was or was not adequately addressed?**

A: First, the authors compared the heterogeneity patterns of cells from each cell line in each pool and between pools and stated that heterogeneity patterns within each cell line were similar in the two.

Second, the authors compared gene expression profiles and heterogeneity patterns of 6 cell lines with and without 3 days of co-culture and concluded that heterogeneity patterns were consistent between the two groups.

I do not believe that these results are enough to conclude that co-culturing cells did not have a significant effect on gene expression patterns of cells, since the authors studied 200 cell lines but only compared 6 cell lines with and without cu-culture. In addition, if different pools consisted of the same cell line composition, it makes sense that different pools would present similar heterogeneity patterns and that does not mean that co-culturing did not have any effect on the cell lines.

**Q2: The authors identified discrete subpopulations of cells within a subset of individual cell lines (Fig. 2A-B). What might be the reason why some cell lines have these discrete subpopulations while others do not?**

A: As stated in the paper, discrete subpopulations arise mostly due to genetic differences (mutations). One reason explaining why some cell lines demonstrate these discrete subpopulations might be that some cell lines have higher genomic instability and therefore higher mutation rates.

**Q3: What are Recurrent Heterogeneous Programs (RHPs) and how were they defined?**

A: Recurrent heterogeneous programs (RHPs) are cellular programs that show differential activation between cells within multiple cell lines. The authors defined these programs by first using NMF on top 50 upregulated genes in each cell. They also performed hierarchical clustering to find the programs most active in each cell.

**Q4: How do the identified RHPs relate to in vivo programs of heterogeneity in tumors, and what evidence supports this relationship?**

A: The authors compared the RHPs present in cancer cell lines and in vivo tumor samples and found that these RHPs significantly overlap between cell lines and in vivo samples.

**Q5: Where can you download the scRNA-seq data as shown in Figure 1B?**

A: [Link to the dataset in Broad Institute’s single-cell portal](https://singlecell.broadinstitute.org/single_cell/study/SCP542/pan-cancer-cell-line-heterogeneity)
GEO accession number: GSE157220








