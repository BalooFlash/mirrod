# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.224.2/containers/rust/.devcontainer/base.Dockerfile

# [Choice] Debian OS version (use bullseye on local arm64/Apple Silicon): buster, bullseye
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/rust:0-${VARIANT}

RUN rustup toolchain install nightly-x86_64-unknown-linux-gnu && rustup component add rustfmt --toolchain nightly-x86_64-unknown-linux-gnu && rustup component add clippy --toolchain nightly-x86_64-unknown-linux-gnu
RUN apt-get update && apt-get install -y clang
RUN curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.16.0/kind-linux-amd64 && chmod +x ./kind && mv ./kind /usr/local/bin/kind
