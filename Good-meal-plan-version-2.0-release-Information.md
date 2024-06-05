# Good Meal Plan - Version 2.0 - Release information

**Project Code:** Mealplanner

**Release:** Version 2.0

**Client:** Greener Village

**Demo Date:** 28-May-2024

**Release Date:** 5-June-2024

**Demo Video URL:** https://www.youtube.com/watch?v=PL-hsxbr7Ek

## Volunteers:
### Developers: 
_Shanthi Shanmugam, Vagmi Mudumbai, Bo Sun Kim, Priya Guntupalli, Rodrigo Castro, Pavitra Modi, Jon Dalton_
### QAs: 
_Ola Makhlouf, Ala Salehi_
### Data entry: 
_Folashade Jemilo, Rhoda Mairabo, Adeniyi Oluokun, Mohamed Alsadek Mohamed, Ola Makhlouf, Tracy Copeland, Oliver Ogbaka, Olufemi Awodola, Pavitra Modi, Bo Sun Kim, Akinwale Mayomi Aisida, Oluwatoyosi Adelekan, Ashwant Manikoth_
### Database and deployment support: 
_Rory Bray, Vagmi Mudumbai_

## Features List:
### Database level:
1. Introduced a new system of migration for the database changes 
1. Imported recipes from docx to text and text to JSON using AI and wrote scripts to update the database
1. We scraped thousands of products based on keywords related to recipe ingredients. We used a scraper API from the Walmart website. These prices and data are as of March 2024 and cannot be programmatically updated as some entries have been manually added.
1. Login secure cookie. - We set the cookie secure field to true on the production environment.

### Admin UI:
1. Meal designer has now permission to access admin UI except the `Users` section
1. Search for any word in the meal name yields accurate results in the meals section
1. Search for any word in the product name yields accurate results in the products section.
1. Every meal has a code based on the unique meals alphabetically ordered.
1. Meals have ingredients that can be individually created with quantity and unit.
1. The ingredient code should be unique for a recipe and ordered as in the recipe document.
1. In the case of multiple ingredients with the word OR in the ingredient, e.g., Raspberry or Apricot jam, I have introduced substitute ingredients and substitute reasons and assigned the first ingredient as the primary ingredient.
1. Match ingredient to products: The suggestions to what to buy for a specific ingredient of a recipe are accomplished with a match view
   1. It has a list of products shown that matches the product keyword of the ingredient.
   1. The product list has a name, quantity, unit, image and source URL shown.
   1. When selecting the products from the list, they get added to a drop-down box. It is ideal to select 3 to 5 relevant products 
   1. From this drop-down box, you can select one which is marked as the best match
1. Each ingredient of a meal and products are matched using a ‘product keyword’.
1. The tags and product keywords are one or two words specified in lowercase. But should not have special characters. Should be separated with a comma
1. The meal name appears on the `ingredients` and `match` pages, with a link to return to the previous page. 
1. Show meal page — This is an individual meal page with sections and an ingredients link. After editing the meal, it redirects to the show page of the meal.
1. The tips on the meals page are in rich text format just like the method.
1. Reset password will reset to the given password and can be set only by the admin.

### Main UI:
1. Login - The first-time login will show the terms and conditions page. Only on accepting can I login
1. Login - Meals and meal page can be accessed without login
1. Login - Display error message when invalid credentials are given
1. Mealplans - Create a mealplan has a tooltip for name and description
1. Mealplans - Create a new template for admins and meal designers
1. Mealplans — Templates can be identified with a T in a grey circle. When no user is assigned, it is a green circle with a person icon. If a user is assigned, their initials are shown.
1. Mealplans - filter by tags
1. Mealplans - Search a meal by name, template or filter by tags
1. Mealplans - Duplicate meal plan - to create multiple meal plans based on an existing one by copying it.
1. Mealplans - Trash can denotes Delete on hover turns green and asks for confirmation on delete
1. Mealplans — The Cart represents the Shopping list. It will turn green when hovered, and clicking it opens a printable page.
1. Mealplans - Shopping list 
   1. revamped to show the product suggestions for each ingredient
   1. Shows the quantity and unit for each meal
1. Mealplan has a start date, which can be set when creating or editing a meal plan.
1. Mealplan calendar - User field
   1. The user field will be shown as `No User assigned` when no users have been assigned to the meal plan.
   1. In the case of client login, this field is not visible as the user will be assigned only by admin or meal designer.
1. In case of client login, this field is not visible as user will be assigned only by admin or meal designer.
1. Print of Shopping list, meal plan calendar and meal has CivicTech Logo.
1. Meals - Search for a meal on the meals page
1. Meals — Favourite a meal—On hover, it turns red, and on click, it sets a favourite meal for the current and on another click removes the favourite.
1. Meals - Search by favourite of current user for a client or any user for admin and meal designer
1. Meals - Filter by tags
1. Meal - Shows the prep time, cook time, portions
1. Meal - Ingredients
   1. Ingredients are shown as a table grid with substitute ingredients and reasons.
   1. Substitute reason will be shown as ‘Not specified’ if no reason is specified.
1. Meal - Nutrition data is shown on the `mealplan` page
