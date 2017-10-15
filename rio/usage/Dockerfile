FROM ruaridhw/rio:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

COPY . /usr/local/R/

WORKDIR /usr/local/R

RUN Rscript -e 'devtools::install_dev_deps()'

CMD ["Rscript", "-e", "devtools::check()"]
