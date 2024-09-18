# RSG-Single-Cell-Workshop2024
Before you start …
Remember to create a working directory, and use an R script in Rstudio to type your command lines, as we covered in our previous workhop.
1.	Installation Instructions for Seurat
To install Seurat, R version 4.0 or greater is required. We also recommend installing R Studio.
  Seurat 5: 
Install from GitHub
Install devtools
This package is necessary to install some packages from GitHub.
if (!requireNamespace("devtools", quietly = TRUE)) {
    install.packages("devtools")
}
Copy the code below to install Seurat v5:
remotes::install_github("satijalab/seurat", "seurat5", quiet = TRUE)
The following packages are not required but are used in many Seurat v5 vignettes:
•	SeuratData: automatically load datasets pre-packaged as Seurat objects
•	Azimuth: local annotation of scRNA-seq and scATAC-seq queries across multiple organs and tissues
•	SeuratWrappers: enables use of additional integration and differential expression methods
•	Signac: analysis of single-cell chromatin data
remotes::install_github("satijalab/seurat-data", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/azimuth", "seurat5", quiet = TRUE)
remotes::install_github("satijalab/seurat-wrappers", "seurat5", quiet = TRUE)
remotes::install_github("stuart-lab/signac", "seurat5", quiet = TRUE)
Install from CRAN
Seurat is available on CRAN for all platforms. To install, run:
# Enter commands in R (or R studio, if installed)
install.packages('Seurat')
library(Seurat)
If you see the warning message below, enter y:
package which is only available in source form, and may need compilation of C/C++/Fortran: 'Seurat'
Do you want to attempt to install these from sources?
y/n:
Install from Conda
To install this package run one of the following:
conda install bioconda::r-seurat
conda install bioconda/label/cf201901::r-seurat
conda install bioconda/label/gcc7::r-seurat
Install Seurat and SeuratData in R
The core packages for your workshop will be Seurat and SeuratData.
# Install Seurat V5
if (!requireNamespace("Seurat", quietly = TRUE)) {
    install.packages("Seurat")
}

# Install SeuratData
if (!requireNamespace("SeuratData", quietly = TRUE)) {
    install.packages("SeuratData")
}
2.	Install Additional Useful Packages
2.1 Data manipulation and visualization
•	dplyr and tidyverse: for efficient data wrangling.
•	ggplot2: for powerful and flexible data visualization.
if (!requireNamespace("dplyr", quietly = TRUE)) {
    install.packages("dplyr")
}

if (!requireNamespace("tidyverse", quietly = TRUE)) {
    install.packages("tidyverse")
}

if (!requireNamespace("ggplot2", quietly = TRUE)) {
    install.packages("ggplot2")
}

3.	Verify Installation
After installing all the packages, it’s good practice to load them to ensure everything is working correctly.
# Load core packages
library(Seurat)
library(SeuratData)

# Load data wrangling and visualization packages
library(dplyr)
library(ggplot2)

If you encounter any problems, do not hesitate to contact us using the contact information below:

Melike Güler – melgulerw@gmail.com
Ali Yavuz Çakır - ayavuzcakir@gmail.com
