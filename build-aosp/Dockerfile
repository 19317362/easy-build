# ===========================================================================================
# Dockerfile for building Android Open Source Project
#
# References:
#       http://source.android.com/source/index.html
# ===========================================================================================

FROM ubuntu:14.04

RUN sed -i 's/main$/main universe/' /etc/apt/sources.list \
  && apt update \
  && apt install -y software-properties-common python-software-properties \
  && add-apt-repository -y ppa:openjdk-r/ppa \
  && apt update \
  && dpkg --add-architecture i386 \
  && apt-get -qq update && apt-get -qqy dist-upgrade \
  && apt-get -y install curl git mc rsync screen tig vim openjdk-8-jdk \
  && update-alternatives --config java \
  && update-alternatives --config javac \
  && apt-get -y install git-core gnupg flex bison gperf build-essential \
  zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 \
  lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache \
  libgl1-mesa-dev libxml2-utils schedtool xsltproc unzip \
  python-networkx bc lzop u-boot-tools \
  && apt-get clean \
  && useradd noroot -u 1000 -s /bin/bash \
  && echo "noroot ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers


# EOF
