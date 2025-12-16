# Practice 3: Recipe Page (Hard)

## Objective

Create a comprehensive recipe page with multiple sections, nested lists, images, and proper HTML structure. This exercise will test your understanding of HTML organization and various elements.

## Requirements

Create a file named `recipe.html` that includes:

1. Proper HTML5 document structure
2. A page title: "Recipe: [Your Chosen Recipe]"
3. A main heading (`<h1>`) with the recipe name
4. A recipe image with proper alt text
5. A brief description paragraph about the dish
6. A "Recipe Info" section with:
   - An `<h2>` heading
   - Prep time, cook time, and servings (use paragraph or div elements)
   - Use `<strong>` to label each piece of information
7. An "Ingredients" section with:
   - An `<h2>` heading
   - An unordered list of all ingredients
   - At least one nested list for sub-ingredients (e.g., "For the sauce:")
8. An "Instructions" section with:
   - An `<h2>` heading
   - An ordered list of step-by-step instructions
   - At least 5 steps
9. A "Tips" section with:
   - An `<h2>` heading
   - An unordered list of cooking tips
10. A "Nutrition Facts" section (optional)
11. Navigation links at the bottom to:
    - "Back to Top" (links to top of page using `#`)
    - "More Recipes" (external link)

## Example Structure

```
Chocolate Chip Cookies
[Image of cookies]

Delicious homemade chocolate chip cookies...

Recipe Info
-----------
Prep Time: 15 minutes
Cook Time: 12 minutes
Servings: 24 cookies

Ingredients
-----------
• 2 cups flour
• 1 cup butter
• For the chocolate mixture:
  • 2 cups chocolate chips
  • 1 tsp vanilla

Instructions
------------
1. Preheat oven to 350°F
2. Mix dry ingredients...
...
```

## Tips

- Use nested lists by placing a `<ul>` or `<ol>` inside a `<li>` element
- Use `<a href="#top">` to create a link to the top of the page (add `id="top"` to an element)
- Keep your code well-organized and properly indented
- Test your page in a browser to ensure everything displays correctly

## Bonus Challenges

- Add a table for nutrition facts
- Include multiple images showing different steps
- Add a "Related Recipes" section with links
- Use `<abbr>` for abbreviations like "tsp" (teaspoon)

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recipe: Chocolate Chip Cookies</title>
</head>
<body id="top">
    <h1>Classic Chocolate Chip Cookies</h1>
    
    <img src="https://via.placeholder.com/600x400" alt="Freshly baked chocolate chip cookies on a cooling rack">
    
    <p>These <strong>classic chocolate chip cookies</strong> are crispy on the outside, chewy on the inside, and packed with chocolate chips. Perfect for any occasion and loved by everyone!</p>
    
    <hr>
    
    <h2>Recipe Info</h2>
    <p><strong>Prep Time:</strong> 15 minutes</p>
    <p><strong>Cook Time:</strong> 12 minutes</p>
    <p><strong>Total Time:</strong> 27 minutes</p>
    <p><strong>Servings:</strong> 24 cookies</p>
    
    <hr>
    
    <h2>Ingredients</h2>
    <ul>
        <li>2 1/4 cups all-purpose flour</li>
        <li>1 tsp baking soda</li>
        <li>1 tsp salt</li>
        <li>1 cup (2 sticks) butter, softened</li>
        <li>3/4 cup granulated sugar</li>
        <li>3/4 cup packed brown sugar</li>
        <li>2 large eggs</li>
        <li>2 tsp vanilla extract</li>
        <li>2 cups chocolate chips</li>
        <li>Optional additions:
            <ul>
                <li>1 cup chopped nuts</li>
                <li>1/2 cup toffee bits</li>
            </ul>
        </li>
    </ul>
    
    <hr>
    
    <h2>Instructions</h2>
    <ol>
        <li>Preheat your oven to 375°F (190°C).</li>
        <li>In a small bowl, combine flour, baking soda, and salt. Set aside.</li>
        <li>In a large mixing bowl, beat the softened butter, granulated sugar, and brown sugar until creamy.</li>
        <li>Add eggs and vanilla extract to the butter mixture. Beat until well combined.</li>
        <li>Gradually stir in the flour mixture until just combined.</li>
        <li>Fold in the chocolate chips (and optional nuts or toffee bits).</li>
        <li>Drop rounded tablespoons of dough onto ungreased cookie sheets, spacing them about 2 inches apart.</li>
        <li>Bake for 9-12 minutes or until golden brown around the edges.</li>
        <li>Let cookies cool on the baking sheet for 2 minutes before transferring to a wire rack.</li>
        <li>Enjoy warm or store in an airtight container!</li>
    </ol>
    
    <hr>
    
    <h2>Tips</h2>
    <ul>
        <li>For chewier cookies, slightly underbake them and let them cool on the pan.</li>
        <li>Room temperature butter mixes better with the sugars.</li>
        <li>Don't overmix the dough after adding flour to keep cookies tender.</li>
        <li>Chill the dough for 30 minutes before baking for thicker cookies.</li>
        <li>Use a cookie scoop for uniform-sized cookies that bake evenly.</li>
    </ul>
    
    <hr>
    
    <h2>Nutrition Facts (Per Cookie)</h2>
    <p><strong>Calories:</strong> 180 | <strong>Fat:</strong> 9g | <strong>Carbs:</strong> 24g | <strong>Protein:</strong> 2g</p>
    
    <hr>
    
    <p>
        <a href="#top">Back to Top</a> | 
        <a href="https://www.example.com/recipes" target="_blank">More Recipes</a>
    </p>
    
    <p><em>Happy Baking!</em></p>
</body>
</html>
```

</details>
