FROM ruaridhw/r-pkgdev:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

COPY . /usr/local/R/

WORKDIR /usr/local/R

RUN Rscript -e 'devtools::install_dev_deps()'

RUN rm -rf /usr/local/R

CMD ["R"]
