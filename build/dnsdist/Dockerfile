FROM parrot.run/core:5
MAINTAINER Lorenzo "Palinuro" Faletra (palinuro@linux.it)
ENV DEBIAN_FRONTEND noninteractive
ENV VERSION 2

# Update system
RUN apt-get update;apt-get -y dist-upgrade; rm -rf /var/lib/apt/lists/*

# Install dependencies
RUN apt-get update;apt-get -y install dnsdist ca-certificates ssl-cert; \
	rm -rf /var/lib/apt/lists/*

COPY ./start.sh /start.sh

STOPSIGNAL SIGTERM
CMD /start.sh
ENTRYPOINT /start.sh
