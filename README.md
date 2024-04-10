# Calculator Microservice

## Overview
This project is a simple calculator microservice built with Node.js and Express. It supports basic arithmetic operations such as addition, subtraction, multiplication, division, square root, exponentiation, and modulo.

## Steps:

1. **Creating a Private Container Registry**: Due to permission constraints with Google Cloud, Docker Hub was chosen as an alternative for hosting the private container registry

2. **Authentication**: Used `docker login` to authenticate with Docker Hub, which is analogous to authenticating with Google Cloud's Artifact Registry

3. **Building the Docker Image**: Constructed a Docker image of the microservice using the `Dockerfile` present in the repository and the command `docker build -t myapp:latest .`

4. **Tagging the Docker Image**: Tagged the Docker image for pushing to Docker Hub using `docker tag myapp:latest 221351413/myapp:latest`

5. **Publishing the Image**: Successfully pushed the Docker image to Docker Hub with `docker push 221351413/myapp:latest`

6. **Running the Microservice**: Launched the microservice locally using `docker run -p 3000:3000 --name my-microservice 221351413/myapp:latest` to ensure that it was working correctly. The microservice is now accessible at `http://localhost:3000`
   
## Operations
The service supports the following operations:
- Addition: `/add?num1={number}&num2={number}`
- Subtraction: `/subtract?num1={number}&num2={number}`
- Multiplication: `/multiply?num1={number}&num2={number}`
- Division: `/divide?num1={number}&num2={number}`
- Square Root: `/sqrt?num={number}`
- Exponentiation: `/power?num1={number}&num2={number}`
- Modulo: `/modulo?num1={number}&num2={number}`

Replace `{number}` with actual numbers to perform calculations.
