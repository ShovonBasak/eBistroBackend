# syntax=docker/dockerfile:1.4

FROM mcr.microsoft.com/devcontainers/base:jammy

EXPOSE 8000

# Install pip
RUN apt-get update && apt-get install -y python3-pip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace

RUN pip install poetry

COPY pyproject.toml poetry.lock ./