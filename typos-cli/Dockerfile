# https://github.com/crate-ci/typos/blob/03286f0f825752c12a8521a4d2225b2f182f70b4/Dockerfile
ARG DEBIAN_DIST=bullseye

FROM rust:${DEBIAN_DIST} as builder
ARG TYPOS_CLI_VERSION=1.14.3
RUN cargo install typos-cli@${TYPOS_CLI_VERSION}

FROM debian:${DEBIAN_DIST}-slim
COPY --from=builder /usr/local/cargo/bin/typos /usr/local/bin/typos
ENTRYPOINT ["typos"]
CMD ["--help"]
