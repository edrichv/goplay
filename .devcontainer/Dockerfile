FROM --platform=linux/amd64 docker.io/rockylinux/rockylinux:9

ENV GO_VERSION=1.26.0
ENV GO_ARCHIVE=go${GO_VERSION}.linux-amd64.tar.gz

RUN dnf install -y \
    git \
    vim-minimal

RUN curl -LO https://go.dev/dl/${GO_ARCHIVE} \
    && tar xf ${GO_ARCHIVE} -C /usr/local/ \
    && rm -f ${GO_ARCHIVE}

ENV GOROOT=/usr/local/go
ENV GOPATH=/go
ENV PATH=${GOROOT}/bin:${PATH}