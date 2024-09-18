# Seurat Installation Guide

## Before You Start
Make sure to create a working directory and use an R script in Rstudio to type your command lines, as we covered in our previous workshop.

## 1. Installation Instructions for Seurat

### R and RStudio Setup
- Seurat requires **R version 4.0** or greater.
- We recommend installing **RStudio**.

### Installing Seurat 5 from GitHub

First, install **devtools** as it is necessary to install packages from GitHub:

```r
if (!requireNamespace("devtools", quietly = TRUE)) {
    install.packages("devtools")
}
remotes::install_github("satijalab/seurat", "seurat5", quiet = TRUE)
Additional Packages
While not required, the following packages are often used in Seurat v5 vignettes:

SeuratData: Load pre-packaged datasets as Seurat objects
Azimuth: Local annotation of scRNA-seq and scATAC-seq queries across multiple tissues
SeuratWrappers: Enables additional integration and differential expression methods
Signac: Analysis of single-cell chromatin data
Install these packages using the following commands:

remotes::install_github("satijalab/seurat-data", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/azimuth", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/seurat-wrappers", "seurat5", quiet = TRUE)
remotes::install_github("stuart-lab/signac", "seurat5", quiet = TRUE)

install.packages('Seurat')
library(Seurat)


You may see the following warning message:


package which is only available in source form, and may need compilation of C/C++/Fortran: 'Seurat'
Do you want to attempt to install these from sources? y/n:

Installing Seurat via Conda
If you're using Conda, you can install Seurat using the following commands:

conda install bioconda::r-seurat
conda install bioconda/label/cf201901::r-seurat
conda install bioconda/label/gcc7::r-seurat
Installing Seurat and SeuratData in R
For the workshop, the core packages are Seurat and SeuratData.

if (!requireNamespace("Seurat", quietly = TRUE)) {
    install.packages("Seurat")
}

if (!requireNamespace("SeuratData", quietly = TRUE)) {
    install.packages("SeuratData")
}

Additional Packages
The following packages are often used in Seurat v5 vignettes:

SeuratData: Load pre-packaged datasets as Seurat objects
Azimuth: Local annotation of scRNA-seq and scATAC-seq queries across multiple tissues
SeuratWrappers: Enables additional integration and differential expression methods
Signac: Analysis of single-cell chromatin data
Install these packages using the following commands:

r
Copy code
remotes::install_github("satijalab/seurat-data", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/azimuth", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/seurat-wrappers", "seurat5", quiet = TRUE)
remotes::install_github("stuart-lab/signac", "seurat5", quiet = TRUE)
Installing Seurat from CRAN
Seurat is available on CRAN. To install it, run:

r
Copy code
install.packages('Seurat')
library(Seurat)
If you see the following warning:

vbnet
Copy code
package which is only available in source form, and may need compilation of C/C++/Fortran: 'Seurat'
Do you want to attempt to install these from sources? y/n:
Type y to proceed.

Installing Seurat via Conda
If you're using Conda, you can install Seurat using the following commands:

bash
Copy code
conda install bioconda::r-seurat
conda install bioconda/label/cf201901::r-seurat
conda install bioconda/label/gcc7::r-seurat
Installing Seurat and SeuratData in R
For the workshop, the core packages are Seurat and SeuratData:

r
Copy code
if (!requireNamespace("Seurat", quietly = TRUE)) {
    install.packages("Seurat")
}

if (!requireNamespace("SeuratData", quietly = TRUE)) {
    install.packages("SeuratData")
}
2. Install Additional Useful Packages

Data Manipulation and Visualization
For efficient data wrangling and visualization, install the following packages:

dplyr and tidyverse: Data manipulation
ggplot2: Data visualization
Install them using these commands:

r
Copy code
if (!requireNamespace("dplyr", quietly = TRUE)) {
    install.packages("dplyr")
}

if (!requireNamespace("tidyverse", quietly = TRUE)) {
    install.packages("tidyverse")
}

if (!requireNamespace("ggplot2", quietly = TRUE)) {
    install.packages("ggplot2")
}
3. Verify Installation

After installing all the necessary packages, load them to ensure everything is working correctly:

r
Copy code
# Load core packages
library(Seurat)
library(SeuratData)

# Load data wrangling and visualization packages
library(dplyr)
library(ggplot2)
Support

If you encounter any issues, feel free to reach out using the contact information below:

Melike Güler – melgulerw@gmail.com
Ali Yavuz Çakır - ayavuzcakir@gmail.com


