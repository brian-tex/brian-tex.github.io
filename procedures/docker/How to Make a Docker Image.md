# Introduction
### Docker Hub Container Images
- These are created by service providors and the community and exist for many services. These images lower the development needed for service deployment and are often supported by the image owner for version upgrades and security patching. The downside to these public images are that you have less control over how the image was made, what packages are included and how the container is configured/managed.

### Custom Docker Container Images
- These address the security and control constraints of public images as you are in full control of the image from start to finish. You can start with a scratch base image or a base image you trust, build out the container the way you want it made and then build the container into an image. A few downsides to custom images are that it takes development time to create, you need to inventory and monitor the packages in your container, manually upgrade your services and personally patch security vulnerabilities.

### A Middle Ground
1. Build an idempotent script that applies common best practices.
1. Download the public container image.
1. Run a vulnerability check against the image to identify vulerable packages.
1. Create a container using a public image.
1. Connect to the container and patch any vulnerabilities and apply your best practices script.
1. Build the container as a custom image and save it to Docker Hub.

## Image Creation Using a Dockerfile
1. Create an empty directory for your custom image.
1. ``cd`` into the new directory. 
1. Locate the Dockerfile you wish to use ([create one if needed](https://github.com/brian-tex/public-documentation/blob/main/procedures/docker/How%20to%20Create%20a%20Dockerfile.md)) and move it into the new directory.
1. Move all directories, scripts, files, etc. needed by the Dockerfile (if applicable) into the new directory.
1. Get your Docker Hub username.
1. Identify what you want to name your image.
1. Identify what tag you wish to use for this specific build. It usually starts as ```01``` ad iterates with each build.
1. Run the following: ```docker build -t <yourDockerHubUsername>/<yourDesiredImageName>:<tag>```
    - e.g., ```docker build -t johnb1/nextcloud:01```
1. List out all Docker images on your computer: ```docker images```
1. Locate your newly craeted image and note the container image number associated with it.

## Image Creation Using a Docker Container
- TBD
---
- For more information, see the [docker glossary](https://github.com/brian-tex/public-documentation/blob/main/reference/docker/glossary.md).
