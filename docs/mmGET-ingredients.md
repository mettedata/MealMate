# Ingredients

## GET /ingredients

`{base_url}/ingredients`

Provides a list of all common pantry items available in the MealMate database.

### Headers

None

### Path Parameters

None

### Query Parameters

The following query parameters are available to filter the results. All parameters are optional.

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `name` | String | Optional | Search for an ingredient by its name. |
| `category`| String | Optional | Filter ingredients by category (e.g., "vegetable", "protein"). |
| `isVegan` | Boolean | Optional | Filter ingredients by their vegan status (`true` or `false`). |
| `limit` | Integer | Optional | The maximum number of ingredients to return. |
| `offset` | Integer | Optional | The number of ingredients to skip, used for pagination. |

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a collection of Ingredient objects. If no ingredients match the query, an empty collection is returned. |

### Ingredient Object

The `GET /ingredients` endpoint returns an array of Ingredient objects. Each object has the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | Integer | The unique identifier for the ingredient. | `1` |
| `name` | String | The common name of the ingredient. | `"Broccoli"` |
| `category`| String | The category the ingredient belongs to. | `"vegetable"` |
| `isVegan` | Boolean | Indicates if the ingredient is vegan. | `true` |

### Example

#### Example Request (cURL)

```sh
curl -X GET https://localhost:3000/ingredients
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/ingredients`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response

```json
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
