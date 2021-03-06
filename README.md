# Docker and Kubernetes: The Complete Guide

This repository contains my solutions to the exercises from the *Docker and Kubernetes: The Complete Guide* course.

Course available at [Udemy](https://www.udemy.com/docker-and-kubernetes-the-complete-guide)

## Projects

- [***redis-server***](p1-redis-server/): Use a *redis:latest* image as a base image, download and install a dependency and tell the image what to do when it starts as a container.

- [***nodejs-app***](p2-nodejs-app/): A simple *node.js/express.js* "Hello world" application. Use a *node:10-alpine* as a base image and change the image's working directory, copy/install dependencies and run a default command.

- [***visits-app***](p3-visits-app/): A *node.js/express.js* application that counts the number of page visits. It uses two containers, one for the Node.js server and the other for Redis to store the number of page visits value.

- [***react-app***](p4-react-app/): A simple *react.js* application running on a container. It uses different containers for different working environments:
  - One container for the development environment which uses a *node:10-alpine* as a base image and runs a local development server via `npm run start` command.
  - One container for the testing environment which uses a *node:10-alpine* as a base image and runs the test suites via `npm run test` command.
  - One container for the production environment which uses a *node:10-alpine* as a base image and runs the production build process via `npm run build` command. And another container that uses `nignx:alpine` as a base image and run a `Nginx` web server to server the static content reside in the `build` folder.
- [***multi-container-app***](p5-multi-container-app/): Multi-container app which constists of three containers interacting together to save indices and compute fibonacci series of them. These containers are deployed in a Kuberenetes cluster and use Ingress services to interact with together.

## What I have learned

- Download and install *Docker* in different environments such as *Linux*, *Windows* and *MacOS*.
- Use ***Docker CLI*** to inspect and debug running containers.
- Build custom Docker images through the ***Docker Server***.
- Use ***Docker Compose*** to define and run multi-container *Docker* applications.
- Create and configure multi-step *Docker* builds.
- Use ***Kubernetes*** different objects such as Deployment, NodePort Service, ClusterIP Service, Ingress, etc. to deploy a fully functional application with multiple containers.
