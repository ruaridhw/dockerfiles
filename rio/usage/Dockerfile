FROM ruaridhw/rio:latest
LABEL org.label-schema.license="GPL-2.0" \
      org.label-schema.vcs-url="https://github.com/ruaridhw/dockerfiles/tree/master/rio/usage" \
      org.label-schema.vendor="" \
      maintainer="Ruaridh Williamson <ruaridh.williamson@gmail.com>"

ENV workingdir /usr/local/R

COPY . "$workingdir"

WORKDIR "$workingdir"

RUN Rscript -e 'devtools::install_dev_deps()'

CMD ["Rscript", "-e", "devtools::check()"]
