################## BASE IMAGE ######################
FROM biocontainers/biocontainers:latest

################## METADATA ######################
LABEL base.image="biocontainers:latest"
LABEL version="2"
LABEL software="TPP"
LABEL software.version="4.8"
LABEL description="a collection of integrated tools for MS/MS proteomics"
LABEL website="http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP"
LABEL documentation="http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP"
LABEL license="http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP"
LABEL tags="Proteomics"

################## MAINTAINER ######################
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>

USER root

WORKDIR /usr/local/

RUN apt-get update && apt-get install -y libxml-sax-expat-perl && apt-get clean all

RUN wget https://github.com/BioDocker/software-archive/releases/download/TPP/tpp-4.8.0.zip && \
  unzip tpp-4.8.0.zip

ENV PATH /usr/local/tpp/bin/:$PATH

USER biodocker

WORKDIR /data/
