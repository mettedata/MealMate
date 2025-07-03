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
| `name` | `string` | Optional | Search for an ingredient by its name. |
| `category`| `string` | Optional | Filter ingredients by category (Examples: "vegetable", "protein"). |
| `isVegan` | `boolean` | Optional | Filter ingredients by their vegan status (`true` or `false`). |
| `limit` | `integer` | Optional | The maximum number of ingredients to return. |
| `offset` | `integer` | Optional | The number of ingredients to skip. Used for pagination when making subseqent API calls. |

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a collection of Ingredient objects. If no ingredients match the query, an empty collection is returned. |
| `404 Not Found` | Returned if an ingredient with the specified ID does not exist. |

### Ingredient Object

The `GET /ingredients` endpoint returns an array of Ingredient objects. Each object has the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | `integer` | The unique identifier for the ingredient. | `1` |
| `name` | `string` | The common name of the ingredient. | `"Broccoli"` |
| `category`| `string` | The category the ingredient belongs to. | `"vegetable"` |
| `isVegan` | `boolean` | Indicates if the ingredient is vegan. | `true` |

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

## Other Endpoints

* [GET /ingredients by id](../reference/mmGET-ingredients-id.md)
* [GET /recipes](../reference/mmGET-recipes.md)
* [GET /recipes by id](../reference/mmGET-recipes-id.md)
* [GET /plans](../reference/mmGET-plans.md)
* [GET /plans by id](../reference/mmGET-plans-id.md)

## Other Links

[Home](../index.md) |  [App Considerations](../mmoverview.md)  | [Architecture](../mmarchitecture.md) | [Diagrams](../mmdiagrams.md)  | [Setup](../mmprefland.md) | [Tutorials](../mmtutorial.md)  |  [Reference](../mmref.md)
