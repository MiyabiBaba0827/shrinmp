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
    npm config set prefix /home/vscode/.npm && \
    chown -R vscode:vscode /home/vscode/.npm

USER vscode

WORKDIR /workspace/nodejs

# Clean npm cache and set safe permissions
RUN npm cache clean --force