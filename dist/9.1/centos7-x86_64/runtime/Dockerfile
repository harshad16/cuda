
FROM cuda:9.1-base-centos7

LABEL maintainer "NVIDIA CORPORATION <sw-cuda-installer@nvidia.com>"

RUN yum install -y \
    cuda-libraries-$CUDA_PKG_VERSION \
    && yum clean all \
    && rm -rf /var/cache/yum/*

