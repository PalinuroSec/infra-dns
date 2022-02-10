FROM docker.io/parrotsec/core:5.0
MAINTAINER Lorenzo "Palinuro" Faletra (palinuro@linux.it)
ENV DEBIAN_FRONTEND noninteractive
ENV VERSION 1.0

# Update system
RUN apt-get update;apt-get -y dist-upgrade; rm -rf /var/lib/apt/lists/*

# Install dependencies
RUN apt-get update;apt-get -y install dnsdist ca-certificates ssl-cert; \
	rm -rf /var/lib/apt/lists/*

STOPSIGNAL SIGTERM
CMD /start.sh
