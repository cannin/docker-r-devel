# Dockerfile for r-devel

## Get Image
```
docker pull cannin/r-devel
```

## Build Image
```
docker build -t cannin/r-devel .
```

## Access shell
```
docker run -i -t cannin/r-devel bash
```

## Clone Bioconductor GitHub Package Repository

NOTE: Replace PACKAGE and VERSION with the name/version of the package
```
git clone https://github.com/Bioconductor-mirror/PACKAGE.git
```

## Install R Packages on either CRAN or Bioconductor
```
source("https://gist.githubusercontent.com/cannin/6b8c68e7db19c4902459/raw/installPackages.R")

pkgs <- c("Biobase", "rcdk", "fingerprint", "rcellminerData", "gplots", "shiny")

installPackages(pkgs)
```

## Build R Package
```
R CMD build PACKAGE
R CMD check PACKAGE_VERSION.tar.gz
```
