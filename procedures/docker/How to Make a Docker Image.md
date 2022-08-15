# Introduction
Docker container images are created by service providors and the community and exist for many services. These images lower the development needed for service deployment and are often supported by the image owner for version upgrades and security patching. The downside to these public images are that you have less control over how the image was made, what packages are included and how the container is configured/managed.

Custom Docker container images address the security and control constraints of public images as you are in full control of the image from start to finish. You can start with a scratch base image or a base image you trust, build out the container the way you want it made and then build the container into an image. A few downsides to custom images are that it takes development time to create, you need to inventory and monitor the packages in your container, manually upgrade your services and personally patch security vulnerabilities.

A middle ground between public and custom images can be using a base image you trust and 

## Using a Dockerfile
- TBD

## Using a Docker Container
- TBD
---
- For more information, see the [docker glossary](https://github.com/brian-tex/public-documentation/blob/main/reference/docker/glossary.md).
