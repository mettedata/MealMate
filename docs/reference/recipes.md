# Recipes resource (draft)

Contains the ingredient combinations, diet type, and instructions for making a meal.
Currently, you can only request recipes.

## Data Model

| Property| Data Type | Description |
|---|---|---|
| `id` | `integer`| Unique identifier for the recipe |
| `title` | `string` | Name of the recipe |
| `ingredients` | `array of integers` | List of ingredient IDs required for the recipe |
| `diet` | `string` | Dietary classification (Examples: "vegetarian", "high-protein") |
| `prepTime` | `integer` | Estimated preparation time in minutes |
| `instructions` | `string` | Brief, basic steps to combine ingredients and prepare the recipe |

## Code Example

```json
{
  "id": 1,
  "title": "Quick Veggie Stir Fry",
  "ingredients": [1, 2, 3],
  "diet": "vegetarian",
  "prepTime": 15,
  "instructions": "Stir-fry vegetables in sesame oil and add soy sauce to taste."
}
```

## Other Links

[Home](../index.md)| [Prerequisites](../mmprefland.md) | [Tutorials](../mmtutorial.md)
