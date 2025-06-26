# Recipe by ID

## GET /recipes/{id}

`{base_url}/recipes/{id}`

Retrieves a specific recipe by its unique ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| `id` | `integer` | Required | The unique identifier for the recipe. |

### Query Parameters

None

### Request Body

None

### Responses

| Code | Description |
| --- | --- |
| `200 OK` | Returns a single Recipe object. |
| `404 Not Found` | Returned if a recipe with the specified ID does not exist. |

### Recipe Object

The endpoint returns a single Recipe object with the following properties:

| Property Name | Data Type | Description | Example Value |
| --- | --- | --- | --- |
| `id` | `integer` | The unique identifier for the recipe. | `2` |
| `title` | `string` | The name of the recipe. | `"Chicken Avocado Wrap"` |
| `ingredients`| `array of integers` | A list of ingredient IDs used in the recipe. | `[4, 5, 6]` |
| `diet` | `string` | The dietary classification of the recipe. | `"high-protein"` |
| `prepTime`| `integer` | The preparation time in minutes. | `10` |
| `instructions`| `string` | The brief, basic steps to prepare the recipe. | `"Layer cooked chicken, avocado, and greens in a whole wheat wrap."` |

### Example (id = 2)

#### Example Request (cURL)

```sh
curl -X GET https://localhost:3000/recipes/2
```

#### Example Request (Postman)

* **Method**: GET
* **Request URL**: `https://localhost:3000/recipes/2`
* **Headers**: No specific headers are required.
* **Body**: No body is needed for a GET request.
* Click **Send**.

#### Example Response (200 OK)

```json
{
  "id": 2,
  "title": "Chicken Avocado Wrap",
  "ingredients": [
    4,
    5,
    6
  ],
  "diet": "high-protein",
  "prepTime": 10,
  "instructions": "Layer cooked chicken, avocado, and greens in a whole wheat wrap."
}
```

## Other Links

[Home](../index.md) | [Prerequisites](../mmprefland.md) | [Tutorials](../mmtutorial.md)
