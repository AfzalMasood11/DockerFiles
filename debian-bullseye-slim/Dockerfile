FROM debian:bullseye-slim

LABEL maintainer="Afzal Masood <afzal.masood@coeus-solutions.de>"

RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install -y --no-install-recommends ca-certificates curl wget gnupg netbase \
  		git openssh-client \
		autoconf \
		imagemagick \
		g++ \
		libxml2-dev \
		libxslt-dev \
		libpq-dev \
		bzip2 \
		gcc \
		libcurl4-openssl-dev \
		libdb-dev \
		libssl-dev \
		libtool \
		libwebp-dev \
		libyaml-dev \
		unzip \
		xz-utils \
		zlib1g-dev \
	; \
	rm -rf /var/lib/apt/lists/*
