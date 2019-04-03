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
  && apt-get -y install curl git mc rsync screen tig genisoimage vim \
  gcc bison autoconf wget \
  # patch, texinfo, 
  dos2unix \
  git-core gnupg flex bison gperf build-essential \
  zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 \
  lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache \
  libgl1-mesa-dev libxml2-utils schedtool xsltproc unzip \
  python-networkx bc lzop u-boot-tools tofrodos python-markdown\
  libgl1-mesa-dev xsltproc texi2html texinfo gawk busybox \
  && apt-get clean \
  && useradd --uid 1000 --create-home --shell /bin/bash u1000 \
  && useradd --uid 1001 --create-home --shell /bin/bash u1001 \
  && useradd --uid 1002 --create-home --shell /bin/bash u1002 \
  && useradd --uid 1003 --create-home --shell /bin/bash u1003 \
  && useradd --uid 1004 --create-home --shell /bin/bash u1004 \
  && useradd --uid 1005 --create-home --shell /bin/bash u1005 \
  && useradd --uid 1006 --create-home --shell /bin/bash u1006 \
  && useradd --uid 1007 --create-home --shell /bin/bash u1007 \
  && useradd --uid 1008 --create-home --shell /bin/bash u1008 \
  && useradd --uid 1009 --create-home --shell /bin/bash u1009 \
  && useradd --uid 1010 --create-home --shell /bin/bash u1010 \
  && useradd --uid 1011 --create-home --shell /bin/bash u1011 \
  && useradd --uid 1012 --create-home --shell /bin/bash u1012 \
  && useradd --uid 1013 --create-home --shell /bin/bash u1013 \
  && useradd --uid 1014 --create-home --shell /bin/bash u1014 \
  && useradd --uid 1015 --create-home --shell /bin/bash u1015 \
  && useradd --uid 1016 --create-home --shell /bin/bash u1016 \
  && useradd --uid 1017 --create-home --shell /bin/bash u1017 \
  && useradd --uid 1018 --create-home --shell /bin/bash u1018 \
  && useradd --uid 1019 --create-home --shell /bin/bash u1019 \  
  && useradd --uid 1020 --create-home --shell /bin/bash u1020 \
  && echo "u1000 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1001 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1002 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1003 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1004 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1005 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1006 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1007 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1008 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1009 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1010 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1011 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1012 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1013 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1014 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1015 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1016 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1017 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1018 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1019 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1020 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers 

# ENV USER='u1000'
ENV TZ=Asia/Shanghai


# EOF
