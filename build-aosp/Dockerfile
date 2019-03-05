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
  && apt-get -y install curl git mc rsync screen tig genisoimage vim openjdk-8-jdk \
  && update-alternatives --config java \
  && update-alternatives --config javac \
  && apt-get -y install git-core gnupg flex bison gperf build-essential \
  zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 \
  lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache \
  libgl1-mesa-dev libxml2-utils schedtool xsltproc unzip \
  python-networkx bc lzop u-boot-tools \
  && apt-get clean \
  && useradd --uid 1000 --create-home --shell /bin/bash u1000 \
  && useradd --uid 1001 --create-home --shell /bin/bash u1001 \
  && useradd --uid 1002 --create-home --shell /bin/bash u1002 \
  && useradd --uid 1003 --create-home --shell /bin/bash u1003 \
  && echo "u1000 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1001 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1002 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1003 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers

ENV USER='u1000'

# EOF
