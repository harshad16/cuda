
FROM cuda:8.0-runtime-centos6
LABEL maintainer "NVIDIA CORPORATION <sw-cuda-installer@nvidia.com>"

ENV CUDNN_VERSION 7.1.2.21
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=a5dfd656811fe9c43d87c40338cec5e1a85ad5a9cd3b5f1e95dd67d5e126aacc && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.1.2/cudnn-8.0-linux-x64-v7.1.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-8.0-linux-x64-v7.1.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-8.0-linux-x64-v7.1.tgz -C /usr/local --wildcards 'cuda/lib64/libcudnn.so.*' && \
    rm cudnn-8.0-linux-x64-v7.1.tgz && \
    ldconfig
