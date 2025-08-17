Before learning about Docker, we need to know why Docker is needed. Imagine there is  company that is developing a website for client Ram. Developers made a fully functional website on his Mac and sent the source code to Ram. But when Ram tries to open the website on his local machine (Windows), it doesn't work. When Ram complains about the issue to company, the developer says, "It's working on my machine." This is all because of different OS, different versions of packages, and code environment.

![Most Common Problem of IT industry](https://github.com/cybercena/Static-assets/blob/main/Docker/its_working.png?raw=true)

## Concept of Containerization

During development, we use different libraries, tools, and dependencies. Whenever we try to use the same source code on a different machine, we need to manually install those tools and dependencies. Sometimes, even after installing them, the software doesn’t run due to OS-level dependencies.

To address this problem, the concept of virtualization was introduced. However, virtualization often consumes a large amount of system resources. To overcome this limitation, Docker and the concept of containerization were later introduced as a more lightweight and efficient solution.

![Virtualization vs Container](https://github.com/cybercena/Static-assets/blob/main/Docker/virtualization_vs_container.png?raw=true)

## Docker File

A **Dockerfile** is a blueprint used to create a **Docker image**. It defines the base operating system image, required libraries and dependencies, source code, and other configurations. Dockerfiles use a **Domain-Specific Language (DSL)** and contain step-by-step instructions for building a Docker image. it should be create with filename ``Dockerfile`` without any extensions.

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Docker/dockerfile.png)


## Docker Image 

A **Docker image** is a lightweight, read-only package that contains everything needed to run a piece of software. It includes the application code, runtime, libraries, dependencies, and configuration. You can create a Docker image using a **Dockerfile**. Once built, a Docker image can be shared and reused across different environments. When you run a Docker image, it becomes a **container** (a running instance of that image).

## Docker Container

A **Docker container** is like a small, lightweight box that holds everything your application needs to run. It is created from a Docker image and runs as an isolated process on your computer or server. Containers make sure the app runs the same way everywhere, whether on your laptop, in testing, or in production.

