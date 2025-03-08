FROM mcr.microsoft.com/devcontainers/base:1.0.19-bookworm

ARG AIDER_VERSION=0.75.2

# May not be able to use ARG for uv version?
COPY --from=ghcr.io/astral-sh/uv:0.6.5 /uv /uvx /usr/local/bin/

USER vscode

RUN uv tool install --force --python python3.12 aider-chat@${AIDER_VERSION}
