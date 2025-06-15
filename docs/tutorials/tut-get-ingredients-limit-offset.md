# Paginate Results

When an API can return a large number of items, it often uses pagination to break the results into smaller, more manageable pages. This tutorial guide you through using the `limit` and `offset` parameters to fetch a specific page of results from the API.

## Get Started

This tutorial requires a local JSON server to make API calls. Before you begin, please ensure your server is running. All API calls must be performed in a separate program or window, such as Postman or a command-line terminal for cURL. All examples use the base URL `http://localhost:3000`.

## Fetch a Specific Page of Ingredients

**Goal**: Retrieve the second page of ingredients, assuming each page displays 5 items.
**Endpoint**: GET /ingredients

Use the endpoint and these query parameters to request the second page of ingredients:

* `limit=5`: Instructs the server to return a maximum of 5 items.
* `offset=5`: Instructs the server to skip the first 5 items before retrieving the results.

This combination retrieves items 6 through 10, which represents the second page.

### Example Request in cURL

1. Open a command-line tool such as Terminal or PowerShell.
2. Enter (or copy and paste) the following command. Place the URL in quotes to accommodate the "&" character.

    ```Bash
    curl -X GET "https://localhost:3000/ingredients?limit=5&offset=5"
    ```

### Example Request in Postman

1. Open Postman and set the method to `GET`.
2. Set the Request URL to `http://localhost:3000/ingredients`.
3. On the Params tab, enter the follow key-value pairs:
    * **Key**: `limit`, **Value**: `5`
    * **Key**: `offset`, **Value**: `5`
4. Click **Send**.

### Response

The request returns a 200 OK status and a JSON array containing the second page of ingredients.

```JSON


[
  {
    "id": 6,
    "name": "Whole Wheat Wrap",
    "category": "grain",
    "isVegan": true
  },
  {
    "id": 7,
    "name": "Lentils",
    "category": "protein",
    "isVegan": true
  },
  {
    "id": 8,
    "name": "Carrots",
    "category": "vegetable",
    "isVegan": true
  },
  {
    "id": 9,
    "name": "Vegetable Broth",
    "category": "liquid",
    "isVegan": true
  },
  {
    "id": 10,
    "name": "Rolled Oats",
    "category": "grain",
    "isVegan": true
  }
]
```
