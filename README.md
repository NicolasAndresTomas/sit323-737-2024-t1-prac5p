# Calculator Microservice

## Overview

This project is a simple calculator microservice built with Node.js and Express. It supports basic arithmetic operations such as addition, subtraction, multiplication, division, square root, exponentiation, and modulo.

## Build and Run

To build and run the application using Docker, follow these steps:

1. Build the Docker image:
- docker build -t my-web-app .

2. Run the Docker container:
- docker run -p 3000:3000 my-web-app

3. Alternatively, use Docker Compose to build and run the service:
- docker-compose up

## Accessing the Application

After starting the service, access the application at [http://localhost:3000](http://localhost:3000).

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
