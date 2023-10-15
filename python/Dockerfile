FROM --platform=amd64 python:latest
RUN apt update && apt upgrade
RUN apt install -y git python3-pip
RUN apt clean && rm -rf /var/lib/apt/lists/*
RUN pip3 cache purge