# Plan by ID

## GET /plans/{id}

`{base_url}/plans/{id}`

Retrieves a specific meal plan by its unique ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `id` | Integer | Required | The unique identifier for the meal plan. |

### Query Parameters

None

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a single Plan object. |
| `404 Not Found` | Returned if a plan with the specified ID does not exist. |

### Plan Object

The endpoint returns a single Plan object with the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | Integer | The unique identifier for the plan. | `1` |
| `name` | String | The name of the meal plan. | `"Busy Week Vegetarian Plan"` |
| `recipes`| Array of Integers | A list of recipe IDs included in the plan. | `[1, 3, 4]` |
| `diet` | String | The dietary classification of the plan. | `"vegetarian"` |
| `duration`| String | The duration of the plan. | `"3 days"` |

### Example (id = 1)

#### Example Request (cURL)

```sh
curl -X GET https://localhost:3000/plans/1
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/plans/1`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response (200 OK)

```json
{
  "id": 1,
  "name": "Busy Week Vegetarian Plan",
  "recipes": [
    1,
    3,
    4
  ],
  "diet": "vegetarian",
  "duration": "3 days"
}
```
