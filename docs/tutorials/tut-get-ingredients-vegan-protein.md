# Find Ingredients with Specific Attributes

This tutorial guides you through filtering the GET /ingredients endpoint to find to find ingredients that meet multiple criteria.

This tutorial takes about 10 minutes to complete.

## Get Started

This tutorial requires a local JSON server to make API calls. Before you begin, please ensure your server is running. All API calls must be performed in a separate program or window, such as Postman or a command-line terminal for cURL. All examples use the base URL `http://localhost:3000`.

## Find Vegan Proteins

**Goal**: Find ingredients that are classified as both vegan and protein.
**Endpoint**: GET /ingredients

Use the endpoint and add query parameters to filter the results based on the `vegan` and `protein` properties.

### Example Request in cURL

1. Open a command-line tool such as Terminal or PowerShell.
2. Enter (or copy and paste) the following command, setting the URL in quotes to respect how command lines reserve the & character to control background operations.

    ```Bash
    curl -X GET "https://localhost:3000/ingredients?isVegan=true&category=protein"
    ```

### Example Request in Postman

1. Open Postman and set the method to `GET`.
2. Set the Request URL to `http://localhost:3000/ingredients`.
3. On the Params tab, enter the follow key-value pairs:
    * **Key**: `isVegan`, **Value**: `true`
    * **Key**: `category`, **Value**: `protein`
4. Click **Send**.

### Response

The request returns a 200 OK status and a JSON array containing the ingredient objects that match both of your criteria.

```JSON
[
  {
    "id": 7,
    "name": "Lentils",
    "category": "protein",
    "isVegan": true
  }
]
```
