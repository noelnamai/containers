################## BASE IMAGE ######################
FROM biocontainers/biocontainers:latest

################## METADATA ######################
LABEL base.image="biocontainers:latest"
LABEL version="2"
LABEL software="bwa"
LABEL software.version="0.7.12"
LABEL description="Burrow-Wheeler Aligner for pairwise alignment between DNA sequences"
LABEL website="http://bio-bwa.sourceforge.net/"
LABEL documentation="http://bio-bwa.sourceforge.net/"
LABEL license="http://bio-bwa.sourceforge.net/"
LABEL tags="Genomics"

################## MAINTAINER ######################
MAINTAINER Saulo Alves Aflitos <sauloal@gmail.com>

################## INSTALLATION ######################

RUN conda install bwa=0.7.12

WORKDIR /data/

CMD ["bwa"]
