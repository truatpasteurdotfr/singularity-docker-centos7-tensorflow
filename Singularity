BootStrap: docker
From: centos:centos7
# Tru Huynh <tru@pasteur.fr>

%runscript
    echo "This is what happens when you run the container..."
    bash


%post

yum -y update
yum -y install wget \
               tar gzip \
               perl \
               which findutils zip unzip zlib-devel \
               java-1.8.0-openjdk-devel \
               git \
               numpy python-devel

yum -y install centos-release-scl-rh

yum -y install devtoolset-3-gcc devtoolset-3-gcc-c++ devtoolset-3-binutils 

yum -y install epel-release
yum -y install  python-wheel python-pip
                   
yum -y install https://people.centos.org/tru/bazel-centos7/bazel-0.4.5-1.el7.centos.x86_64.rpm

wget https://github.com/tensorflow/tensorflow/archive/v1.0.1.tar.gz -O /tmp/tensorflow-1.0.1.tar.gz

mkdir /build && tar -C build -xzf /tmp/tensorflow-1.0.1.tar.gz && /bin/rm /tmp/tensorflow-1.0.1.tar.gz
wget https://raw.githubusercontent.com/truatpasteurdotfr/docker-centos7-tensorflow/master/tf-c7.ans -O /tmp/tf-c6.ans
wget https://raw.githubusercontent.com/truatpasteurdotfr/docker-centos7-tensorflow/master/runme.sh  -O /tmp/runme.sh
cat /tmp/runme.sh | scl enable devtoolset-3 bash
