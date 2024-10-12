# Product Service

The **Product Service** handles product catalog management, including product listings, details, search, and filtering for the e-commerce platform.

## Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Running the Service](#running-the-service)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)

## Features

- **Product Listings:** Provides a list of all available products in the catalog.
- **Product Details:** Retrieves detailed information for a specific product.
- **Search and Filtering:** Allows users to search for products by keyword and filter by attributes like price or category.
- **Inventory Management:** Tracks product stock and updates inventory levels.

## Technology Stack

- **Language:** Python
- **Framework:** Flask or FastAPI
- **Database:** PostgreSQL
- **Containerization:** Docker

## Prerequisites

- **Python** 3.8 or higher
- **pip** package installer
- **PostgreSQL** 12 or higher
- **Docker** (optional, for containerization)

## Installation

1. **Clone the repository:**

  ```bash
git clone https://github.com/your-username/product-service.git
cd product-service

2. **Install Dependencies:**

  ```bash
pip install -r requirements.txt
```

3. **Environment Variables:**
Create a .env file in the root directory and add the following environment variables:

 ```dotenv
PORT=5000
DATABASE_URL=postgresql://user:password@localhost:5432/productdb
PORT: The port number on which the service will run.
DATABASE_URL: PostgreSQL connection string.
```

4. **Running Docker:**

Build the docker image:

 ```bash
docker build -t product-service:latest .
 ```
***Run the Docker container:***

 ```bash
docker run -p 5000:5000 --env-file .env product-service:latest
 ```
The service should now be accessible at http://localhost:5000

5. **API Endpoints:**
   
***Get all products***
* Endpoint: GET /api/v1/products
* Description: Retrieves a list of all products.
***Get product by ID***
* Endpoint: GET /api/v1/products/{product_id}
* Description: Retrieves details of a specific product.
***Search products***
* Endpoint: GET /api/v1/products/search?q=keyword
* Description: Searches for products matching the keyword.

6. **Testing:**
* Run unit tests using:
```bash
pytest
```
 This command will execute all tests located in the tests directory.

