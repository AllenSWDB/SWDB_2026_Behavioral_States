# hash:sha256:7b05cd025460086671c9ea657c8148cf3a6f6a020e3e6443564af765adb082d9
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/swdb:Python3.12code-server4.133

ARG DEBIAN_FRONTEND=noninteractive
ARG GIT_ASKPASS
COPY git-ask-pass /

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential=12.9ubuntu3 \
    && rm -rf /var/lib/apt/lists/*

RUN pip install -U --no-cache-dir \
    dynamax[notebooks]==1.0.2 \
    ipykernel==7.3.0 \
    matplotlib==3.11.1 \
    pandas==3.0.5 \
    pynwb[zarr]==4.0.0
