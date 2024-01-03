## Inventory and Payment FastAPI Services

### Overview

This repository contains two FastAPI services, Inventory, and Payment, which are microservices communicating with each other. They provide basic functionalities for managing products, orders, and payments.

#### Features

- **Inventory Service:**
  - Create, delete, and manage products.
  - Exposes endpoints to interact with product inventory.
  
- **Payment Service:**
  - Handles order placement and payment processing.
  - Communicates with the Inventory service to manage orders.

#### Technologies Used

- **FastAPI:** FastAPI framework for building APIs with Python.
- **Redis:** Redis database used for storing product information and orders.
- **Frontend:** Simple frontend interface to interact with the services.

## Setup

#### Prerequisites

- Python 3.8+
- Redis Server


## Usage

#### Running the Services

1. Start the Inventory Service:

    ```bash
    uvicorn inventory.main:app --reload
    ```

2. Start the Payment Service:

    ```bash
    uvicorn payment.main:app --reload --port=8001
    ```

#### Interacting with the Services

- **Inventory Service Endpoints:** Access endpoints to manage products:
    - `http://localhost:8000/docs`: Swagger UI for API documentation.
    - `http://localhost:8000/products`: CRUD operations for products.

- **Payment Service Endpoints:** Place orders and process payments:
    - `http://localhost:8001/docs`: Swagger UI for API documentation.
    - `http://localhost:8001/orders`: Endpoint to place orders and process payments.

#### Frontend Interface

- Access the simple frontend interface to interact with the services:
    - Open `frontend/index.html` in a browser to use the basic interface.
