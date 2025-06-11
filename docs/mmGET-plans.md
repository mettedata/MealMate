# Plans

## GET /plans

`{base_url}/plans`

Provides a list of all available meal plans.

### Headers

None

### Path Parameters

None

### Query Parameters

The following query parameters are available to filter the results. All parameters are optional.

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `diet` | String | Optional | Filter plans by dietary classification (example: "vegetarian", "vegan"). |
| `duration`| String | Optional | Filter plans by their duration (e.g., "3 days"). |
| `limit` | Integer | Optional | The maximum number of plans to return. |
| `offset` | Integer | Optional | The number of plans to skip, used for pagination. |

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a collection of Plan objects. If no plans match the query, an empty collection is returned. |

### Plan Object

The `GET /plans` endpoint returns an array of Plan objects. Each object has the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | Integer | The unique identifier for the plan. | `1` |
| `name` | String | The name of the meal plan. | `"Busy Week Vegetarian Plan"` |
| `recipes`| Array of Integers | A list of recipe IDs included in the plan. | `[1, 3, 4]` |
| `diet` | String | The dietary classification of the plan. | `"vegetarian"` |
| `duration`| String | The duration of the plan. | `"3 days"` |

### Example

#### Example Request (cURL)

```sh
curl -X GET https://localhost:3000/plans
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/plans`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response

```json
[
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
  },
  {
    "id": 2,
    "name": "High-Protein Plan",
    "recipes": [
      2,
      3
    ],
    "diet": "high-protein",
    "duration": "2 days"
  }
]
```
