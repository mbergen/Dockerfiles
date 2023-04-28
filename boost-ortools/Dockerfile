FROM alpine:latest

LABEL maintainer="mbergen@tzi.de"

# Base
RUN apk add --no-cache bash git build-base curl cmake ninja tar
RUN apk add --no-cache alpine-sdk linux-headers lsb-release-minimal

# Libraries
# boost
RUN apk add --no-cache boost-dev

#or-tools
RUN apk add --no-cache zlib-dev protobuf-dev
RUN git clone https://github.com/google/or-tools.git \
    && cd or-tools \
    && cmake -S. -Bbuild -G "Ninja" -DCMAKE_BUILD_TYPE=Release -DBUILD_DEPS=ON -DBUILD_SAMPLES=OFF -DBUILD_SAMPLE=OFF -DBUILD_EXSAMPLES=OFF\
    && cmake --build build --config Release -v \
    && cmake --build build --target install
RUN rm -rf or-tools

CMD ["bash"]