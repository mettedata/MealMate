# MealMate Service Architecture

The MealMate API is a RESTful API, designed around predictable, resource-oriented URLs. It  uses standard HTTP to interact with these resources. The API is currently read-only. Key aspects of the RESTful design include:

* **CRUD Operations and HTTP Methods**: We use standard HTTP methods that correspond to Create, Read, Update, and Delete (CRUD) operations. As the API is currently read-only, it supports only the Read operation, which you can perform using the GET method. In the future, we plan to support Create (POST), Update (PUT), and Delete (DELETE) operations.

* **HTTP Status Codes**: The API uses standard HTTP status codes to communicate the success or failure of your requests. Examples: `200 OK` for a successful request, `404 Not Found` when a resource doesn't exist.

* **Statelessness**: The service doesn't store any client state between requests. Every request that you send to the API must contain all the information we need to process it.

## Authentication

The MealMate API is public and does not require any authentication.

* **No API Keys**: You don't need an API key, token, or  other form of authorization to access the data. You can make requests to MealMate endpoints directly.

* **HTTP Protocol**: You make all connections over `http://` and not `https://`. This means the connection is not encrypted. Since the API handles only public, non-sensitive data that is  read-only, this is currently sufficient.

## Data Format

The MealMate API sends and receives all data as JavaScript Object Notation (JSON).

**Request Headers**

Because the API is currently read-only (GET requests only), it doesn't require any specific headers with your requests. However, when we enable support for methods that send data (like POST or PUT), you'll be required to include a `Content-Type: application/json` header.

**Response Headers**

Expect a `Content-Type: application/json` header on all responses that you receive from the MealMate API.

## Base URL

All API endpoints are relative to a base URL. For local development and testing, use the following:

`http://localhost:3000`

**Example**: To access the list of all recipes, you make a GET request to:

`http://localhost:3000/recipes`

## Other Links

[Home](./index.md) | [Prerequisites](./mmprefland.md) | [Tutorials](./mmtutorial.md) | [Reference](./mmref.md)
