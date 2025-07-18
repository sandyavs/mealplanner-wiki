# Minutes of Meeting 6-Jun-2023
1. Data entry to be done in local server. Practice well and ask doubts within peers. If unable to solve please ask me
2. Then data entry on the develop server. 1 recipe only entered by one person so that there are no duplicates
3. For that following needs to be done
4. we need to list all the recipes from Greener village along with their ingredients in google sheet. Sort the ingredients and then filter.
5. Create a list of products from the unique list of ingredients.
6. Then enter product code based on what is already on the database entered by seed.sql and recipes_seed.sql. create new product codes for new ingredients.
7. Please keep the same row id for the product as mentioned in the admin UI.
8. All the above is only preparation because we have existing data. Then the actual data entry is simple
9. First create a product in the Admin UI with the product code in the Google sheet in the order as per the ids. Please be careful not to create duplicates. Please note that the row id is automatically generated by the database. The Google sheet should reflect what is in the admin UI so that we have a clear picture.

Issues assigned:
1. Riya - favourites. Explained about db table, frontend UI - link to list all favourites for a user after selection.
2. I thought about the database design a little more. My original idea will be the best of having a seperate favourites table and having user_id and meal_id. The reason is that if we have arrays then GraphQL fetch will become difficult as it can't use referential integrity. Also you can't handle cascade delete when a meal is deleted as it will sit as an array element inside a field in user table.
3. Pujitha, Bo, Mayomi, Tulio
Each of you can pair with Riya to do the favourites feature.
I would like you to figure out how to write SQL to create a table,
create the GraphQL query,
how to call the GraphQL query inside the react component
and then how to create the frontend show a link and show favourites page.
One of you create the following bug
Bug:
If you create a meal without user assigned, in the meal calendar view there is no way we can edit a user. So the user field in the meal calendar view should show No assigned user as an option in the drop down and should be the value shown when there is no user assigned.

Pavithra: working on shopping list calculating correct cost based on ingredients measure vs the product price.

Dev process:
You will work on your ticket branch
After completion create merge request to v2.
Upon reviewing and testing will be merged to develop

# Minutes of Meeting 13-Jun-2023
1. Riya favourites feature (issue #455): Code review finished, must create graphQL query, and make a PR
2. Mayomi's bug (issue #355) where empty meals are being created: initial solution involves making every field as required so that empty meals cannot be created, but code and name_en is mandatory, the rest of the fields are not mandatory. Must fix this in the solution.
3. Getting familiarized with reactJS
    - Mayomi, Bo, Pujitha, Tulio must do a sample project (different project for each members) in react. Push code to github.
    - To be complete by Friday/Saturday
    - can use material UI (MUI) instead of css, bootstrap 
    - https://mui.com/
4. Sebastian is awaiting code review for his issue
5. Bo is to create a PR for bug where username is not showing up when meal is not assigned to a user (issue #456)
6. Duplicate meal plan feature (issue #377) assigned to Pujitha
7. New feature: In mealplanner AdminUI (localhost:2000), be able to search particular meals in meal table
    - assigned to Tulio
    - Tulio must create new feature issue on github
8. Print Meal plan calendar is broken when in portrait view bug (issue #345) assigned to Mayomi
9. New bug: on the meal plans page, change trash and shopping cart icon colours to green when hovering the mouse over
     - assigned to Bo
     - Bo must create new bug issue
10. New bug: on the meal plans page, on click delete, must have confirmation dialogue.
     - assigned to Bo
     - Bo must create a new bug issue

11. Steps on how to push code and create PR
     - git checkout v2
     - git pull origin v2
     - git checkout -b {issue#}-{descriptionofissue}
         - ex: git checkout -b 456-display-username
     - git add {changedfiles}
     - git commit -m "[#issuenumber] descriptionofwhatyourcodeacheives"
         - ex: git commit -m "[#456] username will be displayed as no user assigned in the mealplanner calendar"
     - git push origin {yourbranchname}
         - ex: git push origin 456-display-username
     - create PR: select V2, not develop for base
     - assign PR to Shanthi


