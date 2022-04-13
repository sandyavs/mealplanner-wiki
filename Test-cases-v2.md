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