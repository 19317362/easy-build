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
  && apt-get -y install curl git mc rsync screen tig genisoimage vim openjdk-7-jdk \
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
  && useradd --uid 1021 --create-home --shell /bin/bash u1021 \
  && useradd --uid 1022 --create-home --shell /bin/bash u1022 \
  && useradd --uid 1023 --create-home --shell /bin/bash u1023 \
  && useradd --uid 1024 --create-home --shell /bin/bash u1024 \
  && useradd --uid 1025 --create-home --shell /bin/bash u1025 \
  && useradd --uid 1026 --create-home --shell /bin/bash u1026 \
  && useradd --uid 1027 --create-home --shell /bin/bash u1027 \
  && useradd --uid 1028 --create-home --shell /bin/bash u1028 \
  && useradd --uid 1029 --create-home --shell /bin/bash u1029 \
  && useradd --uid 1030 --create-home --shell /bin/bash u1030 \
  && useradd --uid 1031 --create-home --shell /bin/bash u1031 \
  && useradd --uid 1032 --create-home --shell /bin/bash u1032 \
  && useradd --uid 1033 --create-home --shell /bin/bash u1033 \
  && useradd --uid 1034 --create-home --shell /bin/bash u1034 \
  && useradd --uid 1035 --create-home --shell /bin/bash u1035 \
  && useradd --uid 1036 --create-home --shell /bin/bash u1036 \
  && useradd --uid 1037 --create-home --shell /bin/bash u1037 \
  && useradd --uid 1038 --create-home --shell /bin/bash u1038 \
  && useradd --uid 1039 --create-home --shell /bin/bash u1039 \  
  && useradd --uid 1040 --create-home --shell /bin/bash u1040 \  
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
  && echo "u1020 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1021 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1022 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1023 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1024 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1025 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1026 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1027 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1028 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1029 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1030 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1031 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1032 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1033 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1034 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1035 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1036 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1037 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1038 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1039 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers \
  && echo "u1040 ALL=(ALL) NOPASSWD: ALL" | tee -a /etc/sudoers 

# ENV USER='u1000'
ENV TZ=Asia/Shanghai
ENV JAVA_OPTS="-Duser.timezone=Asia/Shanghai -Xms2G -Xmx8G"
ENV JACK_SERVER_VM_ARGUMENTS="-Xmx8G"


# EOF
