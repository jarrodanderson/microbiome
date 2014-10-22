Carry out the following steps to install the R package/s to extract
and analyze HITChip data. Note that admin rights may be required to
complete the installation, and the data is protected by password/IP
combinations. Kindly report any problems to [developers](Contact).

### Install R

  1. Install [R](http://www.r-project.org/) (NOTE: only the newest version is supported!)
  1. Consider installing [RStudio](http://rstudio.org); a high-quality graphical user interface to R
  1. If you use Windows, install also [RTools](http://cran.r-project.org/bin/windows/Rtools/) (version corresponding to your R version)

### Install dependent packages

Open R. Then Install dependencies from the Tools panel, or run the following commands:


```r
source("http://www.bioconductor.org/biocLite.R")
biocLite(c("ade4", "fastcluster", "df2json", "rjson", "gplots", "devtools", "ggplot2","MASS","minet","mixOmics", "plyr","qvalue","reshape2","RPA","svDialogs","vegan","WGCNA"))
```

If some of these installations fail, ensure from the tools panel that
you have access to CRAN and Bioconductor repositories, then return to
previous step. If you cannot install some of these packages, you can
still try installing the microbiome/HITChipDB packages but some
functionality therein may not work.


### Install microbiome package

The microbiome package contains general data analysis routines. Install the package with the following installation commands in R:


```r
library(devtools) # Load the devtools package
install_github(repo = "microbiome", username = "microbiome") # Install the package
# Test installation by loading the microbiome package in R
library("microbiome")
```

Try out [examples](analysis)!


## Install HITChipDB package (for developers only)

The HITChipDB package contains additional routines to fetch and preprocess HITChip (or MIT/PITChip) data from the MySQL database. Install the package with the following installation commands in R:


```r
library(devtools) # Load the devtools package
install_github(repo = "HITChipDB", username = "microbiome") # Install the package
# Also install RMySQL, multicore and tcltk !
# Test installation by loading the microbiome package in R
library("HITChipDB")
```

Try out [examples](analysis)!
