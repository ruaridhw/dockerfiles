FROM ruaridhw/rclr:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

COPY . /usr/local/R/

WORKDIR /usr/local/R

RUN Rscript -e 'devtools::install_dev_deps()'

CMD ["/usr/local/lib/R/bin/R", "--no-site-file", "--no-environ", "--no-save", "--no-restore", "--quiet", "CMD INSTALL", "/usr/local/R", "--library='/usr/local'"]
