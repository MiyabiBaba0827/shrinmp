FROM node:18-bullseye

# Update and install required tools
RUN apt-get update && apt-get install -y \
    sudo \
    curl \
    git \
    && rm -rf /var/lib/apt/lists/*

# Create vscode user with proper shell
RUN useradd -m -s /bin/bash -G sudo vscode && \
    echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER vscode

WORKDIR /workspace/nodejs