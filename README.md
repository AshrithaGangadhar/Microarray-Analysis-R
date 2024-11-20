# Microarray Analysis

To identify differentially expressed genes across different experimental conditions in microarray datasets using R.

## **Contents**

- `data/`: Contains raw data files such as the CEL files and targets.
- `scripts/`: R scripts for data normalization, statistical analysis, and visualization.
- `results/`: Processed results, including tables of differentially expressed genes and other analysis outputs.
- `figures/`: Plots and visualizations
- `README.md`: Documentation for the project.


## **Requirements**

### **Software and Tools**
- **R**: Version 4.0 or higher
- **RStudio**: Optional but recommended

### **R Packages**
- `oligo`: For reading and normalizing CEL files.
- `pd.mogene.2.1.st`: Annotation package for the microarray platform.
- `Biobase`: Provides standardized data structures for genomic data.
- `arrayQualityMetrics`: For generating quality metrics reports for microarray data.
- `genefilter`: To filter genes based on specific criteria.
- `annotate`: For extracting gene annotations.
- `limma`: For linear modeling and differential expression analysis.
- `gplots`: Tools for data plotting.
- `ggplot2`: For advanced plotting.
- `ggrepel`: To avoid overlapping of labels in plots.
- `pvca`: For assessing batch effects.
- `org.Mm.eg.db`: Organism-centric annotation package for mouse.
- `mogene21sttranscriptcluster.db`: Platform-centric annotation package.
- `ReactomePA`: For pathway enrichment analyses.

### Install the packages using the following commands in R:
```R
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(c("oligo", "pd.mogene.2.1.st", "Biobase", "arrayQualityMetrics", 
                       "genefilter", "annotate", "limma", "org.Mm.eg.db", 
                       "mogene21sttranscriptcluster.db", "ReactomePA"))
install.packages(c("gplots", "ggplot2", "ggrepel", "pvca"))
