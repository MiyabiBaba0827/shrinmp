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

# Set npm permissions to avoid EACCES errors
RUN mkdir -p /home/vscode/.npm && \
    chown -R vscode:vscode /home/vscode/.npm

# Ensure workspace directories exist and have proper permissions
RUN mkdir -p /workspace/nodejs && \
    chown -R vscode:vscode /workspace

USER vscode

WORKDIR /workspace/nodejs

# Clean npm cache
RUN npm cache clean --force