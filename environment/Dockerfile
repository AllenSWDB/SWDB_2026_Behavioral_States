# hash:sha256:af9883cba13dd53ce225545bcf17e488f0de8bf641c3817a308071ed9d28a138
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/code-server-python-extensions-pack:v5.0

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
