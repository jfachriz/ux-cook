FROM ubuntu:impish

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
    && apt-get -y upgrade -y \
    && apt-get clean

RUN apt-get install -y apt-utils \
    && apt-get install -y build-essential \
        qemu-user-static \
        wget \
        curl \
        git \
        ubuntu-keyring \
        gnupg \
        binfmt-support

ENV HOME /root
WORKDIR ${HOME}
RUN git clone https://github.com/jfachriz/ux-cook
WORKDIR ${HOME}/ux-cook

CMD ["/root/ux-cook/build-hirsute-raw.sh"]