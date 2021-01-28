FROM r-base

# Install apt packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    libcurl4-openssl-dev libcairo2-dev \
    && rm -rf /var/lib/apt/lists/*

# Install R packages
RUN R -e "install.packages(c('immunarch','svglite'))"

