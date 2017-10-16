FROM rocker/r-ver:latest
MAINTAINER Ruaridh Williamson "ruaridh.williamson@gmail.com"

# Install dependencies for curl, openssl, git2r and xml2 packages
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcurl4-openssl-dev \
    libssl-dev \
    zlib1g-dev \
    libxml2-dev \
    git-all \
  && install2.r --error \
    devtools

CMD ["R"]
