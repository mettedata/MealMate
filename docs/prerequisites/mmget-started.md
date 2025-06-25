# Get Started

The MealMate API is designed to be easy to use. Making your first call takes about 5 minutes.

## Before Your First Call

Ensure that you have your development environment set up and configured correctly [before you start][def] to use the MealMate API.

After you set up your development environment, follow this [quickstart](mmquickstart.md) guide to set up the MealMate API and start the service.

## Base URL and Authentication

<http://localhost:3000>

This is a local development URL for this project.
No authentication is required to us this API. You can make this request using cURL, Postman, or a tool like Postman.

## Data Format

The API uses JSON for all requests and responses.

## Your First Call

Let's start with a call to ensure you can connect to the MealMate API and retrieve data.

**Goal:** Fetch the complete list of ingredients available in the Meal

**Enpoint:** GET /ingredients

### Steps in cURL

1. Open a command-line application such as Terminal on macOS or PowerShell on Windows.
2. Enter (or copy and paste) the following command into the terminal window:

```Bash
curl -X GET http:localhost:3000/ingredients
```

### Steps in Postman

1. Set the method to GET.
2. Set the Request URL to `http://localhost:3000/ingredients`.

    This call requires no headers or body content.
3. Click **Send**.

### Expected Success Response

When your request is successful, the API returns a `200 OK` status and a JSON array of ingredient objects, similar to this:

```JSON
[
  { 
    "id": 1, 
    "name": "Broccoli", 
    "category": "vegetable", 
    "isVegan": true 
  },
  { 
    "id": 2, 
    "name": "Bell Pepper", 
    "category": "vegetable", 
    "isVegan": true 
  },
  { 
    "id": 3, 
    "name": "Soy Sauce", 
    "category": "condiment", 
    "isVegan": true 
  }
]
```

## Other Links

[Home](../index.md) | [Tutorials](../mmtutorial.md) | [Reference](../reference/)

[def]: mmbefore-you-start.md