FROM ruaridhw/r-pkgdev:latest
LABEL org.label-schema.license="GPL-2.0" \
      org.label-schema.vcs-url="https://github.com/ruaridhw/dockerfiles/tree/master/rClr" \
      org.label-schema.vendor="" \
      maintainer="Ruaridh Williamson <ruaridh.williamson@gmail.com>"

WORKDIR /usr/local/R

ADD https://api.github.com/repos/ruaridhw/rClr/compare/master...HEAD /dev/null
RUN git clone https://github.com/ruaridhw/rClr

# Mono 3.12.1 Dockerfile
## https://github.com/mono/docker/blob/e61f59607011d1acd9d594bcef936588a78929e6/3.12.1/Dockerfile
## MAINTAINER Jo Shields <jo.shields@xamarin.com>
##
## This file is no longer maintained and has recently been deleted because
## the Mono 3.x series is "ancient and not updated any longer".
## -- https://github.com/mono/docker/commit/454d06e1
## Unfortunately, rClr doesn't compile with Mono 4.x or Mono 5.x (as yet).

RUN apt-get update \
	&& apt-get install -y gnupg curl \
	&& rm -rf /var/lib/apt/lists/* \
  && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF \
  && echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/3.12.0 main" > /etc/apt/sources.list.d/mono-xamarin.list \
  && echo "deb http://download.mono-project.com/repo/debian 312-security main" >> /etc/apt/sources.list.d/mono-xamarin.list \
	&& apt-get update \
	&& curl -s https://gist.githubusercontent.com/ruaridhw/b00e75647c8e96c2f44044c970f19c7f/raw/dc347b538676281c2cf1e35392f5ab9d13d84336/install-mono-3_12.sh | bash /dev/stdin \
	## && apt-get install -y mono-devel ca-certificates-mono fsharp mono-vbnc nuget \
	&& apt-get update \
	&& apt-get install -y libglib2.0-dev \
	&& rm -rf /var/lib/apt/lists/*

RUN Rscript -e 'devtools::install_dev_deps()'

RUN rm -rf /usr/local/R

CMD ["R"]
