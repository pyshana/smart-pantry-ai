<!-- This is the markdown template for the final project of the Building AI course, created by Reaktor Innovations and University of Helsinki. Copy the template, paste it to your GitHub README and edit! -->

# Smart Pantry & Nutrition Companion
Final project for the Building AI course

## Summary
Smart Pantry is an AI-driven tool designed to reduce domestic food waste and recommend personalized meals based on available ingredients and user preferences. Building AI course project.

## Background
Food waste is a major global issue; households throw away tons of edible food every year simply due to forgotten expiration dates or lack of meal inspiration:
* Inefficient grocery utilization leads to unnecessary financial costs for households.
* Food decomposition in landfills significantly contributes to greenhouse gas emissions.
* Daily meal planning is time-consuming for busy individuals and students.

My motivation is to combine computer vision and natural language processing to help ordinary households optimize their kitchens sustainably.

## How is it used?
The user snaps a picture of their refrigerator shelves or grocery receipts using a smartphone. The system identifies items, tracks their freshness, and automatically suggests easy recipes before ingredients spoil.
* Environment: Mobile application used in homes and student kitchens.
* Users: Busy professionals, students, and home cooks seeking easy meal plans.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Good_Food_Display_-_NCI_Visuals_Online.jpg/640px-Good_Food_Display_-_NCI_Visuals_Online.jpg" width="450">

```python
def suggest_recipes(available_ingredients, recipe_database):
    # Match available ingredients with recipe requirements
    matches = []
    for recipe, ingredients in recipe_database.items():
        overlap = set(available_ingredients).intersection(set(ingredients))
        if len(overlap) >= 2:
            matches.append(recipe)
    return matches
