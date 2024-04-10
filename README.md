# Calculator Microservice

## Overview
This project is a simple calculator microservice built with Node.js and Express. It supports basic arithmetic operations such as addition, subtraction, multiplication, division, square root, exponentiation, and modulo.

## Steps

### Creating a Private Container Registry
Due to permission constraints with the Google Cloud Artifact Registry, Docker Hub was selected as an alternative solution to meet the project's requirement for a private container registry.

### Authentication
Docker Hub authentication was performed using the `docker login` command. This step is crucial for pushing images to the registry and ensuring secure access.

### Publishing the Docker Image
The Docker image was tagged and pushed to Docker Hub successfully. The commands used were:
- docker tag myapp:latest 221351413/myapp:latest
- docker push 221351413/myapp:latest

### Running the Microservice
The microservice was launched locally using Docker with the following command:
- docker run -p 3000:3000 --name my-micro0 --name my-microservice 221351413/myapp:latest

### Accessing the Application
After execution, the service was accessible via [http://localhost:3000](http://localhost:3000).

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
