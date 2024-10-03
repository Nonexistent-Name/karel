# Start from the universal image
FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Set non-interactive frontend for apt to avoid interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Install openbox
RUN apt-get update && \
    apt-get -y install --no-install-recommends openbox && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set openbox to start automatically
RUN echo 'openbox-session &' >> ~/.xinitrc
