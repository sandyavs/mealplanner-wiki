# Test case Portfolio v 1.0

| S.No | Test case ID   | Test case name                                         |
|:-----|:---------------|--------------------------------------------------------|
| 1 | [MP-Login-001](#001) | Login with meal designer credentials       |
| 2 | [MP-MPCalendar-002](#002)|  View a specific Meal Plan in Desktop view |
| 3 | [MP-SelectMeal-003](#003) | Select a meal based on the search criteria. |
| 4 | [MP-AddMeal-004](#004) | Add meals in the specific category of meal plan |
| 5 | [MP-DeleteMeal-005](#005) | Delete meals in the specific category of meal plan |
| 6 | [MP-EditMealPlanName-006](#006) | Select User |
| 7 | [MP-SelectUser-007](#007) | Select User |
| 8 | [MP-AddTag-008](#008) | Add tags to the meal plan |
| 9 | [MP-AddDescription-009](#009) | Description of the meal plan |
| 10 | [MP-Logout-010](#010) | Check whether the user can log out successfully |
| 11 | [MP-Menu bar-011](#011) | Check the menu is displayed properly on the top of the web page |

# Test case Portfolio v 2.0

| S.No | Test case ID   | Test case name                                         |
|:-----|:---------------|--------------------------------------------------------|
| 1 | [MP-Login-001](#001) | Login with meal designer credentials       |
| 2 | [MP-MPCalendar-002](#002)|  View a specific Meal Plan in Desktop view |
| 3 | [MP-SelectMeal-003](#003) | Select a meal based on the search criteria. |
| 4 | [MP-AddMeal-004](#004) | Add meals in the specific category of meal plan |
| 5 | [MP-DeleteMeal-005](#005) | Delete meals in the specific category of meal plan |
| 6 | [MP-EditMealPlanName-006](#006) | Select User |
| 7 | [MP-SelectUser-007](#007) | Select User |
| 8 | [MP-AddTag-008](#008) | Add tags to the meal plan |
| 9 | [MP-AddDescription-009](#009) | Description of the meal plan |
| 10 | [MP-Logout-010](#010) | Check whether the user can log out successfully |
| 11 | [MP-Menu bar-011](#011) | Check the menu is displayed properly on the top of the web page |
| 12 | [MP-MPCalendar-012](#012) | User should show 'No user assigned'|
| 13 | [MP-MPSearch-013](#013) | Search for a meal plan based on any word of the name |
| 14 | [AA-Autocomplete-014](#014) | Enable autocomplete feature for Products and Meals fields in admin app measure form |
| 15 | [MP-FilterByTags-015](#015) | Filter meal plans by tags                                                |
| 16 | [AA-MultipleTags-016](#016) | Verify creation of multiple tags for a product in Admin app product page   |
| 17 | [MP-CalenderUsername-017](#017) | Verify display of "no user assigned" on meal plan calendar when no user is assigned |
| 18 | [AA-DeleteMeal-018](#018) | Verify deletion of a meal from the meals table without foreign key constraint error |
| 19 | [MP-LoginErrorDisplay-019](#019) | Verify display of error message when hitting enter with invalid credentials in the login page |
| 20 | [MP-DuplicateMealPlan-020](#020) | Create a duplicate meal plan from an existing meal plan |



## <a id="001">Test case ID: MP-Login-001</a> 

## Test case name: 
Login with meal designer credentials

## Steps to follow:
1. Check that the login page contains input boxes for Username and Password and with Sign-in button
2. Check that the cursor is in the “Username” text box by default on the page load (login page)
3. Check that the tab functionality is working by pressing the tab button on the keyboard to move to the Password field from the Username.
4. Check that when the user clicks on the show password icon, the user should be able to view the password
5. Check that when the user clicks on hide password, the user shouldn't be able to view the password
6. Check whether the User is able to log in with an invalid Username and invalid Password
7. Check whether the User is able to log in with a Valid Username and an invalid Password
8. Check whether the User is able to log in with an invalid Username and Valid Password
9. Check whether the User is able to log in with a blank Username or Password
10. Check whether the User is able to log in with inactive credentials
11. Check whether the User is able to log in when a valid username and password are entered

## Expected result: 
Users should be able to log in successfully when the valid username and password are entered and view the home page by clicking on the sign-in button and display an error that username/password is wrong when invalid parameters are passed in username or password fields.

## <a id="002">Test case ID: MP-MPCalendar-002</a>

## Test case name: 
View a specific Meal Plan in the Desktop view

## Steps to follow:
Pre-requisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check the meal plan name is displayed in tabular form
3. Check whether the 7 days (Sunday, Monday, Tuesday, Wednesday, Thursday, Friday) are listed
4. Check the categories Breakfast, Lunch, Dinner, and Snack are displayed
5. Check the meals are displayed in a specific category for a particular day. Eg: In Breakfast on Monday, the added meal should be listed.

## Expected Behaviour:
Meals should be displayed correctly as per the meal plan

## <a id="003">Test case ID: MP-SelectMeal-003</a>

## Test case name:
Select a meal based on the search criteria.

## Steps to follow:

Pre-requisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Click the search box to input text
3. Check when the user starts typing words in the search box, it should suggest words that match typed keywords
4. Choose and select from the list of suggested meal catalogue options
5. Ensure that the meal is selected from the suggested meal catalogue
6. Check whether there is an option to cancel(X mark) the selected meal
7. Click on the Cancel button
8. Ensure that the meal option is not selected now.

## Expected Behaviour:
Meals should be selected from the suggested meal catalogue

## <a id="004">Test case ID: MP-AddMeal-004</a>

## Test case name: 
Add meals in the specific category of the meal plan

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Select the meal from the selected meal catalogue
3. Drag and drop it in the specific category of meal plan
4. Check whether the meal is added to the specific category of meal plan for a particular day. Eg: In the Lunch section for Monday, the selected meal should have been added.
5. Check whether the meal added is also added to the database.

## Expected Behaviour:
Should be able to select the meal from the selected meal catalog and add it to the specific category of the meal plan

## <a id="005">Test case ID: MP-DeleteMeal-005</a>

## Test case name: 
Delete meals in the specific category of the meal plan

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Verify when the mouse hovers the meal item in a specific category of the meal plan is highlighted with green colour and shows the delete icon or not
3. check that the user is able to click on the delete icon/button
4. Check that when the user clicks on the delete icon/button then the meal in the specific category of meal plan for a particular day gets deleted. Eg: In the Lunch section for Monday, the selected meal should have been deleted
5. Check the meal is also deleted from the database.

## Expected Behaviour:
Should be to able delete the meal in the specific category of the meal plan when clicking on the delete icon

## <a id="006">Test case ID: MP-EditMealPlanName-006</a>

## Test case name: 
Select User

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check in the header section, when the user clicks on the meal plan name make sure the previous meal plan name is highlighted.
3. Check to make sure it is editable such as "Vegetarian Meal Plan".
4. Check to make sure that it is automatically saved in the database.
5. Check whether the meal plan name input box accepts alphabets A-Z.
6. Check whether the meal plan name input box accepts both upper and lower case alphabets.
7. Check whether the meal plan name input box accepts numeric, special characters and symbols.

Expected Behaviour:
The user should be able to edit the meal plan name.

## <a id="007">Test case ID: MP-SelectUser-007</a>

## Test case name: 
Select User

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. On the header section when Signed in check whether the name of the user such as "Admin" is displayed
3. Check that the Dropdown is present in the header section and whether it is Clickable.
4. Check that by clicking on the dropdown a list of users is displayed.
5. Check whether the dropdown is displaying all the users or only a few as the user clicks on the dropdown.
6. Check that the user should be able to select different users such as "meal designer" in the dropdown.
7. Check to make sure that the selected user name is automatically saved in the database.
8. Check and make sure to scroll down functionality working in the dropdown list and view other user options.
9. check that the drop-down list is scrolled down by pressing the Arrow-down key on the keyboard.
10. check that the dropdown is not editable.
11. check that the dropdown values are accessible and the user is able to select by clicking on specific values in the dropdown by mouse pointer.

Expected Behaviour:
Should be able to select the user such as "meal designer" from the dropdown.

## <a id="008">Test case ID: MP-AddTag-008</a>

## Test case name:
Add tags to the meal plan

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id 
2. Check and make sure that on the header section, there is an arrow key pointing downwards by default.
3. Click on the arrow key pointing downwards to expand the view to display the description and add tag details.
4. When the view is in expanded form as that of an arrow turning upwards check the add tag input box is displayed and if it's clickable.
5. Click on the input textbox to enter the required text
6. Check whether it takes only alpha characters(A to Z).
7. Check whether it takes Numeric characters (numbers 0-9)
8. Make sure that after entering characters and when you click enter, a tag is added to the meal plan with the text that has been input in step 6
9. Check to make sure that it is automatically saved in the database.
10. Check whether there is an option to delete(X mark) the selected tag.
11. Click on the delete button to delete the tag.
12. Check to make sure that the tag is also deleted from the database.
13. Check and make sure the arrow now pointing upwards and when clicking on it should collapse the view and hide the description and tags

## Expected Behaviour:
It should allow only Alphabets and Should be able to add tags to the meal plan and when clicked delete, the selected tag should be deleted.

## <a id="009">Test case ID: MP-AddDescription-009</a>

## Test case name: 
Description of the meal plan

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check and make sure that on the header section, there is an arrow key pointing downwards by default.
3. Click on the arrow key pointing downwards to expand the view to display the description and add tag details.
4. When the view is in expanded form as that of an arrow turning upwards check the description input box is displayed and if it's clickable.
5. Check whether the description input box accepts alphabets A to Z.
6. Check whether the description input box accepts both upper and lower-case alphabets.
7. Check the maximum and minimum character length of the description box.
8. Check whether the description box accepts numeric, special characters and symbols.
9. Check to make sure that it is automatically saved in the database.
10. Check whether the user is able to view the description, after the user gets logged out and sign-in again.
11. Check and make sure the arrow now pointing upwards and when clicking on it should collapse the view and hide the description and tags

Expected Behaviour:
The user should be able to click on the Description input box and be able to enter both Alphanumeric characters and the user should be able to view the saved description after the user logins again

## <a id="010">Test case ID: MP-Logout-010</a>

## Test case name: 
Check whether the user can log out successfully

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check after successful login such as "Admin", the logout button is visible on the top right corner of the webpage.
3. Check whether the logout button is clickable or not.
4. Check whether the user is able to log out successfully by clicking on the logout button.
5. After successful logout users should be able to view the sign-in page of the meal planner website.
6. After logout check whether the user is able to log in again by clicking on the back button on the sign-in page of the meal planner website.
7. Check by logging into more than one browser and log out from any of them and check whether other accounts are properly working or all get logged out.
8. Check the logout option should not be visible till the user is logged in.
9. After logging in with the correct user credentials, close the browser by clicking on (X) and again reopen the browser and check whether the user is logged in or automatically logged out from the meal planner website.

## Expected Behaviour:
The user should be able to log out successfully by clicking on the logout button.

## <a id="011">Test case ID: MP-Menu bar-011</a>

## Test case name: 
Check the menu is displayed properly on the top of the web page

## Steps to follow:

Prerequisite: MP-Login-001
1. Go to url/mealplan/:id
2. Check the menus are displaying properly without any congestion and properly displayed.
3. Check whether the menu is adjusting automatically or not based on the number of menus.
4. Check whether the menu item is clickable.
5. When the user clicks on the menu item such as "Plans", the user should view the "Plans" web page.
6. Check "Good Meal Plan" logo is properly visible on the menu bar of the web page.

## Expected Behaviour:
When a user clicks on the menu item such as "Plans", a user should be able to view the "Plans" web page.

## <a id="012">Test case ID: MP-MPCalendar-012</a>

## Test case name: 
User not assigned should be shown as text in the meal calendar 

## Related Bug ID: #456

## Steps to follow:
Pre-requisite: MP-Login-001
1. Go to '/mealplans'
2. Click on 'Create Meal Plan'
3. Enter the meal plan name 'Veg' and do not assign a user
4. Click on the created meal plan
5. In the meal plan calendar view, notice there is no user field next to the meal plan name.


## <a id="013">Test case ID: MP-MPSearch-013</a>

## Test case name:

Search for a meal plan based on any word of the name

## Related Bug ID: #372

## Steps to follow:

1. Pre-requisite: MP-Login-001
2. Go to '/mealplans'
3. Go to the ‘Select Meal from the list’ section of the page
4. Locate the search bar designated for searching meal plans.
5. Enter one or more characters from a word from the name of any existing meal plan into the search bar.
6. Check whether the search results include the meal plan whose name contains the entered word.
7. Verify that the search results display relevant meal plans matching the search criteria.
8. Select any of the displayed meal plans from the search results.
9. Add the meal to the proper timeslot of the Meal Plan table
10. Confirm that the selected meal plan is navigated to and displayed on the screen.

## Expected Behaviour:

Upon entering a word from the name of any existing meal plan into the search bar and initiating the search, the system should return relevant search results containing meal plans whose names contain the entered word. Users should be able to select a meal plan from the search results, and upon selection, by adding the meal to the proper timeslot of the Meal Plan table the corresponding meal plan should be displayed on the screen.


## <a id="014">Test case ID: AA-Autocomplete-014</a>

## Test case name:

Enable autocomplete feature for Products and Meals fields in admin app measure form

## Related Bug ID: #482

## Steps to follow:

1. Pre-requisite: MP-Login-001.
2. Log in to the admin app (AA). 
3. From the Local Navigation Bar, access to the "Measures" form.
4. Navigate to the Measure form in the admin app.
6. Go to \Create
5. From the input blocks in the form, locate the "Products" and "Meals" fields.
7. Start typing in the Products or Meals field.
8. Check whether the autocomplete feature suggests appropriate items based on characters of the user input.
9. Verify that the dropdown displays all available products or meals matching the entered text.
10. Select a product or meal from the autocomplete suggestions.
11. Confirm that the selected item is populated in the corresponding field of the measure form.

## Expected Behaviour:

When users fill in step 9, when the Products or Meals fields in the admin app measure form, the autocomplete feature should suggest appropriate items based on the user input. Users should be able to select the correct product or meal from the autocomplete suggestions, improving the user experience and accuracy of data entry.

**Failed Case: ** Autocomplete feature suggests inappropriate items when user types more than one character. For example trying to find "Onion" by typing "ONI", it suggests "Iodized Salt Table".

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/0bda33d0-9730-41de-a173-78c7759bab95)


## <a id="015">Test case ID: MP-FilterByTags-015</a>

## Test case name:

Filter meal plans by tags

## Related Feature: Filter by tags for meal plan #522

## Steps to follow:

1. Pre-requisite:MP-Login-001.
2. Navigate to the meal plans section.
3. Locate the "Filter by tags" view.
4. Check whether the list of unique meal plan tags is automatically displayed.
5. Verify that the listed tags include all tags associated with existing meal plans.
6. Select one of the displayed tags from the list.
7. Confirm that the meal plans displayed are filtered based on the selected tag.
8. Select another tag from the list.
9. Verify that the meal plans displayed are now filtered based on both selected tags.
10. Clear the selected tags.
11. Confirm that all meal plans are displayed again without any filtering.

## Expected Behaviour:

Upon accessing the "Filter by tags" view in the meal planner application, users should be able to view a list of unique meal plan tags automatically. The list should dynamically update to reflect any changes in meal plans, such as creation or deletion, ensuring that all tags associated with existing meal plans are accurately displayed. Users should be able to filter meal plans by selecting one or more tags from the list, with the displayed meal plans updating accordingly. Additionally, users should have the option to clear selected tags to view all meal plans without filtering.


## <a id="016">Test case ID: AA-MultipleTags-016</a>

## Test case name:

Verify creation of multiple tags for a product in Admin app product page

## Related Bug: [BUG] multiple tags are not getting created in Admin app product page #483

## Steps to follow:

1. Pre-requisite: MP-Login-001.
2. Log in to the admin app (AA). 
3. Navigate to the 'products/create' page or edit an existing product.
4. Scroll down to the 'tags' entry field.
5. Enter more than one tag separated by commas (e.g., "vegan,grocery") into the 'tags' field.
6. Click the 'Save' button to save the product.
7. Verify that the product is saved successfully without any error messages.
8. Navigate back to the product details page or search for the product in the product list.
9. Check the tags associated with the product.
10. Confirm that all tags entered in the 'tags' field during creation/editing are displayed and associated with the product.

## Expected Behaviour:

When multiple tags are entered into the 'tags' field for a product during creation or editing, the system should correctly create and associate all tags with the product. Each tag entered should be treated as a separate tag, and the tags displayed for the product should reflect all entered tags without any loss or truncation.

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/6abed09d-03de-4c96-ad34-f53e1892f7b0)



## <a id="017">Test case ID: MP-CalenderUsername-017</a>

## Test case name:

Verify display of "no user assigned" on meal plan calendar when no user is assigned

## Related Bug: Username will be displayed as no user assigned on meal plan calendar #458

## Steps to follow:

1. Pre-requisite: MP-MPCalendar-002.
2. Navigate to the meal plan calendar page where meal plans are displayed.
3. Go to \Create.
4. Create a new meal plan with a user assigned to it. 
5. Verify that on the meal plan calendar, the username associated with the meal plan is displayed.
6. Go to \Create.
7. Create a new meal plan without assigning any user to it. 
8. Check for a meal plan that has no user assigned to it.
9. Refresh or navigate back to the meal plan calendar page.
10. Confirm that "no user assigned" is displayed instead of the username.

## Expected Behaviour:

When a meal plan has no user assigned to it, the meal plan calendar should display "no user assigned" instead of a username. This ensures clarity and indicates that the meal plan is not assigned to any specific user. Upon assigning a user to the meal plan, the respective username should be displayed on the calendar.

## Test Results:

Passed all the steps except the step 10. Instead of display "no user assigned", it doesn't show anything. The screenshot attached the output. 

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/b5473120-fc36-4a1f-a42b-8a8994732b9b)


## <a id="018">Test case ID: AA-DeleteMeal-018</a>

## Test case name:
Verify deletion of a meal from the meals table without foreign key constraint error

## Related Bug: Deleting a meal from the meals table throws an error foreign key constraint #426

## Steps to follow:
1. Pre-requisite: MP-Login-001.
2. Log in to the Admin App (AA). 
3. Navigate to the Meals section in the Admin App.
4. Identify a meal entry in the meals table that you want to delete.
5. Click on the checkbox next to the meal entry to select it for deletion.
6. Click on the 'Delete' button to initiate the deletion process.
7. Verify that the system does not display any error message related to foreign key constraint violations.
8. Confirm that the selected meal entry is deleted from the meals table.
9. Refresh the page or navigate back to the meals table to ensure that the deleted meal entry is no longer present.

## Expected Behaviour:
Upon selecting and deleting a meal entry from the meals table, the system should successfully delete the entry without encountering any foreign key constraint errors. The meal entry should be removed from the meals table as expected.

## Test Results:
Passed.

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/bbbde30c-a13f-4af4-9446-c07bc36b59eb)

After deleting the meal. 
![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/ada028a6-a4cc-4b6a-afd0-e64582e1f315)


## <a id="019">Test case ID: MP-LoginErrorDisplay-019</a>

## Test case name:
Verify display of error message when hitting enter with invalid credentials in the login page

## Related Bug: Error message is not displayed when you hit enter while using invalid credentials #413

## Steps to follow:
1. Pre-requisite: MP-Login-001.
2. The meal planner app should be accessible and running.
2. Navigate to the Login page of the meal planner app.
3. Enter invalid credentials such as 'admin' for username and 'pass' for password.
4. Press the 'Enter' key on the keyboard.
5. Check if an error message indicating the login failure due to wrong credentials is displayed.
6. Verify that the error message clearly states that "invalid user credentials".

## Expected Behaviour:
Upon entering invalid credentials and pressing the 'Enter' key, the system should display an error message indicating that the login failed due to wrong credentials. The error message should clearly inform the user about the incorrect credentials entered.

## Test Results:
Passed in all steps. 
![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/cab4aed3-a0e9-4abe-b4c9-eeb3bb915afe)


## <a id="020">Test case ID: MP-DuplicateMealPlan-020</a>

## Test case name:

Create a duplicate meal plan from an existing meal plan.

## Related Bug: Duplicate meal plan #377

## Steps to follow:

1. Pre-requisite: MP-Login-001.
2. Navigate to the existing meal plan that you want to duplicate.
3. Open the meal plan and review its details.
4. Look for an option or button to duplicate the meal plan.
5. Click on the duplicate button.
6. Provide a new name or identifier for the duplicated meal plan.
7. Confirm the duplication process.
8. Verify that the duplicated meal plan is created successfully.
9. Check that the content of the duplicated meal plan matches the original one.
10. Ensure that any assigned tags, descriptions, or other details are also copied to the duplicated meal plan.

## Expected Behaviour:

When duplicating a meal plan, the system should create an exact replica of the original meal plan, including all its content, tags, descriptions, and other associated details. The duplicated meal plan should have a new identifier to differentiate it from the original, and it should be created successfully without any loss of data.

## Test Results:

All steps passed successfully. The duplicated meal plan was created with the expected content and details matching the original meal plan.
