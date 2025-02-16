# Dockerfile Optimization

This repository demonstrates an issue with an inefficient Dockerfile and provides an optimized solution.  The original Dockerfile uses `ubuntu:latest`, leading to slow build times and a large image size. The optimized version utilizes a smaller base image and only installs necessary dependencies. 

## Original Dockerfile

The original `Dockerfile` uses `ubuntu:latest` and installs unnecessary packages via `apt-get`.

## Optimized Dockerfile

The `DockerfileOptimized` demonstrates improvements:

* Uses a slimmer base image (`python:3.9-slim-buster`).
* Uses `pip` directly for installing requirements in a single `RUN` command.
* Avoids unnecessary package installations

These changes lead to faster builds and a smaller resulting Docker image.