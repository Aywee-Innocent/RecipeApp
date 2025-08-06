# RecipeApp
One notes the ingredients they have then it creates a recipes for the ingredients noted 
# Ingredient Recipe Generator

A simple and user-friendly web app that allows users to enter ingredients and get recipe suggestions from **TheMealDB** API. The app fetches recipes containing *all* the input ingredients and displays detailed information including instructions and images.

---

## Features

- Input ingredients as a comma-separated list (e.g. `chicken, tomato, garlic`)
- Fetches recipes that include *all* the specified ingredients using TheMealDB’s free public API
- Displays recipe name, list of ingredients (with measures), cooking instructions, and an image
- Graceful handling of no matches or invalid input
- Clean, responsive, and visually simple interface built with only HTML, CSS, and JavaScript
- No backend needed — runs fully client-side in any modern browser

---

## Demo

Try entering ingredients like:

- `chicken, garlic`  
- `tomato, onion`  
- `beef, rice`  

and see matching recipes appear instantly!

---

## Setup and Usage

1. **Download or copy the `index.html` file** from the repository.

2. **Open `index.html`** in any modern web browser (Chrome, Firefox, Edge, Safari, etc.).

3. **Enter one or more ingredients** separated by commas in the text input field.

4. Click on the **Generate Recipes** button.

5. The app will fetch matching recipes from TheMealDB API and display the details below the button.

---

## How It Works

1. The user inputs a list of ingredients separated by commas.

2. For each ingredient, the app queries TheMealDB API endpoint to fetch recipes containing that ingredient:
https://www.themealdb.com/api/json/v1/1/filter.php?i={ingredient}


3. The app takes the intersection of recipes returned for all input ingredients, thus filtering for only recipes containing *all* specified ingredients.

4. It then fetches full details for each recipe (ingredients, measures, instructions, and image) from:

https://www.themealdb.com/api/json/v1/1/lookup.php?i={mealID}


5. The results are displayed nicely with recipe name, list of ingredients, instructions, and meal image.

---

## Technologies Used

- **HTML5** - Basic page layout and user input.
- **CSS3** - Styling and responsive design.
- **JavaScript (ES6+)** - Fetch API calls, data processing, DOM manipulation.
- **TheMealDB API** - Free public API for recipe data.

---

## API References

- TheMealDB API Documentation:  
https://www.themealdb.com/api.php

---

## Limitations

- TheMealDB API only supports searching by single ingredients; to find recipes with multiple ingredients, the app performs multiple API calls and looks for common recipes.
- Results are limited to the recipes available in TheMealDB’s database.
- No offline support or caching implemented.
- Does not currently support partial ingredient matches or fuzzy search (requires exact matches in database).

---

## Possible Improvements

- Add partial matching or fuzzy ingredient matching for more flexible search.
- Add autocomplete or suggestions for ingredient names.
- Support filtering by diet types, meal categories, or cuisine.
- Add pagination for large result sets.
- Improve UI/UX with better design and responsive elements.
- Integrate additional recipe APIs for more recipe options.
- Implement local caching to reduce API calls.
- Add user accounts to save favorite recipes (would require backend).

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Author

Created by [Your Name] (replace with your name or GitHub handle).

---

Feel free to reach out with suggestions or issues!

---

