FROM mcr.microsoft.com/devcontainers/base:1.0.19-bookworm

ARG AIDER_VERSION=0.75.2

COPY --from=ghcr.io/astral-sh/uv:0.6.5 /uv /uvx /usr/local/bin/

# Used for goose
RUN apt-get update && apt-get install -y libxcb1 libdbus-1-3

# Install Node.js latest LTS
RUN curl -fsSL https://deb.nodesource.com/setup_22.x | bash - && \
    apt-get install -y nodejs

USER vscode

RUN uv tool install --force --python python3.12 aider-chat@${AIDER_VERSION}

RUN cd $HOME && curl -fsSL https://github.com/block/goose/releases/download/stable/download_cli.sh | CONFIGURE=false bash
