# Test case Portfolio v 1.0

| S.No | Test case ID   | Test case name                                         |
|:-----|:---------------|--------------------------------------------------------|
| 1 | [MP-Login-001](#001) | Login with meal designer credentials          |
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
| 12| [MP-DeleteMeasureTable-033](#033) | Verify deletion of measure table                                           |

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
| 21 | [MP-FilterByTagMeals-021](#021) | Filter meals by tags on the meals page |
| 22 | [AA-ProductDropdownDisplay-022](#022) | Verify all products are displayed in the product dropdown when creating a measure in Admin app|
| 23 | [AA-SearchBarProducts-023](#023) | Verify the presence and functionality of the search bar in Products section of the Admin App|
| 24 | [MP-IconHoverColor-024](#024) | Verify the hover effect of the trash can and shopping cart icons in the meal plans page |
| 25 | [MP-ConfirmDelete-025](#025) | Confirm deletion of a meal plan when clicking the trash icon |
| 26 | [MP-FavouritesHover-026](#026) | Verify favorites/heart icon turns red on mouse hover |
| 27 | [MP-ProductQuantityUpdate-027](#027) | Verify updating the Quantity and Unit for the product Lettuce |
| 28 | [AA-SearchBarMeals-028](#028)| Verify the presence and functionality of the search bar in the Admin App (Meals) | 
| 29 | [MP-InsertTooltip-029](#029) | Insert tooltip for name and description on the meal plan creation page |
| 30 | [MP-FilterByTags-030](#030) | Verify automatic listing of meal plan tags for filtering |
| 31 | [MP-Template-031](#031) | Verify the functionality of creating and filtering meal plan templates |
| 32 | [MP-AddPrepCookPortions-032](#032) | Verify addition of prep time, cook time, and portions to the Meal UI      |
| 33 | [MP-DeleteMeasureTable-033](#033) | Verify deletion of measure table                                           |
| 34 | [AA-ProductKeywordsSpaces-034](#034) | Verify ability to use spaces in product keywords and tags in Admin UI   |
| 35 | [AA-IngredientCreationError-035](#035) | Verify successful creation of ingredients in Admin UI without error   |
| 36 | [AA-ImageVideoEmbedding-036](#036) | Verify embedding of images and videos for meals in the meal planner interface |
| 37 | [AA-IngredientCodeUnique-037](#037) | Ensure ingredient code is unique for each meal |
| 38 | [AA-MealsShowPage-038](#038) | Verify the presence of a show page and show button for meals in the admin UI, and ensure that edit redirects to the show page instead of the meals list |
| 39 | [MP-MyFavouriteMeal-039](#039) | Displaying user's favorite meals |
| 40 | [MP-UpdateMealTable-040](#040) | Update meal table with prep time, cook time, and portions |
| 41 | [AA-UpdateIngredientTable-041](#041) | Verify Admin UI changes for ingredient table and product table             |
| 42 | [AA-MealDesignerModify-042](#042) | Verify meal designer's ability to modify meals, products, and nutrition using admin UI |






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

## <a id="021">Test case ID: MP-FilterByTagMeals-021</a>

## Test case name:

Filter meals by tags on the meals page.

## Related Feature: Filter by tag for meals page #517

## Steps to follow:

1. Pre-requisite: MP-Login-001.
2. Navigate to the meals page in the meal planner app.
3. Look for the filter options menu.
4. Check for the presence of the "Filter by tag" option.
5. Click on the "Filter by tag" option.
6. Verify that a list of available tags is displayed.
7. Select one or more tags from the list.
8. Confirm the selection.
9. Check that the meals displayed on the page are filtered based on the selected tags.
10. Ensure that only meals tagged with the selected tags are shown, while others are hidden.

## Expected Behaviour:

When filtering meals by tags, the system should provide a list of available tags to choose from. Upon selecting one or more tags, the meals page should display only those meals that are tagged with the selected tags. This helps users to quickly find meals based on specific criteria and improves navigation within the application.

## Test Results:

All steps passed successfully. The meals were filtered based on the selected tags, and only the relevant meals were displayed on the page.


## <a id="022">Test case ID: AA-ProductDropdownDisplay-022</a>

## Test case name:
Verify all products are displayed in the product dropdown when creating a measure in Admin app.

## Related Bug: [BUG] When creating measure, not all products displayed in Admin app #482

## Steps to follow:

1. Go to the 'measures/create' page in the Admin app.
2. Click on the dropdown menu for selecting the product.
3. Verify that all available products are listed in the dropdown menu.
4. Check if the desired product for creating a measure is visible in the dropdown menu.

## Expected Behavior:
When creating a measure in the Admin app, the dropdown menu for selecting the product should display all available products. This ensures that users can select the desired product without any limitations.

## Test Results:
All steps passed as expected. All available products were displayed in the dropdown menu, allowing the user to select the desired product for creating a measure.


## <a id="023">Test case ID: AA-SearchBarProducts-023</a>
## Test case name:
Verify the presence and functionality of the search bar in the Admin App (Products)

## Related Feature: No search bar on Admin App (Products) #505

## Steps to follow:
1. Open the Admin App and navigate to the Products section.
2. Look for the presence of a search bar at the top of the Products page.
3. Enter a specific keyword, product name, code, UPC, or tag in the search bar.
4. Verify that the products displayed on the page are filtered based on the entered keyword.
5. Confirm that the search results are relevant and match the entered criteria.

## Expected Behaviour:
The Products section in the Admin App should contain a search bar allowing users to search for products by name, code, UPC, or tags. Upon entering a search query, the displayed products should be filtered accordingly, presenting relevant search results to the user.

## Test Results:
The test failed. The search bar was present in the Admin App (Products) section, but searching for specific keywords filtered the products inappropriately. Issue #593 addresses it. 

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/9db4c74b-b318-426a-88a8-703f569647bb)



## <a id="024">Test case ID: MP-IconHoverColor-024</a>

## Test case name:
Verify the hover effect of the trash can and shopping cart icons in the meal plans page

## Related Bug: [BUG] trash can and shopping cart icons not turning green when hovering the mouse over #459

## Steps to follow:
1. Pre-requisite: MP-Login-001.
2. Open the meal plans page by navigating to '/mealplans'.
3. Hover the mouse over the trash can icon.
4. Hover the mouse over the shopping cart icon.
5. Verify the trash can icon and shopping card icon should turn green when the mouse is hovered over it.


## Expected Behaviour:
- The trash can icon should turn green when the mouse is hovered over it.
- The shopping cart icon should turn green when the mouse is hovered over it.

## Test Results:
The test passed as the trash can and shopping cart icons changed color to green when hovered over. 

![Screenshot (3)](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/84db54a7-15ba-4142-9d37-6ebef28cc4b8)


## <a id="025">Test case ID: MP-ConfirmDelete-025</a>

### Description
When deleting a meal plan from the meal plans page, a confirmation dialogue should be displayed to confirm the action.

### Steps to Reproduce
1. Pre-requisite: MP-Login-001.
2. Navigate to the meal plans page '/mealplans'.
3. Locate the meal plan you want to delete.
4. Click on the trash can icon associated with the meal plan.
   
### Expected Behavior
A confirmation dialogue should appear, asking the user to confirm the deletion of the meal plan.
 
## Test Results:
The test passed as dialogue appeared, asking the user to confirm the deletion of the meal plan.

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/96cccf0f-274d-4ae2-a36d-0c1a83ba4fad)


## <a id="026">Test case ID: MP-FavouritesHover-026</a>

## Test case name:
Verify favourites/heart icon turns red on mouse hover

## Related Bug: Favourites icon doesn't turn red on mouse hover #476

## Steps to follow:
1. Pre-requisite: Access to the meal plans page: MP-Login-001..
2. Navigate to the meal plans page.
3. Locate the favourites/heart icon.
4. Hover the mouse over the favourites/heart icon.
5. Observe the colour change of the icon.

## Expected Behaviour:
When the mouse is hovered over the favourites/heart icon, it should turn red, indicating that it is selected or active.

## Test Results:
The test passed as the favourites/heart icon changed color to red when hovered over. 

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/a5cd7fd2-8318-45f1-9a44-7969a69b8d10)


## <a id="027">Test case ID: MP-ProductQuantityUpdate-027</a>

## Test case name:
Verify updating the Quantity and Unit for the product Lettuce

## Related Bug: Updating the Quantity and Unit for the product Lettuce #489

## Description:
Ensure that the product Lettuce is correctly updated to be listed as 1 each in the products table, instead of 3 count.

## Steps to follow:
1. Pre-requisite: MP-Login-001.
2. Open the Admin App and navigate to the Products section.
3. Look for the presence of Lettuce in the Products page.
2. Update the quantity and unit, the cost and product link for Lettuce in the recipes_seed.sql file to 1 each.
4. Run the seed SQL script to populate the database with the updated data.
5. Verify that Lettuce is listed as 1 ea in the products table.

## Expected Behaviour:
After updating the quantity and unit for Lettuce, it should be correctly listed as 1 ea in the products table.

## Test Results:
This test case is marked as obsolete since there is no lettuce in the database to perform the verification.


## <a id="028">Test case ID: AA-SearchBarMeals-028</a>

## Test case name:
Verify the presence and functionality of the search bar in the Admin App (Meals)

## Related Feature: No search bar on Admin App (Meals) #457

## Steps to follow:
1. Pre-requisite: MP-Login-001.
2. Open the Admin App and navigate to the Meals section.
3. Look for the presence of a search bar at the top of the Meals page.
4. Enter a specific keyword, meal name, category, tag, or any other relevant information in the search bar.
5. Verify that the meals displayed on the page are filtered based on the entered keyword.
6. Confirm that the search results are relevant and match the entered criteria.

## Expected Behaviour:
The Meals section in the Admin App should contain a search bar allowing users to search for meals by name, category, tag, or any other relevant information. Upon entering a search query, the displayed meals should be filtered accordingly, presenting relevant search results to the user.

## Test Results:
The test passed. The search bar was present in the Admin App (Meals) section, and searching for specific keywords appropriately filtered the meals.
![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/09ca4c34-9dda-4da5-8cd1-a1b994283959)



## <a id="029">Test case ID: MP-InsertTooltip-029</a>

## Test case name:
Insert tooltip for name and description on the meal plan creation page

## Related Feature: Insert a tooltip for name and description on the meal plan creation page #518

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Navigate to the meal plan creation page.
2. Locate the input field for entering the meal plan name.
3. Hover over the input field to trigger the tooltip.
4. Verify that the tooltip suggests a convention for naming the meal plan, such as 'Client # Week #' for admins/designers, or 'Family member name Week #' for users.
5. Repeat steps 2-4 for the description input field.
6. Verify that the tooltip suggests adding notes based on the discussion with the client about their requirements and suggestions.

## Expected Behaviour:
When hovering over the input fields for meal plan name and description during creation, tooltips should appear suggesting naming conventions and providing guidance on what to include in the description, tailored to the user's role (admin/designer or user).

## Test Results:
Passed. 

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/5a2158ec-8809-45c6-9109-eae9d458b8ce)


## <a id="030">Test case ID: MP-FilterByTags-030</a>
## Test case name:
Verify automatic listing of meal plan tags for filtering

## Related Feature: Filter by tags for meal plan #522

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Create a meal plan.
2. Navigate to the "Filter by tags" view in the meal planner.
3. Verify that the list of meal plan tags is automatically updated to reflect the changes made in step 1.

## Expected Behaviour:
After creating or deleting a meal plan, the list of meal plan tags should be automatically updated on the "Filter by tags" view without requiring a page refresh or navigating to a different option.

## Test Results:
Passed as the list of meal plan tags automatically updated on the "Filter by tags" view without requiring a page refresh or navigating to a different option.

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/af3102a4-45c4-4053-9be0-b9a962997e5d)

## <a id="031">Test case ID: MP-Template-031</a>

## Test case name:
Verify the functionality of creating and filtering meal plan templates

## Related Feature: Template for meal plan #548

## Steps to follow:
1. Log in as a meal designer or admin.
2. Navigate to the meal planner section for creating a new meal plan.
3. Create a new meal plan and select the option to save it as a template.
4. Verify that the meal plan is saved successfully as a template and no user is assigned to it.
5. Navigate to the search view in the meal planner.
6. Apply a filter to display only the templates.
7. Confirm that the list of meal plans shown now includes only the templates created in step 3.

## Expected Behaviour:
When creating a meal plan, the user should have the option to save it as a template, which will not assign any user to it. The user should then be able to filter the meal plans to display only templates, and the list should include the templates created by the user.

## Test Results:
Passed as the user is able to filter the meal plans to display only templates, and the list included the templates created by the user.

## <a id="032">Test case ID: MP-AddPrepCookPortions-032</a>

## Test case name:

Verify addition of prep time, cook time, and portions to the Meal UI

## Related Feature: [FEATURE] adding prep time, portions, cook time to the Meal UI #529

## Steps to follow:
 Pre-requisite: MP-Login-001.
1. Access to the Meal UI with the ability to view and edit meal details.
2. Navigate to the Meal UI page or the page where meal details are displayed.
3. Check for the presence of UI elements that display prep time, cook time, and portions for each meal.
4. Verify that there are distinct UI elements for displaying prep time, cook time, and portions.
5. Create a new meal or edit an existing meal.
6. Enter values for prep time, cook time, and portions in the respective UI elements.
7. Save the changes to the meal.
8. Confirm that the entered values for prep time, cook time, and portions are saved successfully.
9. Navigate back to the Meal UI page or refresh the page to view the updated meal details.
10. Check that the prep time, cook time, and portions for the meal are displayed correctly in the UI elements.

## Expected Behaviour:

The Meal UI should include dedicated UI elements for displaying prep time, cook time, and portions for each meal. Users should be able to enter values for these attributes when creating or editing a meal, and the entered values should be saved and displayed accurately in the UI.

## Test Results:
Passed.

## <a id="033">Test case ID: MP-DeleteMeasureTable-033-033</a>

## Test case name:
Delete measure table

## Related Issue: #568

## Description:
Users should be able to delete the measure table to accommodate changes related to the match issue.

## Steps to follow:
 Pre-requisite: Go to v1 of the MealPlanner, MP-Login-001.
1. Navigate to the measure table section from the shopping list .
2. Locate the option to the measure table.
4. Confirm the deletion of the measure table.

## Expected Behavior:
Upon deletion, the measure table should be successfully removed from the system, allowing for changes related to the match issue.

## Test Results:
Passed in V1, not available in v2 as according to the issue #603 Shopping list under the construction.

## <a id="034">Test case ID: AA-ProductKeywordsSpaces-034</a>

## Test case name:

Verify ability to use spaces in product keywords and tags in Admin UI

## Related Bug: [BUG] In admin UI, tags and product keywords could not have spaces #584

## Steps to follow:

1. Pre-requisite: Access to the Admin UI with permissions to manage products and tags.
2. Navigate to the Admin UI for managing products.
3. Select a specific product for editing or creating a new product.
4. Scroll down to the section for Product Keywords.
5. Attempt to enter a product keyword containing spaces, such as 'egg noodles' or 'feta cheese'.
6. Confirm whether the system allows entering spaces between words in the product keyword field.
7. Similarly, navigate to the section for managing tags.
8. Attempt to create or edit a tag containing spaces.
9. Verify whether the system allows using spaces in tag names.
10. If spaces are allowed, save the changes and ensure they are persisted correctly in the system.
11. If spaces are not allowed, validate that the system displays appropriate error messages or warnings.

## Expected Behaviour:

In the Admin UI for managing products and tags, users should be able to use spaces in product keywords and tag names. Spaces should be accepted and processed correctly without any restrictions, allowing users to input phrases or multi-word descriptors for products and tags. This ensures flexibility and ease of use in managing product information and categorization.

## Test Results:
Passed as in the Admin UI for managing products and tags, users could use spaces in product keywords and tag names successfully. 

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/f4dea039-62a3-44a8-9b95-3ea082f14e3b)


## <a id="035">Test case ID: AA-IngredientCreationError-035</a>

## Test case name:

Verify successful creation of ingredients in Admin UI without error

## Related Bug: [BUG] When we try to create an ingredient we get an error #595

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Access to the Admin UI with permissions to manage ingredients.
2. Navigate to the Admin UI for managing meals.
3. Select a specific meal to which ingredients need to be added.
4. Click on the "Ingredients" section within the meal details.
5. Click on the "Create" button to add a new ingredient.
6. Fill up the required fields with appropriate values, such as ingredient name, quantity, etc.
7. Verify that all mandatory fields are properly filled.
8. Attempt to save the ingredient by clicking on the "Save" or "Submit" button.
9. Confirm whether the system successfully adds the ingredient without displaying any error messages.
10. Check if the newly created ingredient appears in the list of ingredients for the selected meal.
11. If any error message is displayed, note down the details of the error.

## Expected Behaviour:

In the Admin UI for managing meals, users should be able to create ingredients without encountering any errors. Upon filling up the required fields and saving the ingredient, the system should add it successfully to the meal without any issues. Any error messages or unexpected behavior during ingredient creation should be addressed to ensure smooth functionality of the system.

## Test Results:
Passed as in the Admin UI users is able to create ingredients without encountering any errors.

## <a id="036">Test case ID: AA-ImageVideoEmbedding-036</a>

## Test case name:

Verify the embedding of images and videos for meals in the meal planner interface.

## Related Feature: [FEATURE] Adding Image and Video as embedded rather than a URL or text #566

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Pre-requisite: Access to the Admin UI with permissions to manage ingredients.
2. Navigate to the meal details page for a specific meal.
3. Locate the sections for adding images and videos for the meal.
4. Upload or provide links to images and videos associated with the meal.
5. Check whether the images are embedded as thumbnails within the meal details.
6. Verify that the videos are embedded and playable within the meal details.
7. Ensure that the embedded images and videos are clearly distinguishable and identifiable.
8. Attempt to click on the embedded images to view them in full size, if applicable.
9. Try playing the embedded videos to confirm their functionality and quality.
10. Repeat the above steps for multiple meals with different images and videos.

## Expected Behaviour:

In the meal planner interface, images and videos associated with meals should be embedded as thumbnails and playable content, respectively, rather than displayed as plain text or URLs. This enhancement should improve the user experience by providing a more visually appealing and intuitive way to view and interact with meal-related media.

## Test Results:
Passed
![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/92612b0b-28ef-4a5a-a06d-8bcf3224f54f)


## <a id="037">Test case ID: AA-IngredientCodeUnique-037</a>

## Test case name:

Ensure ingredient code is unique for each meal

## Related Bug ID: #592

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Go to the admin page.
2. Click on Meals.
3. Select a meal, for example, "Amish Pie".
4. Select Ingredients for the meal.
5. Assign code "1" to the first ingredient.
6. Select another meal.
7. Select Ingredients for the second meal.
8. Attempt to assign a code e.g., "112" to the first ingredient again.
9. Verify if an error message "duplicate key value violates unique constraint 'ingredient_code_key'" is thrown.

## Expected Behaviour:

Ingredient codes should be unique for each meal, preventing the duplication of codes across different meals in the system.

## Test Results:
Passed successfully.


![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/9f63b6ca-0450-410a-858b-2a58795ebab9)


## <a id="038">Test case ID: AA-MealsShowPage-038</a>

## Test case name:

Verify the presence of a show page and show button for meals in the admin UI, and ensure that edit redirects to the show page instead of the meals list.

## Related Feature: [FEATURE] Meals has a show page and a show button in admin UI and edit redirects to Show instead of meals list #590

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Pre-requisite: Access to the Admin UI with permissions to manage meals.
2. Navigate to the Admin UI for managing meals.
3. Select a specific meal for editing or viewing.
4. Confirm the presence of a show button associated with the selected meal.
5. Click on the show button to access the show page for the meal.
6. Verify that the show page displays all relevant details and attributes of the meal, including its name, description, ingredients, and any other pertinent information.
7. If available, navigate back to the list of meals.
8. Repeat steps 3-5 for a different meal, ensuring consistency in the presence and functionality of the show button.
9. Now, attempt to edit a meal by clicking on the edit button or link.
10. After making changes to the meal, save the edits and observe the redirection behavior.
11. Confirm whether the edit operation redirects the user to the corresponding show page for the edited meal instead of the meals list page.
12. If necessary, navigate back to the list of meals and repeat the edit process for another meal to validate consistency in redirection behavior.

## Expected Behaviour:

In the Admin UI for managing meals, there should be a dedicated show page for each meal along with a show button for convenient access. When editing a meal, saving the changes should automatically redirect the user to the show page for the edited meal, enhancing user experience by eliminating the need to search for the edited meal again in the meals list.

## Test Results:
Passed successfully as there is a dedicated show page for each meal along with a show button for convenient access.


![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/20897bca-c504-4325-9385-2ce7ef1c8d17)


## <a id="039">Test case ID: MP-MyFavouriteMeal-039</a>

## Test case name:
Displaying user's favorite meals

## Related Feature ID: #516

## Description:
This feature allows users to view their favorite meals easily.

## Steps to follow:
Pre-requisite: MP-Login-001.
1. Log in to the application with valid credentials.
2. Navigate to the "My Favorite Meals" section.
3. Ensure that only the favorite meals of the currently logged-in user are displayed.
4. Verify that the favorite meals are listed in a user-friendly format.
5. Check if there is an option to select or interact with the favorite meals for further actions.

## Expected Behavior:
- Only the favorite meals of the currently logged-in user should be displayed.
- The favorite meals should be presented in a clear and understandable format.
- Users should be able to easily select or interact with their favorite meals as needed.

## Test Results:
Passed as only the favorite meals of the currently logged-in user is displayed.



## <a id="040">Test case ID: MP-UpdateMealTable-040</a>

### Test case name:
Update meal table with prep time, cook time, and portions

### Related Feature ID: #537

### Description:
This feature updates the meal table to include columns for preparation time, cooking time, and portions.

### Steps to follow:
Pre-requisite: MP-Login-001.
1. Log in to the application with valid credentials.
2. Navigate to the "Meal" section or any relevant page displaying meal information.
3. Check for the presence of columns labeled "Prep Time," "Cook Time," and "Portions" in the meal table.
4. Verify that the data displayed in these columns corresponds to the preparation time, cooking time, and portions of each meal.
5. Ensure that the columns are labeled correctly and clearly visible to users.

### Expected Behavior:
The expected behavior is that after the update, the meal table should display three new columns: "Prep Time," "Cook Time," and "Portions." These columns should accurately reflect the preparation time, cooking time, and portions of each meal respectively. The data in these columns should be clearly visible and properly aligned with the corresponding meal entries in the table. Additionally, the labels for these columns should be correctly displayed.

### Test Results:
Test case passed: All steps were successfully executed, and the expected behavior was observed.
![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/efc96cac-aeeb-42ad-ae56-0de3fd7a217a)

## <a id="041">Test case ID: AA-UpdateIngredientTable-041</a>

## Test case name:

Verify Admin UI changes for ingredient table and product table

## Related Feature: [FEATURE] Admin UI changes for ingredient table and product table #543

## Steps to follow:

1. Pre-requisite: Access to the Admin UI.
2. Navigate to the ingredient table section in the Admin UI.
3. Verify that the new ingredient table is displayed with the updated columns as per the solution described in the feature request.
4. Check for options to create, edit, and delete columns in the ingredient table.
5. Ensure that the Admin UI provides functionality to add, modify, and remove ingredients in the ingredient table.
6. Navigate to the product table section in the Admin UI.
7. Verify that the product table reflects the changes made in the ingredient table.
8. Check for options to create, edit, and delete columns in the product table.
9. Ensure that the Admin UI provides functionality to add, modify, and remove products in the product table.

## Expected Behaviour:

The Admin UI should accurately reflect the changes made to the ingredient table and product table as per the feature request #543. Users should be able to seamlessly create, edit, and delete columns, ingredients, and products using the updated Admin UI.

## Test Results: 
Passed.

![image](https://github.com/CivicTechFredericton/mealplanner/assets/59191427/7479967d-ea74-4f19-869b-80de3cec915d)

## <a id="042">Test case ID: AA-MealDesignerModify-042</a>

## Test case name:

Verify meal designer's ability to modify meals, products, and nutrition using admin UI

## Related Feature: [FEATURE] Meal designer should be able to use admin UI to modify meals, products, nutrition #588

## Steps to follow:

1. Pre-requisite: Access to the Admin UI with permissions assigned as a meal designer.
2. Navigate to the meals section in the Admin UI.
3. Verify that as a meal designer, you have access to modify existing meals, including recipes, ingredients, products, and nutrition details.
4. Check for options to add, edit, and delete meals.
5. Ensure that the Admin UI provides functionality to modify ingredients, products, and nutrition associated with meals.
6. Navigate to the products section in the Admin UI.
7. Verify that as a meal designer, you can modify existing products used in meal recipes.
8. Check for options to add, edit, and delete products.
9. Ensure that the Admin UI provides functionality to modify details such as ingredients, nutrition, and availability for products.
10. Navigate to the nutrition section in the Admin UI.
11. Verify that as a meal designer, you have access to modify nutrition information for meals and products.
12. Check for options to add, edit, and delete nutrition details.
13. Ensure that the Admin UI provides functionality to update nutritional values and specifications for meals and products.

## Expected Behaviour:

Meal designers should be able to utilize the Admin UI to modify meals, products, and nutrition details as described in the feature request #588. They should have access to the necessary functionalities to manage recipes, ingredients, and nutritional information while excluding user administration capabilities typically reserved for admins.

### Test Results:
Test case passed. 
