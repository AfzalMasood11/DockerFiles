# Using slim-stretch image for small size
FROM debian:buster-slim

LABEL maintainer="Afzal Masood <afzal.masood@coeus-solutions.de>"

RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install -y --no-install-recommends ca-certificates curl netbase wget \
  		bzr git mercurial openssh-client procps gnupg dirmngr && \
  rm -rf /var/lib/apt/lists/*

RUN set -ex; \
	apt-get update; \
	apt-get upgrade -y; \
	apt-get install -y --no-install-recommends \
		autoconf \
		automake \
		bzip2 \
		dpkg-dev \
		file \
		g++ \
		gcc \
		imagemagick \
		libcurl4-openssl-dev \
		libdb-dev \
		libmagickcore-dev \
		libmagickwand-dev \
		libpq-dev \
		libssl-dev \
		libtool \
		libwebp-dev \
		libxml2-dev \
		libxslt-dev \
		libsqlite3-dev \
		libyaml-dev \
		unzip \
		xz-utils \
		zlib1g-dev \
		\
# https://lists.debian.org/debian-devel-announce/2016/09/msg00000.html
		$( \
# if we use just "apt-cache show" here, it returns zero because "Can't select versions from package 'libmysqlclient-dev' as it is purely virtual", hence the pipe to grep
			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then \
				echo 'default-libmysqlclient-dev'; \
			else \
				echo 'libmysqlclient-dev'; \
			fi \
		) \
	; \
	rm -rf /var/lib/apt/lists/*
