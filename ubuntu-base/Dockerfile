FROM --platform=amd64 mcr.microsoft.com/devcontainers/base:jammy
RUN sudo apt update && sudo apt upgrade -y
RUN sudo apt install python3 python3-pip git -y
RUN sudo apt clean && sudo rm -rf /var/lib/apt/lists/*
RUN sudo pip3 cache purge