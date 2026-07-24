# hash:sha256:8d9839ca9da895b89e92e9c55f56720c756095067b598222962df586e08a2b8d
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
    pynwb==4.0.0
