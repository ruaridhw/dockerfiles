FROM ruaridhw/r-pkgdev:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

ADD https://api.github.com/repos/ruaridhw/rio/compare/master...HEAD /dev/null
RUN git clone https://github.com/ruaridhw/rio

WORKDIR /usr/local/R

RUN Rscript -e 'devtools::install_dev_deps()'

RUN rm -rf /usr/local/R

CMD ["R"]
