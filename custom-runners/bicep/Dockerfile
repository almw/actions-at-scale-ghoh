#  azure-cli:latest
FROM mcr.microsoft.com/azure-cli:latest
LABEL maintainer="support@techtrend.us"
# install bicep
RUN curl -Lo bicep.bin https://github.com/Azure/bicep/releases/latest/download/bicep-linux-musl-x64 \
 && chmod +x ./bicep.bin \
 && mv ./bicep.bin /usr/local/bin/bicep \
 && bicep --version

# GHES actions-runner
FROM summerwind/actions-runner:latest

# This will be a good place to add your CA bundle if you're using
# a custom CA.

# If you have proxy configurations, you can also add them here

# Change the work dir to tmp because these are disposable files
WORKDIR /tmp

