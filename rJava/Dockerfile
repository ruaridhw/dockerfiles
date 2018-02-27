FROM rocker/tidyverse:latest
LABEL org.label-schema.license="GPL-2.0" \
      org.label-schema.vcs-url="https://github.com/ruaridhw/dockerfiles/tree/master/rsqlserver" \
      org.label-schema.vendor="" \
      maintainer="Ruaridh Williamson <ruaridh.williamson@gmail.com>"

RUN apt-get install liblzma-dev libbz2-dev openjdk-8-jre

RUN export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
RUN R CMD javareconf

RUN Rscript -e "install.packages('rJava', repos='https://cran.rstudio.com/')"

EXPOSE 8787
CMD ["/init"]
