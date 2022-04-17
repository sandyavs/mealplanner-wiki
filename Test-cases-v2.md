## Test case No: MP-Login-001
## Test case description: 
Login with meal designer credentials
## Steps to follow:
1. Login <url> 
2. Enter <username>
3. Enter <password>

Expected result: Should successfully login and enter the home page

## Test case No: MP-Plans-001

## Test case description: 
View a specific Meal Plan in Desktop view
## Steps to follow:
Pre-requisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check the meal plan name is displayed in tabular form
3. Check whether the 7 days (Sunday, Monday, Tuesday, Wednesday, Thursday, Friday) are listed
4. Check the categories Breakfast, Lunch, Dinner, Snack are displayed
5. Check the meals are displayed in a specific category for a particular day. Eg: In Breakfast of Monday, the added meal should be listed.

## Expected Behaviour:
Meals should be displayed correctly as per the meal plan


## Test case No: MP-MealCatalog-002

## Test case description: View meal catalog based on search criteria.
## Steps to follow:

Pre-requisite: MP-Login-001
1. Go to url/mealplan/:id 
2. click the search box to input text
3. check when user start typing word in the search box, it should suggest words that matches typed keywords
4. Choose and select from the list of suggested meal catalog options
5. Ensure that meal is selected from the suggested meal catalog
6. check whether there is option to cancel(X mark) the selected meal
7. click on Cancel button
8. ensure that the meal option is not selected now.

## Expected Behaviour:
Meals should be selected from the suggested meal catalog

## Test case No: MP-AddMeal-003

## Test case description: Add meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Select the meal from the selected meal catalog
3. Drag and drop it in the specific category of meal plan
4. Meal should be added to the specific category of meal plan

## Expected Behaviour:
Should be able select the meal from the selected meal catalog and add it to the specific category of meal plan


## Test case No: MP-DeleteMeal-004

## Test case description: Delete meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Verify when mouse hover the meal item in a specific category of meal plan is highlighted with green color and showing delete icon or not
3. check that the user is able to click on the delete icon/button
4. check that when the user clicks on the delete icon/button then the meal in the specific category of meal plan gets deleted.

## Expected Behaviour:
Should be able delete the meal in the specific category of meal plan when clicked on the delete icon
