FROM rocker/tidyverse:latest

RUN apt-get update

# Install external dependencies
RUN apt-get update -qq \
  && apt-get install -y --no-install-recommends \
    libcurl4-openssl-dev \
    libssl-dev \
    libxml2-dev \
    git \
    zlib1g-dev \
    qpdf \
    mesa-common-dev \
    libglu1-mesa-dev \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/ \
  && rm -rf /tmp/downloaded_packages/ /tmp/*.rds

# "heatmap3,ggrepel,reshape2,DBI,factoextra,fpc,circlize,tidyr,MASS,Rtsne,readr,shiny,shinythemes,treemap,igraph,airr,ggseqlogo,UpSetR,stringr,ggalluvial,ggplot2,dplyr,dtplyr,dbplyr,data.table,gridExtra,ggpubr,Rcpp,knitr,roxygen2,testthat,pkgdown,assertthat,sparklyr"

RUN install2.r --deps TRUE --skipinstalled --error heatmap3 ggrepel reshape2 DBI factoextra fpc circlize tidyr MASS Rtsne readr readxl shiny shinythemes treemap igraph airr ggseqlogo UpSetR stringr ggalluvial ggplot2 dplyr dtplyr dbplyr data.table gridExtra ggpubr Rcpp knitr roxygen2 testthat pkgdown assertthat sparklyr rsconnect

RUN rm -rf /tmp/downloaded_packages/
