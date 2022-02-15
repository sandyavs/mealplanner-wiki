============================================================================================
# Test Case #1: E3.01 Select one or more Meal Plans #21

### Description:
As a Client user, or acting on behalf of the client, I want to select one or more weekly meal plans so that I can organize my meals.

To manage the household, you can create multiple plans for a given week. Maximum 10.

Select plans for up to 4 future weeks. Multiple plans are assigned to upcoming weeks for a specific client.
(A week should start on a Monday) (The earliest week you can assign a meal plan to is the upcoming week)

Each meal plan needs to have portion selection. Granularity is half portions. Minimum is 0.5, Maximum is 10

### Assumptions:

### Acceptance Criteria:
User is able to select/assign at least one weekly meal plan, up to 10 meals plans for one week.
User can scale the plan size by "half portions" per plan.
Meal Plan selections are assigned to the client, for future re-use.
Meal Plans cannot be assigned to the current week or to past weeks
Meal Plans can be duplicated from previous weeks into future weeks
Meal Plans can be created from scratch
Meal Plans are editable until they are no longer in the future

### Expectations: 
I can log in, select a Client, and navigate to the Weekly Meal Plan page for the Client. From there, I can copy an existing  Meal Plan, copy a template Meal Plan, or create a new Meal Plan. After designing a Meal Plan, I can assign a week to it. After assigning a week I can save it, and visit it later.


### Results: 
Logging in as Meal Designer, I added a new Meal Plan. The Name field is required, and validated correctly. Creating a new Meal automatically redirected me to the Weekly Meal Plan page. The Meal Periods highlighted when I hovered a drag-and-drop Meal over it. Letting go of the mouse correctly inserted the Meal into the Meal Period. I was able to add Meals from any Meal Period on a given day of the week. I was able to add multiple Meals to any Meal Period on a given day of the week. Meals can be duplicated in any Meal Period, and exist multiple times in a Weekly Meal Plan. Removing a Meal from a Meal Period correctly removes only that Meal. Adding a Meal multiple times to a Meal Period, then deleting one Meal results in all of that Meal being deleted in the Meal Period. Selecting a different Meal Plan from the Meal Plan DropDownList correctly resets the page for that Meal Plan. The Save button did not save the Meal Plan.

### Issues: 
1. The meals on the left did not highlight to notify me they are draggable objects.
2. The Meal Owner (Client) allows for typing in, but does not state it is for searching only
3. The page has a vertical scrollbar, but also has another vertical scrollbar for just the Meals. The page scrollbar could be removed.
4. There was no option to assign a week to a Meal Plan. Perhaps this is done on another page?
5. The Save button did not save the Meal Plan.
6. Adding a Meal multiple times to a Meal Period, then deleting one Meal results in all of that Meal being deleted in the Meal Period. This issue is referenced in the "Delete Item from Meal Plan#224" item on the Board.

### Notes:
1. This Test Case should be broken up into smaller sub sections. IE: Creating a new Meal Plan for a Client. Creating a second new Meal Plan for a Client. Editing an existing Meal Plan.
2. The Meal Owner (Client) DropDownList does not have a name or label.
3. If the Meal Owner (Client) DropDownList were to grow, the list might become unweildy, forcing the User to constantly type in names or manually search a long list.
4. The Weekly Meal Plan page is missing a header or title or tab name to signify it's intent.
============================================================================================





============================================================================================
# Test Case #2: Delete Recipe#183

### Description:
As an Admin User, I want to delete existing recipes, so that the recipe list could be properly maintained or managed.

### Assumptions:
Only admin user has access to the Delete Recipe Screen.
Meal Designer is an Admin user.

### Acceptance Criteria:
The Delete Recipe screen should be accessible from the Main page or Admin landing page.
The recipe/s should be searchable, so that they could be displayed to the user.
The Delete screen should display the following fields/sections as read-only:
Recipe Name
Recipe Photo
Recipe Video
General Description/Tips
Serving Size
Preparation Time
Ingredients
Cooking/Preparation Directions
The user should be able to delete the recipe.
There should be a message prompt to confirm if the user wants to delete the recipe prior to proceeding with the deletion.


### Expectations: 


### Results: 
Logging in as Meal Designer, I navigated to the Catalogue of Meals page. From there I could not search for Meals. I was confused as to whether more Meals existed than what was displayed. Clicking on the Meal picture did not navigate to the Meal. Hovering over the "i" icon did not produce a tooltip as I expected. Only clicking on the "i" icon navigated to the Meal. 

When navigating to a Meal, the entire screen is filled with a large picture of the Meal. Scrolling down bring the Meal info into view.

## Issues: 


### Notes:
1. The Recipe is referring to the Meal Catalog? Are these "Recipes" or "Meals"?