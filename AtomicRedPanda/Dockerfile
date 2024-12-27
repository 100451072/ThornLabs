FROM ubuntu:latest

# Update and install necessary tools
RUN apt-get update && apt-get install -y \
    git \
    curl \
    python3 \
    python3-pip \
    nano

# Copy the local Atomic Red Team repo into the image
COPY ./atomic-red-team-master /atomic-red-team

# Set working directory
WORKDIR /atomic-red-team
