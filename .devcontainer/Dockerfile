FROM mcr.microsoft.com/devcontainers/base:1.0.19-bookworm

ARG AIDER_VERSION=0.72.0

# May not be able to use ARG for uv version?
COPY --from=ghcr.io/astral-sh/uv:0.5.24 /uv /uvx /usr/local/bin/

RUN uv tool install --force --python python3.12 aider-chat==${AIDER_VERSION}

LABEL org.opencontainers.image.version=${AIDER_VERSION}
