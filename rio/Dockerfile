FROM ruaridhw/r-pkgdev:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

WORKDIR /usr/local/R

ADD https://api.github.com/repos/ruaridhw/rio/compare/master...HEAD /dev/null
RUN git clone https://github.com/ruaridhw/rio

RUN Rscript -e 'devtools::install_dev_deps()'

RUN rm -rf /usr/local/R

CMD ["R"]
