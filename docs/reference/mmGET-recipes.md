# Recipes

## GET /recipes

`{base_url}/recipes`

Provides a list of available recipes, which can be filtered by various criteria.

### Headers

None

### Path Parameters

None

### Query Parameters

The following query parameters are available to filter the results. All parameters are optional.

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `diet` | String | Optional | Filter recipes by dietary classification (example: "vegetarian", "vegan"). |
| `prepTime`| Integer | Optional | Filter for recipes with a preparation time less than or equal to the specified value (in minutes). |
| `ingredients` | String | Optional | Filter for recipes containing specific ingredients. (Note: Filtering logic may vary). |
| `limit` | Integer | Optional | The maximum number of recipes to return. |
| `offset` | Integer | Optional | The number of recipes to skip, used for pagination. |

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a collection of Recipe objects. If no recipes match the query, an empty collection is returned. |

### Recipe Object

The `GET /recipes` endpoint returns an array of Recipe objects. Each object has the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | Integer | The unique identifier for the recipe. | `1` |
| `title` | String | The name of the recipe. | `"Quick Veggie Stir Fry"` |
| `ingredients`| Array of Integers | A list of ingredient IDs used in the recipe. | `[1, 2, 3]` |
| `diet` | String | The dietary classification of the recipe. | `"vegetarian"` |
| `prepTime`| Integer | The preparation time in minutes. | `15` |
| `instructions`| String | The steps to prepare the recipe. | `"Stir-fry vegetables in sesame oil and add soy sauce to taste."` |

### Example

#### Example Request (cURL)

```sh
curl -X GET "https://localhost:3000/recipes?diet=vegetarian&prepTime=15"
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/recipes`
* **Params Tab**:
    * Key: `diet`, Value: `vegetarian`
    * Key: `prepTime`, Value: `15`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response

```json
[
  {
    "id": 1,
    "title": "Quick Veggie Stir Fry",
    "ingredients": [
      1,
      2,
      3
    ],
    "diet": "vegetarian",
    "prepTime": 15,
    "instructions": "Stir-fry vegetables in sesame oil and add soy sauce to taste."
  },
  {
    "id": 4,
    "title": "Overnight Oats",
    "ingredients": [
      10,
      11,
      12
    ],
    "diet": "vegetarian",
    "prepTime": 5,
    "instructions": "Combine oats, milk, and fruit. Refrigerate overnight."
  }
]
```

## Other Links

[Home](../index.md) | [Prerequisites](../mmprefland.md) | [Tutorials](../mmtutorial.md)
