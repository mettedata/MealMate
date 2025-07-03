# Ingredients resource

Contains the common pantry items that make up recipes. Currently, you can only request ingredients.

## Data Model

| Property| Data Type | Description |
|---|---|---|
| `id` | `integer`| Unique identifier for the ingredient |
| `name` | `string` | Name of the ingredient |
| `category` | `string` | Food group of the ingredient (Examples: "vegetable", "protein") |
| `isVegan` | `boolean` | `true` if the ingredient is vegan, `false` otherwise |

## Code Example

```json
{
  "id": 1,
  "name": "Broccoli",
  "category": "vegetable",
  "isVegan": true
}
```

## Other Links

[Home](../index.md)| [Setup](../mmprefland.md) | [Tutorials](../mmtutorial.md)
