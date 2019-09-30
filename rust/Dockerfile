FROM jmgao/ubuntu-cosmic-mingw-w64:latest
MAINTAINER Josh Gao

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y --default-toolchain nightly-2019-09-28

ENV PATH "$PATH:/root/.cargo/bin"

RUN rustup toolchain add stable && \
    rustup target add i686-pc-windows-gnu && \
    rustup target add x86_64-pc-windows-gnu && \
    rustup component add rustfmt && \
    rustup component add clippy && \
    cargo install cbindgen
