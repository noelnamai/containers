################## BASE IMAGE ######################

FROM biocontainers/biocontainers:latest

################## METADATA ######################
LABEL base.image="biocontainers:latest"
LABEL version="1"
LABEL software="gapcloser"
LABEL software.version="1.12-r6"
LABEL description="A novel short-read assembly method that can build a de novo draft assembly for the human-sized genomes"
LABEL website="http://soap.genomics.org.cn/gapcloser.html"
LABEL documentation="http://soap.genomics.org.cn/gapcloser.html"
LABEL license="http://soap.genomics.org.cn/gapcloser.html"
LABEL tags="Genomics"

################## INSTALLATION ######################
################## BEGIN INSTALLATION ######################

ENV ZIP=GapCloser-bin-v1.12-r6.tgz
ENV URL=https://github.com/BioDocker/software-archive/releases/download/gapcloser
ENV DST=/home/biodocker/bin

RUN wget $URL/$ZIP -O $DST/$ZIP && \
    tar xvf $DST/$ZIP -C $DST && \
    rm $DST/$ZIP

# CHANGE WORKDIR TO /DATA
WORKDIR /data

# DEFINE DEFAULT COMMAND
CMD ["GapCloser"]

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Saulo Alves Aflitos <sauloal@gmail.com>

