# Plans resource

Contains information about the meal plans you can request from the MealMate service.
Currently, you can only request meal plans.

## Data Model

| Property| Data Type | Description |
|---|---|---|
| `id` | `integer`| Unique identifier for the meal plan |
| `name` | `string` | Name of the meal plan |
| `recipes` | `array of integers` | List of recipe IDs included in the meal plan |
| `diet` | `string` | Primary dietary classification (Examples: "mixed", "high-protein") |
| `duration` | `string` | The number of days that the meal plan lasts (Example: "3 days") |

## Code Example

```json
{
  "id": 1,
  "name": "Busy Week Vegetarian Plan",
  "recipes": [1, 3, 4],
  "diet": "vegetarian",
  "duration": "3 days"
}
```

## Other Links

[Home](../index.md)| [Setup](../mmprefland.md) | [Tutorials](../mmtutorial.md)
