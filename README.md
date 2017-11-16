[![Travis-CI Build Status](https://travis-ci.org/jefferislab/lhns.svg?branch=master)](https://travis-ci.org/jefferislab/lhns)
# lhns
R Package containing neuron skeleton data relevant to the lateral horn of the vinegar fly, Drosophila melanogaster. For use with [nat](https://github.com/jefferis/rcatmaid). In development.

## What's in the package currently?
```r
# install
if (!require("devtools")) install.packages("devtools")
devtools::install_github("jefferislab/lhns")
  
# use
library(lhns)
plot3d(most.lhns)
?most.lhns
plot_pnts()
```

## Remaking data

To remake the data from scratch, I recommend opening the rstudio project and then:

```r
source("data-raw/make.R")
```

To use this, you will then need to reinstall the `lhns` package - you can easily
do this like so:

```r
devtools::update_packages('jefferislab/lhns')
```
### LHN cell types
If you need to alter an LHN cell type classification, you need to edit
[processLHNs.R](data-raw/processLHNs.R) and then follow the steps above i.e. 
`source("data-raw/make.R")`. 

Note: Windows users need [Rtools](http://www.murdoch-sutherland.com/Rtools/) and
[devtools](http://CRAN.R-project.org/package=devtools) to install this way.

## Acknowledgements
* Images from [FlyCircuit](http://flycircuit.tw) were obtained from the NCHC (National Center for High-performance Computing) and NTHU (National Tsing Hua University), Hsinchu, Taiwan.
* Dye-fills of LH neurons were obtained by Shahar Frechter. 

Data compiled and annotated for analysis in Frechter et al. (2017) by Alexander Bates
and Shahar Frechter. 
