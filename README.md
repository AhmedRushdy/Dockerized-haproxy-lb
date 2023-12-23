# Load Balancer with Docker and Docker Compose

## Introduction

In this project, we will learn how to balance traffic load across multiple microservices using a simple round-robin load balancing algorithm. The load balancer will be built using Docker and orchestrated with Docker Compose.

## How it Works

1. The client sends a request to the load balancer's domain.
2. The load balancer receives the request and determines the next microservice to forward the request to based on a round-robin algorithm.
3. The load balancer forwards the request to the selected microservice.
4. The microservice processes the request and sends the response back to the load balancer.
5. The load balancer relays the response back to the client.

## Prerequisites

Make sure you have the following installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. Clone this repository to your local machine.

2. Navigate to the project directory.

3. Open the `docker-compose.yml` file and update the services section with the microservices you want to load balance. Add or remove services as needed.

4. Run the following command to build the Docker images and start the containers:

   ```shell
   docker-compose up -d