
FROM cuda:11.1-devel-centos7
LABEL maintainer "NVIDIA CORPORATION <sw-cuda-installer@nvidia.com>"

ENV CUDNN_VERSION 8.0.4.30
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

RUN yum install -y \
    libcudnn8-devel-${CUDNN_VERSION}-1.cuda11.1 \
    && yum clean all \
    && rm -rf /var/cache/yum/*
