# Raya Challenge

A challenge for a DevOps Internship.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Screenshots](#screenshots)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Docker
- Docker Compose

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ahmaddfathyy/RayaGate-Challenge
   cd RayaGate-Challenge
   ```

2. Create a certs directory and generate a self-signed SSL certificate:

  ```bash
  mkdir -p ./certs
  openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./certs/nginx-selfsigned.key -out ./certs/nginx-selfsigned.crt
  ```

3. Run the application using Docker Compose:

  ```bash
  docker-compose up --build
  ```

## Usage

Access the application at:

- HTTP: http://localhost
- HTTPS: https://localhost (self-signed certificate warning may appear)

## Screenshots
https://github.com/ahmaddfathyy/RayaGate-Challenge/sc/sc.png