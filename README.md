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
```
git clone https://github.com/Bioconductor-mirror/PACKAGE/tree/master
```

## Build R Package
```
R CMD BUILD PACKAGE
R CMD CHECK PACKAGE_VERSION.tar.gz
```
