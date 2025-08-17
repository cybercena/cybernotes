A **Dockerfile** is a blueprint used to create a **Docker image**. It defines the base operating system image, required libraries and dependencies, source code, and other configurations. Dockerfiles use a **Domain-Specific Language (DSL)** and contain step-by-step instructions for building a Docker image. it should be create with filename ``Dockerfile`` without any extensions.

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerfile.png?raw=true)

Docker builds image by reading the instructions from a Dockerfile. The Dockerfile instructions syntax is defined by the specification reference in the [Dockerfile reference.](https://docs.docker.com/reference/dockerfile/)Here are the most common types of instructions:
| Instruction          | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| `FROM <base-image>`  | Sets the base image for your Docker image. Every image starts from a base, like Ubuntu or Python. |
| `RUN <commands>`     | Executes commands in a new layer on top of the current image and commits the results. Can be written in shell form or exec form. |
| `COPY <src> <dest>`  | Copies files or directories from your local machine into the image.                              |
| `WORKDIR <path>`     | Sets the working directory inside the container. All subsequent commands run from this location. |
| `ENV <key>=<value>`  | Defines environment variables inside the container.                                             |
| `EXPOSE <port>`      | Documents which port the container listens on at runtime.                                      |
| `CMD ["executable"]` | Specifies the default command to run when the container starts.                                |
### Example: Dockerfile for a Flask Web App

**Scenario:**  
We want to create a Flask web app using Ubuntu as the base image and run the application on port `8000`.

**Source code (`hello.py`):**

```python

from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello Comrades! Welcome to the Docker world"
```

The following Dockerfile creates a container image, which includes all the dependencies needed and automatically starts your application.

```Shell
#defining the base image for web app 
FROM ubuntu:22.04

# Install app dependencies
RUN apt-get update && apt-get install -y python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Install Flask
RUN pip3 install "flask==3.0.*"

# Copy application code
COPY hello.py /app/hello.py
WORKDIR /app

# Final configuration
ENV FLASK_APP=hello.py
EXPOSE 8000

CMD ["flask", "run", "--host=0.0.0.0", "--port=8000"]

```


