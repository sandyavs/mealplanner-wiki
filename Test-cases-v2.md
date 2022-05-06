## Test case No: MP-Login-001
## Test case description: 
Login with meal designer credentials
## Steps to follow:
1. Login url 
2. Enter username
3. Enter password

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


## Test case No: MP-SelectMeal-002

## Test case description:
Select meal based on  the search criteria.
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

## Test case description: 
Add meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Select the meal from the selected meal catalog
3. Drag and drop it in the specific category of meal plan
4. Check weather the meal is added to the specific category of meal plan for a particular day. Eg: In Lunch section for Monday, the selected meal should have been added.

## Expected Behaviour:
Should be able to select the meal from the selected meal catalog and add it to the specific category of meal plan


## Test case No: MP-DeleteMeal-004

## Test case description: 
Delete meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Verify when mouse hover the meal item in a specific category of meal plan is highlighted with green color and showing delete icon or not
3. check that the user is able to click on the delete icon/button
4. Check that when the user clicks on the delete icon/button then the meal in the specific category of meal plan for a particular day gets deleted. Eg: In Lunch section for Monday, the selected meal should have been deleted

## Expected Behaviour:
Should be to able delete the meal in the specific category of meal plan when clicked on the delete icon

## Test case No: MP-AddTag-005

## Test case description:
Add tags to the meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Click on the input textbox to enter the required text
3. Check whether it takes only alpha characters(A-Z).
4. Check whether it takes Numeric characters (numbers 0-9)
4. Make sure that after entering characters and when you click enter, a tag is added to the meal plan with the text that has been input in step 2

Expected Behaviour:
It should allow only Alphabets and Should be able to add tags to the meal plan.

## Test case No: MP-SelectUser-006

## Test case description: 
Select User
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. check that the Dropdown is Clickable or Not.
3. check that by clicking on the dropdown whether list of users are displayed.
4. check that the dropdown displays all users or few as the user clicks on the dropdown.
5. check that when user selects "admin" in dropdown, make sure admin is able to view the meal planner page.
6. check scroll down functionality working in the dropdown list or not.
7. check that the drop-down list is scrolled down by pressing the Arrow-down key on the keyboard.
8. check that the dropdown is not editable.
9. check that the dropdown values are accessible and user be able to select by clicking on specific value in the dropdown by mouse pointer.

Expected Behaviour:
When user selects "admin" from list of users dropdown, admin should be able to view the meal planner page. 


## Test case No: MP-AddDescription-007

## Test case description: 
Description of the meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check the description input box is clickable or not.
3. Check that whether the description input box accepts alphabets A-Z.
4. Check whether the description input box accepts both upper and lower case alphabets.
5. Check the maximum and minimum character length of description box.
6. Check whether the description box accepts numeric, special characters and symbols.

Excepted Behaviour:
User should be able to click on Description input box and be able to enter both Alphanumeric characters
