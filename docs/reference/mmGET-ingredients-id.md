# Ingredient by ID

## GET /ingredients/{id}

`{base_url}/ingredients/{id}`

Retrieves a specific ingredient by its unique ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `id` | `integer` | Required | The unique identifier for the ingredient.  |

### Query Parameters

None

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a single Ingredient object.  |
| `404 Not Found` | Returned if an ingredient with the specified ID does not exist.  |

### Ingredient Object

The endpoint returns a single Ingredient object with the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | `integer` | The unique identifier for the ingredient.  | `3` |
| `name` | `string` | The common name of the ingredient.  | `"Soy Sauce"` |
| `category`| `string` | The category the ingredient belongs to.  | `"condiment"` |
| `isVegan` | `boolean` | Indicates if the ingredient is vegan.  | `true` |

### Example (id = 3)

#### Example Request (cURL)

```sh
curl -X GET https://localhost:3000/ingredients/3
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/ingredients/3`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response (200 OK)

```json
{ 
  "id": 3, 
  "name": "Soy Sauce", 
  "category": "condiment", 
  "isVegan": true 
}
```

## Other Endpoints

* [GET /ingredients](../reference/mmGET-ingredients.md)
* [GET /recipes](../reference/mmGET-recipes.md)
* [GET /recipes by id](../reference/mmGET-recipes-id.md)
* [GET /plans](../reference/mmGET-plans.md)
* [GET /plans by id](../reference/mmGET-plans-id.md)

## Other Links

[Home](../index.md) | [Prerequisites](../mmprefland.md) | [Tutorials](../mmtutorial.md)
