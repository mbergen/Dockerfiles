FROM alpine:latest

LABEL maintainer="mbergen@tzi.de"

# Base
RUN apk add --no-cache bash git build-base curl cmake ninja tar
RUN apk add --no-cache alpine-sdk linux-headers lsb-release-minimal

# Libraries
# boost
RUN apk add --no-cache boost-dev

#or-tools
RUN curl -Lo or-tools.tar.gz https://github.com/google/or-tools/releases/download/v9.6/or-tools_amd64_alpine-edge_cpp_v9.6.2534.tar.gz \
    && mkdir -p /usr/local/bin/or-tools \
    && tar -xzf or-tools.tar.gz -C /usr/local/bin/or-tools --strip-components=1 \
    && ls /usr/local/bin \
    && cd /usr/local/bin/or-tools \
    && make test \
    && cd -
RUN rm or-tools.tar.gz

CMD ["bash"]