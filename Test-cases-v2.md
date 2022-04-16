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


## Test case No: MP-MealCatalog-001

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