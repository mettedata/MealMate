# Quick Start Guide

Follow these steps to clone the MealMate API repository and start the service before you make your first call to the MealMate service.

These steps should take less than 5 minutes.

## Prerequisites

See [Before Your Start](mmbefore-you-start.md) to ensure that you have your development environment set up and configured correctly.

## Copy the Repository

1. On GitHub, open the [MealMate API repository](index.md).
2. [Fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#forking-a-repository) the MealMate API service for your own use.
3. [Clone your fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#cloning-your-forked-repository) of the MealMate API repository to copy the service's files to your local repository.

You can now test the JSON server.

## Test the JSON Server

Follow these steps to ensure that the server works locally.

1. In GitHub Desktop, access the main branch of the MealMate repository.
2. Open a terminal to access your fork from a command line.
3. Enter the following command to navigate to the .json file:

    ```cd api```
4. From the `/api` directory, enter the following command to start the JSON server:

    ```json-server -w mealmate-db.json```

5. Verify that the service starts:

```json

   \{^_^}/ hi!
    Loading mealmate-db.json
    Done

     Resources
     http://localhost:3000/recipes
     http://localhost:3000/ingredients
     http://localhost:3000/plans

     Home
     http://localhost:3000
```

## Next Steps

Now that you've verified that the MealMate service is started, keep the terminal open and use the [Get Started](mmget-started.md) guide to make your first call to the MealMate API.

## Other Links

[Home](../index.md) | [Setup](../mmprefland.md) | [Tutorials](../mmtutorial.md) | [Reference](../mmref.md)
