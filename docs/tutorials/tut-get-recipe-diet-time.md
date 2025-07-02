# Find a Quick Vegetarian Recipe

The MealMate API can help you find recipes that match specific needs, such as dietary restrictions and how much time you have to cook. This tutorial will walk you through filtering the API's recipes to find a vegetarian meal that can be prepared in 15 minutes or less.

This tutorial takes about 10 minutes to complete.

## Get Started

This tutorial requires a local JSON server to make API calls. Before you begin, please ensure your server is running. All API calls must be performed in a separate program or window, such as Postman or a command-line terminal for cURL.

## Find a Recipe by Diet and Time

ou can find the recipe using an API client like Postman or a command-line tool like cURL.

### Using Postman

1. Open Postman.
2. Set the method to `GET`.
3. On the Params tab, enter the query parameters:
    * Key: `diet`, Value: `vegetarian`
    * Key: `prepTime`, Value: `15`
4. Enter the URL:
    `http:localhost:3000/recipes`.
5. Click **Send**.

### Using cURL

1. Open your command-line terminal.
2. Enter the following command, setting the URL in quotes to respect how command lines reserve the & character to control background operations.

    ```Bash
    curl -X GET "http://localhost:3000/recipes?diet=vegetarian&pepTime=15"`
    ```

## Expected Response

For both Postman and cURL, the API returns a JSON array of recipe objects that match your criteria:

```json
[
  {
    "id": 1,
    "title": "Quick Veggie Stir Fry",
    "ingredients": [ 1, 2, 3 ],
    "diet": "vegetarian",
    "prepTime": 15,
    "instructions": "Stir-fry vegetables in sesame oil and add soy sauce to taste."
  },
  {
    "id": 4,
    "title": "Overnight Oats",
    "ingredients": [ 10, 11, 12 ],
    "diet": "vegetarian",
    "prepTime": 5,
    "instructions": "Combine oats, milk, and fruit. Refrigerate overnight."
  }
]
```

The query parameter `diet=vegetarian` filters the results to show only recipes with the `vegetarian` property. The `prepTime=15` parameter further narrows the results to recipes that have a preparation time of 15 minutes or less.

## Other Tutorials

* [Find a Specific Meal Plan](tut-get-plan-diet-duration.md)
* [Find Ingredients with Specific Attributes](tut-get-ingredients-vegan-protein.md)
* [Paginate Results](tut-get-ingredients-limit-offset.md)

## Other Links

[Home](../index.md) | [Setup](../mmprefland.md) | [Tutorials](../mmtutorial.md) | [Reference](../mmref.md)

