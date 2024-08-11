New methods of preprocessing scRNA/scATAC sequencing data in removing ambient RNA (denosie the background): Cellbender and SoupX

Ambient RNA refers to the RNA molecules present in the sequencing library that do not originate from the individual cells being profiled, but rather from the surrounding cellular environment. I skimed a lot of analyzing codes published in NC journals, it is recommanded to denosie the sequencing data before conducting downstream analysis.

For Cellbender, it uses a deep learning-based approach to identify and remove these ambient RNA contaminations, resulting in a more accurate representation of the true gene expression profiles of the individual cells. The input data requires the h5ad fromat, and can be conducted in the python platform. But, its time-consuming. For more details and useage: https://github.com/broadinstitute/CellBender

For SoupX, unlike Cellbender, it works by analyzing the distribution of gene expression across all cells in the dataset to estimate the ambient RNA contribution, and then subtracts this contribution from each individual cell's gene expression profile. For more details and useage: https://github.com/constantAmateur/SoupX

Recently, I discovered a valuable tool called Celltypist that significantly aids in cell type annotation. This powerful tool stands out due to its flexibility, enabling users to leverage pre-trained models or to develop and train custom models using reference datasets tailored to their specific research interests. We could explore training our annotation models on datasets from hematopoiesis, gastrulation, pre-gastrulation stages or other fields we don't have much experience of annotating, capitalizing on existing published data to enhance our analysis and help discover the subset of cell population. For more details and useage: https://www.celltypist.org/

In addition to my recent explorations, I have dedicated the past two weeks to practicing scATAC-seq analysis. Drawing from my hands-on experience, I've found that employing Python for the analysis offers distinct advantages. Its robust libraries and versatile toolkits streamline the processing and interpretation of scATAC-seq data, making it a more efficient and powerful choice for such complex genomic analyses. For the integration of scRNA-seq and scATAC-seq datasets, the pipeline has been organized in muon.ibpy.

Next plan: reanalysis the data (https://www.sciencedirect.com/science/article/pii/S1934590920305531) "Integrative Single-Cell RNA-Seq and ATAC-Seq Analysis of Human Developmental Hematopoiesis"
