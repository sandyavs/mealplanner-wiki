# Test case Portfolio v 1.0

| S.No | Test case ID   | Test case name                                         |
|:-----|:---------------|--------------------------------------------------------|
| 1 | [MP-Login-001](#001) | Login with meal designer credentials       |
| 2 | [MP-MealCalendar-002](#002)|  View a specific Meal Plan in Desktop view |
| 3 | MP-SelectMeal-003 | Select meal based on the search criteria. |
| 4 | MP-AddMeal-004 | Add meal in the specific category of meal plan |
| 5 | MP-DeleteMeal-005 | Delete meals in the specific category of meal plan |
| 6 | MP-EditMealPlanName-006 | Select User |
| 7 | MP-SelectUser-007 | Select User |
| 8 | MP-AddTag-008 | Add tags to the meal plan |
| 9 | MP-AddDescription-009 | Description of the meal plan |
| 10 | MP-Logout-010 | Check whether the user can logout successfully |
| 11 | MP-Menu bar-011 | Check the menu is displayed properly on the top of the web page |

# Test case Portfolio v 2.0

| S.No | Test case ID   | Test case name                                         |
|:-----|:---------------|--------------------------------------------------------|
| 1 | [MP-Login-001](#001) | Login with meal designer credentials       |
| 2 | [MP-MPCalendar-002](#002)|  View a specific Meal Plan in Desktop view |
| 3 | MP-SelectMeal-003 | Select meal based on the search criteria. |
| 4 | MP-AddMeal-004 | Add meal in the specific category of meal plan |
| 5 | MP-DeleteMeal-005 | Delete meals in the specific category of meal plan |
| 6 | MP-EditMealPlanName-006 | Select User |
| 7 | MP-SelectUser-007 | Select User |
| 8 | MP-AddTag-008 | Add tags to the meal plan |
| 9 | MP-AddDescription-009 | Description of the meal plan |
| 10 | MP-Logout-010 | Check whether the user can logout successfully |
| 11 | MP-Menu bar-011 | Check the menu is displayed properly on the top of the web page |
| 12| [MP-MPCalendar-012](#012) | User should show 'No user assigned' |



## <a id="001">Test case ID: MP-Login-001</a> 
## Test case name: 
Login with meal designer credentials
## Steps to follow:
1. Check that the login page contains input boxes for Username and Password, and with Sign-in button
2. Check that cursor is in the “Username” text box by default on the page load (login page)
3. Check that tab functionality is working by pressing the tab button on keyboard to move to Password field from Username.
4. Check that when user clicks on show password icon, user should be able to view the password
5. Check that when user clicks on hide password, user shouldn't be able to view the password
6. Check that whether the User is able to Login with an invalid Username and invalid Password
7. Check that whether the User is able to Login with a Valid Username and invalid Password
8. Check that whether the User is able to log in with an invalid Username and Valid Password
9. Check that whether the User is able to log in with a blank Username or Password
10. Check that whether the User is able to Login with inactive credentials
11. Check that whether the User is able to Login when valid username and password are entered

## Expected result: 
User should be able to login successfully when the valid username and password are entered and view the home page by clicking on sign-in button and display an error that username/password is wrong when invalid parameters are passed in username or password fields.

## <a id="002">Test case ID: MP-MPCalendar-002</a>

## Test case name: 
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



## Test case ID: MP-SelectMeal-003

## Test case name:
Select meal based on the search criteria.
## Steps to follow:

Pre-requisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Click the search box to input text
3. Check when user start typing word in the search box, it should suggest words that matches typed keywords
4. Choose and select from the list of suggested meal catalog options
5. Ensure that meal is selected from the suggested meal catalog
6. Check whether there is option to cancel(X mark) the selected meal
7. Click on Cancel button
8. Ensure that the meal option is not selected now.

## Expected Behaviour:
Meals should be selected from the suggested meal catalog

## Test case ID: MP-AddMeal-004

## Test case name: 
Add meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Select the meal from the selected meal catalog
3. Drag and drop it in the specific category of meal plan
4. Check weather the meal is added to the specific category of meal plan for a particular day. Eg: In Lunch section for Monday, the selected meal should have been added.
5. Check weather the meal added is also added in the database.

## Expected Behaviour:
Should be able to select the meal from the selected meal catalog and add it to the specific category of meal plan


## Test case ID: MP-DeleteMeal-005

## Test case name: 
Delete meal in the specific category of meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Verify when mouse hover the meal item in a specific category of meal plan is highlighted with green color and showing delete icon or not
3. check that the user is able to click on the delete icon/button
4. Check that when the user clicks on the delete icon/button then the meal in the specific category of meal plan for a particular day gets deleted. Eg: In Lunch section for Monday, the selected meal should have been deleted
5. Check the meal is also deleted from the database.

## Expected Behaviour:
Should be to able delete the meal in the specific category of meal plan when clicked on the delete icon


## Test case ID: MP-EditMealPlanName-006

## Test case name: 
Select User
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check in the header section, when user clicks on the mealplan name make sure the previous mealplan name is highlighted.
3. Check to make sure it is editable such as "Vegetarian Meal Plan".
4. Check to make sure that it is automatically saved in the database.
5. Check that whether the mealplan name input box accepts alphabets A-Z.
6. Check whether the mealplan name input box accepts both upper and lower case alphabets.
7. Check whether the mealplan name input box accepts numeric, special characters and symbols.

Expected Behaviour:
User should be able to edit the mealplan name.


## Test case ID: MP-SelectUser-007

## Test case name: 
Select User
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. On the header section when Signed in check that whether the name of the user such as "Admin" is displayed
3. Check that the Dropdown present in the header section and whether it is Clickable.
4. Check that by clicking on the dropdown whether a list of users are displayed.
5. Check whether the dropdown is displaying all the users or only a few as the user clicks on the dropdown.
6. Check that the user should be able to select different users such as "meal designer" in the dropdown.
7. Check to make sure that the selected user name is automatically saved in the database.
8. Check and make sure to scroll down functionality working in the dropdown list and view other user options.
9. check that the drop-down list is scrolled down by pressing the Arrow-down key on the keyboard.
10. check that the dropdown is not editable.
11. check that the dropdown values are accessible and the user is able to select by clicking on specific values in the dropdown by mouse pointer.

Expected Behaviour:
Should be able to select the user such as "meal designer" from the dropdown.

## Test case ID: MP-AddTag-008

## Test case name:
Add tags to the meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Check and make sure that on the header section there is an arrow key pointing downwards by default.
3. Click on the arrow key pointing downwards to expand the view to display description and add tags details.
4. When the view is in expanded form as that of an arrow turning upwards check the add tag input box is displayed and if it's clickable.
5. Click on the input textbox to enter the required text
6. Check whether it takes only alpha characters(A-Z).
7. Check whether it takes Numeric characters (numbers 0-9)
8. Make sure that after entering characters and when you click enter, a tag is added to the meal plan with the text that has been input in step 6
9. Check to make sure that it is automatically saved in the database.
10. Check whether there is an option to delete(X mark) the selected tag.
11. Click on the delete button to delete the tag.
12. Check to make sure that the tag is also deleted from the database.
13. Check and make sure the arrow now pointing upwards and when clicking on it should collapse the view and hide description and tags


## Expected Behaviour:
It should allow only Alphabets and Should be able to add tags to the meal plan and when clicked delete, the selected tag should be deleted.


## Test case ID: MP-AddDescription-009

## Test case name: 
Description of the meal plan
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check and make sure that on the header section there is an arrow key pointing downwards by default.
3. Click on the arrow key pointing downwards to expand the view to display description and add tag details.
4. When the view is in expanded form as that of an arrow turning upwards check the description input box is displayed and if it's clickable.
5. Check whether the description input box accepts alphabets A-Z.
6. Check whether the description input box accepts both upper and lower case alphabets.
7. Check the maximum and minimum character length of the description box.
8. Check whether the description box accepts numeric, special characters and symbols.
9. Check to make sure that it is automatically saved in the database.
10. Check whether the user is able to view the description, after the user gets logged out and sign-in again.
11. Check and make sure the arrow now pointing upwards and when clicking on it should collapse the view and hide description and tags


Expected Behaviour:
User should be able to click on Description input box and be able to enter both Alphanumeric characters and user should be able view the saved description after the user logins again


## Test case ID: MP-Logout-010

## Test case name: 
Check whether the user can logout successfully
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check after successful login such as "Admin", the logout button is visible on the top right corner of the webpage.
3. Check whether the logout button is clickable or not.
4. Check whether the user is able to logout successfully by clicking on the logout button.
5. After successful logout users should be able to view the sign-in page of the meal planner website.
6. After logout check whether the user is able to login again by clicking on the back button on the sign-in page of the meal planner website.
7. Check by logging into more than one browser and logout from any of them and check whether other accounts are properly working or all get logged out.
8. Check the logout option should not be visible till the user is logged in.
9. After logging in with correct user credentials, close the browser by clicking on (X) and again reopen the browser and check whether the user is logged in or auto logout from the meal planner website.

## Expected Behaviour:
User should be able to logout successfully by clicking on the logout button.

## Test case ID: MP-Menu bar-011

## Test case name: 
Check the menu is displayed properly on the top of the web page
## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check the menus are displaying properly without any congestion and properly displayed.
3. Check the menu is adjusting automatically or not based on the number of menus.
4. Check whether the menu item is clickable.
5. When user clicks on the menu item such as "Plans", user should view "Plans" web page.
6. Check "Good Meal Plan" logo is properly visible on the menu bar of the web page.

## Expected Behaviour:
When user clicks on the menu item such as "Plans", user should be able to view "Plans" web page.

## <a id="012">Test case ID: MP-MPCalendar-012</a>

## Test case name: 
User not assigned should be shown as text in meal calendar 

## Related Bug ID: #456

## Steps to follow:
Pre-requisite: MP-Login-001
1. Go to '/mealplans'
2. Click on 'Create Meal Plan'
3. Enter the meal plan name 'Veg' and do not assign a user
4. Click on the created meal plan
5. In the mealplan calendar view, notice there is no user field next to the meal plan name.

