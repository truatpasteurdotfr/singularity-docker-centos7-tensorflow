# singularity-docker-centos7-tensorflow
singularity recipe for bootstrapping a tensorflow build container from a centos:centos7 docker image

```
sudo singularity create -s 3600 singularity-docker-centos7-tensorflow.img
sudo singularity bootstrap singularity-docker-centos7-tensorflow.img Singularity
