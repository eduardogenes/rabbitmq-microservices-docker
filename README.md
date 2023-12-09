# Microservices with RabbitMQ Docker Compose

This repository contains a Docker Compose setup for microservices using RabbitMQ as a message broker.

## Services

- **rabbitmq:** RabbitMQ container with management interface.
- **ms-escrita:** Microservice for writing messages to the RabbitMQ queue.
- **ms-leitura:** Microservice for reading messages from the RabbitMQ queue.

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. Clone this repository.
2. Navigate to the repository folder.
3. Run `docker-compose up -d` to start the services.

## Usage

- **Sending Messages (ms-escrita):** This microservice generates and sends messages to the RabbitMQ queue at regular intervals. The messages contain information about the application, a timestamp, and a randomly generated sentence.

- **Receiving Messages (ms-leitura):** This microservice consumes messages from the RabbitMQ queue. It simulates processing time by sleeping for a random duration before acknowledging the message.

## Challenges Faced

### 1. Docker Compose Configuration

- Understanding the structure of the `docker-compose.yml` file, including service dependencies and environment variables.

### 2. RabbitMQ Connection

- Configuring RabbitMQ connections in Python scripts (`ms-escrita.py` and `ms-leitura.py`), including setting up credentials and connection parameters.

### 3. Message Generation and Processing

- Implementing message generation in a readable format (`ms-escrita.py`) and simulating message processing delays (`ms-leitura.py`).

### 4. Environment Variables

- Managing environment variables for Docker Compose services and Python scripts, ensuring consistency and security.

## Tips for Study

- **Docker Compose:** Familiarize yourself with the structure of the `docker-compose.yml` file, and understand how services, networks, and volumes are defined.

- **RabbitMQ:** Learn the basics of RabbitMQ, including setting up queues, exchanges, and understanding message broker concepts.

- **Python and Pika:** Explore the Pika library for interacting with RabbitMQ in Python. Understand how to declare queues, publish messages, and consume messages asynchronously.

Feel free to customize the services and configurations based on your requirements.

## Contributing

If you'd like to contribute or have suggestions, please open an issue or create a pull request.


