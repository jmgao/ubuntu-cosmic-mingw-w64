FROM jmgao/ubuntu-cosmic-mingw-w64:latest
MAINTAINER Josh Gao

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y --default-toolchain nightly-2019-05-06

ENV PATH "$PATH:/root/.cargo/bin"

RUN rustup target add i686-pc-windows-gnu && \
    rustup target add x86_64-pc-windows-gnu && \
    rustup component add rustfmt && \
    rustup component add clippy && \
    cargo install cbindgen
