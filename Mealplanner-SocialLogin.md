# Implementation of Social Login Use Case:
## Description:
Add Google and Facebook login support alongside the existing standard login (username/password), allowing users the flexibility to access the Mealplanner application through their preferred login method.

## Use Cases:
- Use Case ID: UC-001
- Use Case Name: Register Social Login User
- Actor(s): Admin
- Description: This use case describes the steps an admin takes to regsiter a new/existing user with their mode of social login (Google or Facebook) to the system.
- Preconditions: The admin must be logged in to the Mealplanner Admin application.
- Postconditions: A new social login user is registered with their mode of login and status defaults to "Pending" to access the Mealplanner application.
- Main Flow:
	- Social Login Users:
		1. Admin clicks on "Register User" Button.
		2. System displays a form to input user details - name, emailID, role (admin, meal-designer, client), status (active, inactive, pending), modeOfLogin (Google or Facebook).
		3. By default, the resgistered social login user must be in the pending status.
		4. Admin fills out the form and clicks "Register".
		5. System validates inputs and registers the user to the application.
		6. Admin should have access to edit/delete the social login user anytime.
- Alternate Flow:
	- A1: System displays appropriate error messages for missing/invalid inputs.
	- A2: If email already exists in the system, show an error message.
- **To be Noted:** Under Users tab there will be 2 subtabs:
	- Standard Login Users (remains unaffected). 
	- Social Login Users (new addition).


- Use Case ID: UC-002
- Use Case Name: Login with Google
- Actor(s): User
- Description: New usee case 