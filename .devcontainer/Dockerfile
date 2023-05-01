# Note: You can use any Debian/Ubuntu based image you want. 
FROM mcr.microsoft.com/devcontainers/python:0-3.10

RUN pip install poetry \
# [Optional] Uncomment this section to install additional OS packages.
    && apt-get update && export DEBIAN_FRONTEND=noninteractive \
    # && apt-get -y install rustc
    # https://www.howtoforge.com/how-to-install-rust-programming-language-on-debian-11/
    && curl -sSf https://sh.rustup.rs | RUSTUP_HOME=/opt/rust CARGO_HOME=/opt/rust sh -s -- -y --no-modify-path
COPY ./rust.sh /etc/profile.d/rust.sh
