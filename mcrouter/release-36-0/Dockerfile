FROM ubuntu:14.04
MAINTAINER Alif Rachmawadi <arch@subosito.com>

ENV MCROUTER_DIR /usr/local/mcrouter
ENV MCROUTER_REPO https://github.com/facebook/mcrouter.git
ENV MCROUTER_RELEASE release-36-0

RUN DEBIAN_FRONTEND=noninteractive \
 && apt-get update \
 && apt-get install -y git \
 && mkdir -p $MCROUTER_DIR/repo \
 && cd $MCROUTER_DIR/repo && git clone $MCROUTER_REPO \
 && cd $MCROUTER_DIR/repo/mcrouter && git checkout $MCROUTER_RELEASE \
 && cd $MCROUTER_DIR/repo/mcrouter/mcrouter/scripts \
 && ./install_ubuntu_14.04.sh $MCROUTER_DIR \
 && ./clean_ubuntu_14.04.sh $MCROUTER_DIR \
 && rm -rf $MCROUTER_DIR/repo \
 && ln -s $MCROUTER_DIR/install/bin/mcpiper /usr/local/bin/mcpiper \
 && ln -s $MCROUTER_DIR/install/bin/mcrouter /usr/local/bin/mcrouter

RUN mkdir -p /var/mcrouter/fifos /var/spool/mcrouter

VOLUME /var/mcrouter/fifos
VOLUME /var/spool/mcrouter

ENTRYPOINT ["mcrouter"]
