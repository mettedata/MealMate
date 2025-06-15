# Find a Specific Meal Plan

This tutorial guides you through using the GET /plans endpoint to find a meal plan that matches a specific diet and duration. This is useful for meal planners who have weekly planning requirements.

## Get Started

This tutorial requires a local JSON server to make API calls. Before you begin, please ensure your server is running. All API calls must be performed in a separate program or window, such as Postman or a command-line terminal for cURL. All examples use the base URL `http://localhost:3000`.

## Find a Meal Plan by Diet and Duration

**Goal**: Find 2 days of vegan meal plans.
**Endpoint**: GET /plans

Use the endpoint and add query parameters to filter the results based on the `diet` and `duration` properties.

### Example Request in cURL

1. Open a command-line tool such as Terminal or PowerShell.
2. Enter (or copy and paste) the following command, setting the URL in quotes to respect how command lines reserve the & character to control background operations. In addition, use `%20` to represent the space in "2 days."

    ```Bash
    curl -X GET "https://localhost:3000/plans?diet=vegan&duration=2%20days"
    ```

### Example Request in Postman

1. Open Postman and set the method to `GET`.
2. Set the Request URL to `http://localhost:3000/plans`.
3. On the Params tab, enter the follow key-value pairs:
    * **Key**: `diet`, **Value**: `vegan`
    * **Key**: `duration`, **Value**: `2 days`
4. Click **Send**.

### Response

The request returns a 200 OK status and a JSON array containing the plan objects that match your criteria.

```JSON
[
  {
    "id": 3,
    "name": "Quick Start Vegan Plan",
    "recipes": [
      3,
      4
    ],
    "diet": "vegan",
    "duration": "2 days"
  }
]
```
